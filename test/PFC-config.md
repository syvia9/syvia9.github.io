1. config  PFC feature:
   def test_hw_pfc_complete_config(self):
......
        # Quanta value
        quanta_value_1 = int((PORT_SPEED / PFC_QUANTA_BIT_VALUE) * QUANTA_1)
        self.mac_port.set_pfc_quanta(QUANTA_1)

        # Periodic timer
        timer_value_1 = int((PORT_SPEED / PFC_QUANTA_BIT_VALUE) * TIMER_1)
        self.mac_port.set_pfc_periodic_timer(TIMER_1)

        # Mac port enable
        self.mac_port.set_fc_mode(sdk.la_mac_port.fc_direction_e_BIDIR, sdk.la_mac_port.fc_mode_e_PFC)
        self.mac_port.set_pfc_enable(TC_BITMAP)
        self.mac_port.set_pfc_tc_xoff_rx_enable(TC_BITMAP)
 ......
}

I config PFC based on the test port:
1.	Enable PFC on the test port (slice =5, ifg=0, first serdes id=0):  set loopback, enable port on TC = 5 to periodically send PFC xoff packet with tx_fc_per_xoff_timer =9, 
         (Pdb)  debug_device.read_register(gibraltar_tree.slice[5].ifg[0].ifgb.fc_cfg0)
        periodic_int_en [23:0] = 0x0000001

        (Pdb) debug_device.read_register(gibraltar_tree.slice[5].ifg[0].mac_pool8[0].tx_mac_fc_per_xoff_timer[0])
        tx_fc_per_xoff_timer [15:0] = 0x00009
        tx_fc_per_xoff_en [23:16] = 0x020
        
        
2.set_pfc_quanta->set_xoff_timer_settings

mac_pool_gibraltar::set_xoff_timer_settings(la_uint8_t tc_bitmap, la_uint_t quanta)
{
    mac_pool8_tx_mac_fc_xoff_timer_register xoff_reg;

    bzero(&xoff_reg, mac_pool8_tx_mac_fc_xoff_timer_register::SIZE);

    xoff_reg.fields.tx_fc_xoff_en = tc_bitmap;
    xoff_reg.fields.tx_fc_xoff_timer = quanta;

    for (size_t serdes = m_serdes_index_in_mac_pool; serdes < m_serdes_index_in_mac_pool + m_serdes_count; serdes++) {
        la_status status;
        status = m_device->m_ll_device->write_register((*m_mac_pool_regs.tx_mac_fc_per_xoff_timer)[serdes], xoff_reg);
        return_on_error(status);

        status = m_device->m_ll_device->write_register((*m_mac_pool_regs.tx_mac_fc_xoff_timer)[serdes], xoff_reg);
        return_on_error(status);
    }

    return LA_STATUS_SUCCESS;
}

>>>debug_device.read_register(gibraltar_tree.slice[5].ifg[0].mac_pool8[0].tx_mac_fc_per_xoff_timer[0])
        tx_fc_per_xoff_timer [15:0] = 0x0ffff
        tx_fc_per_xoff_en [23:16] = 0x020
        
>>>debug_device.read_register(gibraltar_tree.slice[4].ifg[1].mac_pool8[0].tx_mac_fc_xoff_timer[0])
        tx_fc_xoff_timer [15:0] = 0x0ffff
        tx_fc_xoff_en [23:16] = 0x020
        

        
