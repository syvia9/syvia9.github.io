1. config  PFC feature:
   class test_pfc_watchdog(hw_pfc_base, pfc_watchdog, pfc_common):

    @unittest.skipIf(decor.is_graphene(), "Test is not yet enabled on GR")
    def test_hw_pfc_watchdog(self):
        self.init_common()
        self.enable_rx_counting_common(self.topology.rx_eth_port)
        ***self.mac_port.set_fc_mode(sdk.la_mac_port.fc_direction_e_BIDIR,*** 
                                  ***sdk.la_mac_port.fc_mode_e_PFC)***  
        self.pfc_rx_counter = self.device.create_counter(8)
        self.mac_port.set_pfc_enable((1 << TC_VALUE))
        self.mac_port.set_pfc_counter(self.pfc_rx_counter)
        self.enable_rx_counting(self.topology.rx_eth_port)
        self.watchdog_test(self.mac_port)
  The bold and italic part will call an IFG API ifg_handler_base::set_fc_mode() to enable the port serdis send PFC packet periodly:
  
  ifg_handler_base::set_fc_mode(la_uint_t mac_lane_base_id,
                              size_t mac_lanes_reserved_count,
                              la_uint_t serdes_base_id,
                              la_mac_port::port_speed_e speed,
                              la_mac_port::fc_mode_e fc_mode)
{
    
    if (fc_mode == la_mac_port::fc_mode_e::PFC) {
        // Can be either enabled or disabled based on whether we are using HW PFC or SW PFC
        enable_periodic_send = m_pfc_pif_en_periodic_send_map[mac_lane_base_id];
    }

    la_status stat = set_fc_mode_periodic(mac_lane_base_id, mac_lanes_reserved_count, enable_periodic_send);  
    return_on_error(stat);

    stat = set_fc_mode_port(mac_lane_base_id, mac_lanes_reserved_count, serdes_base_id, speed, fc_mode);
    return_on_error(stat);
    ...
}