3.set_pfc_periodic_timer
   m_device->m_ifg_handlers[m_slice_id][m_ifg_id]->set_port_periodic_timer_value(m_serdes_base_id, m_serdes_count, quanta);
   
   la_status
   ifg_handler_gibraltar::set_port_periodic_timer_value:
   {
      for (size_t mac_lane = 0; mac_lane < mac_lanes_reserved_count; mac_lane++) {
        auto fc_port_cfg_0 = (*m_gibraltar_tree->slice[m_slice_id]->ifg[m_ifg_id]->ifgb->fc_port_cfg0)[mac_lane_base_id + mac_lane];
        gibraltar::ifgb_24p_fc_port_cfg0_register fc_port_cfg0;

        la_status status = m_device->m_ll_device->read_register(*fc_port_cfg_0, fc_port_cfg0);
        return_on_error(status);

        // Only update timer value in HW if we are in PFC mode
        if (fc_port_cfg0.fields.port_fc_mode == (size_t)la_mac_port::fc_mode_e::PFC) {
            fc_port_cfg0.fields.port_periodic_timer = timer_value;
            status = m_device->m_ll_device->write_register(*fc_port_cfg_0, fc_port_cfg0);
            return_on_error(status);
        }
    }

   debug_device.read_register(gibraltar_tree.slice[4].ifg[1].ifgb.fc_port_cfg0)
   debug_device.read_register(gibraltar_tree.slice[4].ifg[1].ifgb.fc_port_cfg0[0]
>>>port_pause_mask [7:0] = 0x0ff
port_pause_act_en [8:8] = 0x0
port_periodic_timer [24:9] = 0x00000
port_watch_dog_timer [40:25] = 0x0ffff
port_fc_mode [42:41] = 0x2
port_512bit_time [58:43] = 0x00007
   
 4.set_fc_mode
 
ifg_handler_base::set_fc_mode:
{
    if (m_slice_mode == la_slice_mode_e::CARRIER_FABRIC && m_device->m_fabric_ports_initialized) {
        if (fc_mode != m_device->m_fabric_fc_mode) {
            return LA_STATUS_EINVAL;
        }
    }

    /* Don't enable periodic message sending except for CFFC and PFC mode. Need to consider adding an API to enable it. */
    bool enable_periodic_send = false;
    if (fc_mode == la_mac_port::fc_mode_e::CFFC) {
        enable_periodic_send = true;
    }
    if (fc_mode == la_mac_port::fc_mode_e::PFC) {
        // Can be either enabled or disabled based on whether we are using HW PFC or SW PFC
        enable_periodic_send = m_pfc_pif_en_periodic_send_map[mac_lane_base_id];
    }

    la_status stat = set_fc_mode_periodic(mac_lane_base_id, mac_lanes_reserved_count, enable_periodic_send);
    return_on_error(stat);

    stat = set_fc_mode_port(mac_lane_base_id, mac_lanes_reserved_count, serdes_base_id, speed, fc_mode);
    return_on_error(stat);

    stat = set_fc_mode_fabric_extraction(mac_lane_base_id, m_slice_mode == la_slice_mode_e::CARRIER_FABRIC);
    return_on_error(stat);

    return LA_STATUS_SUCCESS;
}


set_fc_mode_periodic： 
la_status
ifg_handler_gibraltar::set_fc_mode_periodic(la_uint_t mac_lane_base_id, size_t mac_lanes_reserved_count, bool enable)
{
    ifgb_24p_fc_cfg0_register fc_cfg0_reg;

    la_status stat
        = m_device->m_ll_device->read_register(m_gibraltar_tree->slice[m_slice_id]->ifg[m_ifg_id]->ifgb->fc_cfg0, fc_cfg0_reg);
    return_on_error(stat);
 ......

    stat = m_device->m_ll_device->write_register(m_gibraltar_tree->slice[m_slice_id]->ifg[m_ifg_id]->ifgb->fc_cfg0, fc_cfg0_reg);
}

debug_device.read_register(gibraltar_tree.slice[4].ifg[1].ifgb.fc_port_cfg0[0])
>>>port_pause_mask [7:0] = 0x0ff
port_pause_act_en [8:8] = 0x0
port_periodic_timer [24:9] = 0x00000
port_watch_dog_timer [40:25] = 0x0ffff
port_fc_mode [42:41] = 0x2
port_512bit_time [58:43] = 0x00007

set_fc_mode_port:
{
        reg_val_list.push_back({(*ifgb->fc_port_cfg0)[mac_lane_base_id + mac_lane], fc_port_cfg0});
        reg_val_list.push_back({(*ifgb->fc_port_cfg2)[mac_lane_base_id + mac_lane], fc_port_cfg2});

}
debug_device.read_register(gibraltar_tree.slice[4].ifg[1].ifgb.fc_port_cfg0[2])
debug_device.read_register(gibraltar_tree.slice[4].ifg[1].ifgb.fc_port_cfg0[2])
>>>port_pause_mask [7:0] = 0x0ff
port_pause_act_en [8:8] = 0x0
port_periodic_timer [24:9] = 0x00000
port_watch_dog_timer [40:25] = 0x0ffff
port_fc_mode [42:41] = 0x2
port_512bit_time [58:43] = 0x00007

5.set_pfc_enable

  do_pfc_enable
  if (m_pfc_rx_counter) {add counter}
   txn.status = update_pfc_table();
  update_pfc_ssp_em_mp_table();

do_pfc_enable:
la_status status = set_source_if_to_port_map_fc_enable(true /* FC enable */);
    return_on_error(status);

    status = set_fcm_prio_map_bitmap(tc_bitmap);
    return_on_error(status);

    status = m_scheduler->set_pfc(true);
    return_on_error(status);

    for (auto port : m_mac_pool_port) {
        status = port->set_xoff_timer_settings(tc_bitmap, m_pfc_quanta);
        return_on_error(status);

        status = port->set_xon_timer_settings(tc_bitmap, 0 /* Xon timer value */);
        return_on_error(status);
    }

    status = m_device->m_ifg_handlers[m_slice_id][m_ifg_id]->set_port_periodic_int_enable(m_serdes_base_id, m_serdes_count, true);

    return_on_error(status);

    // Disable replicated/MC packets on PFC TCs.
    status = set_mc_oqueues_enable(tc_bitmap, false /* Disable */);
    return_on_error(status);
    return LA_STATUS_SUCCESS;
    }
    
    5.1 
      set_source_if_to_port_map_fc_enable:
    mainly config the rx_cgm, seems not related to our feature:
    auto source_if_to_port_map = (*m_device->m_gb_tree->rx_cgm->source_if_to_port_map)[m_slice_id];
    gibraltar::rx_cgm_source_if_to_port_map_memory source_if_to_port_map_entry;
    la_status status = m_device->m_ll_device->read_memory(*source_if_to_port_map, line_idx, source_if_to_port_map_entry);
    source_if_to_port_map_entry.fields.slice_fc_enable = (fc_enable ? 1 : 0);
    status = m_device->m_ll_device->write_memory(source_if_to_port_map, line_idx, source_if_to_port_map_entry);
    
    debug_device.read_register(gibraltar_tree.rx_cgm.source_if_to_port_map)
    
    
    5.2 
      set_fcm_prio_map_bitmap:
    
      auto fcm_prio_map = m_device->m_gb_tree->slice[m_slice_id]->ifg[m_ifg_id]->ifgb->fcm_prio_map;
   
for i in range(8):
   debug_device.read_memory(gibraltar_tree.slice[4].ifg[1].ifgb.fcm_prio_map,i)
   
>>>fcm_prio_map_data [191:0] = 0x0efefbfcffffbdefcffd79f7b7fb6f4fcdfdaef1f00000000

fcm_prio_map_data [191:0] = 0x0ddc6bcff97dbdc37df7efef7efefffdff76f7b7300000000

fcm_prio_map_data [191:0] = 0x0ffdff3ffff5fe1bff7b72ef7bf5ff79e77fffbe700000000

fcm_prio_map_data [191:0] = 0x0dffdffff876b7f3e3bffdcfdcbb7f7bfbafdecfb00000000

fcm_prio_map_data [191:0] = 0x0bfffe8ff5f7f5dbfd5fbd75df3ffffefecef7faf00000000

fcm_prio_map_data [191:0] = 0x0eff9f9ff3efffff75ff7bfd7dede7ffc5fbfb3fc20202020

fcm_prio_map_data [191:0] = 0x07f1fefed9df3fb7fd9bbe4733eef18bdf5c8ffdd00000000

fcm_prio_map_data [191:0] = 0x0fdeeff98c7af9aeddbef5ffdbfffffdb7fd72ff700000000
   
   
   debug_device.read_memory(gibraltar_tree.slice[4].ifg[1].ifgb.fcm_prio_map,0)
   debug_device.read_memory(gibraltar_tree.slice[4].ifg[1].ifgb.fcm_prio_map,1)
   debug_device.read_memory(gibraltar_tree.slice[4].ifg[1].ifgb.fcm_prio_map,2)
   debug_device.read_memory(gibraltar_tree.slice[4].ifg[1].ifgb.fcm_prio_map,3)
   debug_device.read_memory(gibraltar_tree.slice[4].ifg[1].ifgb.fcm_prio_map,4)
   debug_device.read_memory(gibraltar_tree.slice[4].ifg[1].ifgb.fcm_prio_map,5)
   debug_device.read_memory(gibraltar_tree.slice[4].ifg[1].ifgb.fcm_prio_map,6)
   debug_device.read_memory(gibraltar_tree.slice[4].ifg[1].ifgb.fcm_prio_map,7)
    
    
    
