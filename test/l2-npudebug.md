**>>> npu_sc.print_npe_counters_table()**  
```
>>>+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+---  
|          |s0-in|s0-out|s0-loop|s1-in|s1-out|s1-loop|s2-in|s2-out|s2-loop|s3-in|s3-out|s3-loop|s4-in|s4-out|s4-loop|s5-in|s5-out  
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------  
| NPU-Host |  0  |  0   |   0   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -  
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------  
|Term-NPE-0|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  45 |  45  |   45  |  0  |  0  
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------  
|Term-NPE-1|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  45 |  45  |   45  |  0  |  0  
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------  
|Term-NPE-2|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  45 |  45  |   45  |  0  |  0
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------  
|Fwd-NPE-0 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  44 |  44  |   44  |  0  |  0  
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------  
|Fwd-NPE-1 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  45 |  45  |   45  |  0  |  0  
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------  
|Fwd-NPE-2 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  45 |  45  |   45  |  0  |  0  
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------  
| Tx-NPE-0 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  67 |  67  |   0   |  0  |  0  
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------  
| Tx-NPE-1 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  67 |  67  |   0   |  0  |  0  
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------  
```
\>>> slice = 4  
\>>>stage = "termination"  
\>>>npu_sc.npe_stop_and_step_macro(enable=False, step=False, slice=slice, stage=stage, npe_index=0, print_note=True)  
\>>>0  
Slice[4].Stage['termination'].NPE[0] -> Enable Stop macro feature  
\>>>npu_sc.npe_stop_and_step_macro(enable=False, step=False, slice=slice, stage=stage, npe_index=0, print_note=True)  
\>>>1  

**>>>npu_sc.print_npe_counters_table()**  
```
>>>+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+---
|          |s0-in|s0-out|s0-loop|s1-in|s1-out|s1-loop|s2-in|s2-out|s2-loop|s3-in|s3-out|s3-loop|s4-in|s4-out|s4-loop|s5-in|s5-out
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------
| NPU-Host |  0  |  0   |   0   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------
|Term-NPE-0|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   | 1428| 1332 |  1332 |  0  |  0
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------
|Term-NPE-1|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   | 1544| 1544 |  1544 |  0  |  0
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------
|Term-NPE-2|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   | 1544| 1544 |  1544 |  0  |  0
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------
|Fwd-NPE-0 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   | 1474| 1474 |  1474 |  0  |  0
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------
|Fwd-NPE-1 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   | 1474| 1474 |  1474 |  0  |  0
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------
|Fwd-NPE-2 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   | 1473| 1473 |  1473 |  0  |  0
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------
| Tx-NPE-0 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   | 1998| 1998 |   0   |  0  |  0
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------
| Tx-NPE-1 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   | 1997| 1997 |   0   |  0  |  0
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------
```
**>>>npu_sc.rxpp_term_last_npe_macros(4,0)**  
```
>>>#### NOTES: 1) Max stack depth is 4. Head of the macros stack is entry=0. 2) This register is cleared once read. Since last re
  NPE-macros-stack[entry=0]: macro_id 0x5, i.e. 'network_rx_mac_af_and_termination_macro'
  NPE-macros-stack[entry=1]: macro_id 0x5, i.e. 'network_rx_mac_af_and_termination_macro'
  NPE-macros-stack[entry=2]: macro_id 0x5, i.e. 'network_rx_mac_af_and_termination_macro'
  NPE-macros-stack[entry=3]: macro_id 0x5, i.e. 'network_rx_mac_af_and_termination_macro'
```
**>>> npu_sc.rxpp_term_last_npe_macros(4,0)**  
```
>>>#### NOTES: 1) Max stack depth is 4. Head of the macros stack is entry=0. 2) This register is cleared once read. Since last re
  NPE-macros-stack is empty/cleared
```
**>>>npu_sc.npe_stop_and_step_macro(enable=True, step=True, slice=slice, stage=stage, npe_index=0, print_note=True)**  
```
>>>1
Slice[4].Stage['termination'].NPE[0] -> Stepping single macro

**>>>npu_sc.npe_stop_and_step_macro(enable=True, step=True, slice=slice, stage=stage, npe_index=0, print_note=True)**  

>>>1
Slice[4].Stage['termination'].NPE[0] -> Stepping single macro
```
**>>>npu_sc.get_npe_lookups_and_results(stage="termination", slice=4, npe_index=0, print_note=True)**  
```
>>>|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Key Bucket |                  Key Type                  |      Key Value      | Result Bucket |                 Result Type                 |                Result Value                |
|==========================================================================================================================================================================================|
|     a      | npl_service_mapping_compound_table_key_opt | 0x1040000019000253c |       d       | npl_l2_relay_and_l3_lp_attributes_payload_t |                0xe100001000                |
|            | ion_service_mapping_selector_ac_port_tag_t |                     |               |                                             |                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     a      | npl_service_mapping_compound_table_key_opt | 0x1040000019000253c |       a       |           npl_mac_lp_attributes_t           | 0x2000000000800007efff08000d682bc7ffff0000 |
|            | ion_service_mapping_selector_ac_port_tag_t |                     |               |                                             |                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     a      | npl_service_mapping_compound_table_key_opt | 0x1040000019000253c |       b       |         npl_base_l3_lp_attr_union_t         |                    0x0                     |
|            | ion_service_mapping_selector_ac_port_tag_t |                     |               |                                             |                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

For elaboration of keys/results:
     npu_sc.print_parsed_npe_key(<stage>, <slice>, <npe index>, <bucket a/b/c/d>)
     npu_sc.print_parsed_npe_result(<stage>, <slice>, <npe index>, <bucket a/b/c/d>)
Examples:
     npu_sc.print_parsed_npe_key("termination", 4, 0, "a")
     npu_sc.print_parsed_npe_result("termination", 4, 0, "d")
```
**>>>npu_sc.print_parsed_npe_key("termination", 4, 0, "a")**  
```
>>>Key type: npl_service_mapping_compound_table_key_option_service_mapping_selector_ac_port_tag_t, Value: 0x1040000019000253c
  const1_4b1100_exact_0xc: 0xc
  const2_18d0_exact_0x0: 0x0
  mac_af_local_vars_mac_termination_logical_db: 0x0
  parsing mac_af_local_vars_outer_vlan_tag_vid:
    id: 0x64
  mac_af_local_vars_service_mapping_logical_db: 0x4
  parsing mac_relay_local_vars_mac_da_compound_termination_control:
    append_relay: 0x1
    attempt_termination: 0x1
  mac_relay_local_vars_mac_da_prefix: 0x1
  packet_ethernet_header_da_32_0_: 0x2
  parsing pd_layer_vars_local_slp_id:
    id: 0x9

For elaboration of keys/results:
     npu_sc.print_parsed_npe_key(<stage>, <slice>, <npe index>, <bucket a/b/c/d>)
     npu_sc.print_parsed_npe_result(<stage>, <slice>, <npe index>, <bucket a/b/c/d>)
Examples:
     npu_sc.print_parsed_npe_key("termination", 4, 0, "a")
     npu_sc.print_parsed_npe_result("termination", 4, 0, "d")
 npu_sc.print_parsed_npe_key("termination", 4, 0, "a")

>>>npu_sc.print_parsed_npe_key("termination", 4, 0, "a")
>>>Key type: npl_rx_obm_encap_msb_pack_table_key_option_obm_inject_down_t, Value: 0x253c
  const1_20d0_exact_0x0: 0x253c
  const2_5d0_exact_0x0: 0x0
  const3_INJECT_DOWN_ENCAP_TYPE_TO_DMA_exact_0x7: 0x0
>>>npu_sc.print_parsed_npe_result("termination", 4, 0, "d")
>>>result in bucket d is None

>>>npu_sc.print_parsed_npe_result("termination", 4, 0, "b")
>>>result in bucket b is None

>>>npu_sc.print_parsed_npe_result("termination", 4, 0, "a")
>>>Result type: npl_rx_map_pif_ifg_to_init_data_table_payloads_t, Value: 0x464001411000400
  parsing write_init_data_for_pif_ifg:
    parsing init_data:
      parsing init_data:
        initial_npp_attributes_index: 0x0
        initial_slice_id: 0x0
      initial_is_rcy_if: 0x1
      initial_lp_type: 0x1
      initial_mac_lp_type: 0x0
      initial_mapping_type: 0x1
      initial_vlan_profile: 0x1
      issu_placeholder: 0x0
      parsing mapping_key:
        parsing initial_lp_id:
          id: 0x4
        mpls_label_placeholder: 0x40
      pfc_enable: 0x0
    parsing slice_and_source_if:
      slice_id_on_npu: 0x4
      parsing source_if_on_npu:
        ifg: 0x0
        pif: 0x19
```
**>>>npu_sc.rxpp_term_last_npe_in_nppd(4,0)**  
```
>>>field 'pin2scp_pd' value is 0x1000cccccccb0c53c0686008100019071020e01ede2000364801e00000020000000028e0000000000000000000001000404000000000000000000000000000000000000000000000000000000000000000000000000002800000000007f80000000000000000000000000000000000000

>>>npu_sc.rxpp_term_last_npe_in_nppd(4,0)
>>>field 'pin2scp_pd' value is 0x1000cccccccb0c53c0686008100019071020e01ede2000364801e00000020000000028e0000000000000000000001000404000000000000000000000000000000000000000000000000000000000000000000000000002800000000007f80000000000000000000000000000000000000
```
**>>>npu_sc.txpp_last_npe_in_nppd(4,0)**  
```
>>>field 'pin2scp_pd' value is 0xc0000028e0000000000000000004000000000000000000000000000092a00036401000cccccccb0c53c06860081000190000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000064408080100000c0092000000000000100

>>>npu_sc.txpp_last_npe_in_nppd(4,0)
>>>field 'pin2scp_pd' value is 0xc0000028e0000000000000000004000000000000000000000000000092a00036401000cccccccb0c53c06860081000190000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000064408080100000c0092000000000000100
```
```
>>> la_device
>>><leaba.sdk.la_device; proxy of <Swig Object of type 'silicon_one::la_device *' at 0x7f24205c0e40> >
>>> tables =la_device.get_device_tables()
>>>
>>>tables
>>><nplapi_device_tables.device_tables; proxy of <Swig Object of type 'silicon_one::device_tables *' at 0x7f239a24e690> >
>>> dir(tables)
>>>['__class__', '__del__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattr__', '___', '__sizeof__', '__str__', '__subclasshook__', '__swig_destroy__', '__swig_getmethods__', '__swig_setmethods__', '__weakref__',runing_static_table', 'aci_overlay_ipv4_sip_table', 'aci_overlay_ipv4_sip_tcam_table', 'aci_rx_src_label_static_table', 'aci_sclaer_type_to_protocol_number_table', 'active_ftag_table', 'additional_labels_table', 'all_reachable_vector', 'bfd_desired_tx_intervt_header_static_table', 'bfd_inject_ttl_static_table', 'bfd_ipv6_sip_A_table', 'bfd_ipv6_sip_B_table', 'bfd_ipv6_sip_C_table', 'btic_table', 'bfd_udp_port_static_table', 'bitmap_oqg_map_table', 'bvn_flow_offset_table', 'bvn_tc_map_table', 'calc_checksum_enab_macro', 'compressed_egress_ipv6_acl_sec_table', 'cong_level_ecn_remap_map_table', 'counters_block_config_table', 'counters_voq_b_vlan_membership_table_lu_d_res_d', 'db_access_per_port_destination_table', 'db_access_transmit_per_dest_port_npu_host_macro_stam, 'dlp0_key_lsb_mapping_table', 'dlp1_key_lsb_mapping_table', 'dot1x_actions_table', 'dram_cgm_cgm_deq_lut_table', 'dram_cgm_cgm_ibutes_table', 'dummy_dip_index_table', 'ecn_remark_static_table', 'egress_acl_conf_set_table', 'egress_mac_ipv4_sec_acl_table', e_ipv6_src_ip_table', 'ene_macro_code_tpid_profile_static_table', 'ene_rewrite_punt_sa_prefix_index_table', 'ene_srv6_sid_block_t_mp_table', 'eth_mep_not_ccm_up_em_mp_table', 'eth_meter_profile_mapping_table', 'eth_oam_set_da_mc2_static_table', 'eth_oam_set__drop_mapping_hw_table', 'eve_drop_vlan_id_hw_table', 'eve_interrupt_mapping_hw_table', 'eve_to_ethernet_ene_static_table', 'evenders_type_table', 'fabric_init_cfg', 'fabric_npuh_size_calculation_static_table', 'fabric_out_color_map_table', 'fabric_rx_fwd_ertination_table', 'fabric_scaled_mc_map_to_netork_slice_static_table', 'fabric_smcid_threshold_table', 'fabric_term_error_checker_table', 'fec_table', 'fec_type_decoding_table', 'fi_core_tcam_table', 'fi_macro_config_table', 'filb_voq_mapping', 'first_ene_statable', 'flc_map_header_type_mask_l_table', 'flc_map_header_type_mask_m_table', 'flc_map_header_type_mask_s_table', 'flc_q_range_t_table', 'fwd_and_encap_types_to_field_b_offset_table', 'fwd_bucket_a_lu_data_selector', 'fwd_bucket_b_lu_data_selector', 'fwd_bget_device_id', 'get_ecm_meter_ptr_table', 'get_ingress_ptp_info_and_is_slp_dm_static_table', 'get_l2_rtf_conf_set_and_init_stagea_table', 'ibm_uc_cmd_to_encap_data_table', 'ifgb_tc_lut_table', 'increment_egress_acl_step_static_table', 'increment_rtf_step_stss_rtf_ipv4_db1_160_f1_table', 'ingress_rtf_ipv4_db1_320_f0_table', 'ingress_rtf_ipv4_db2_160_f0_table', 'ingress_rtf_ipv4_db2_16 'ingress_rtf_ipv4_db4_160_f0_table', 'ingress_rtf_ipv4_db4_160_f1_table', 'ingress_rtf_ipv4_db4_320_f0_table', 'ingress_rtf_ipv6table', 'ingress_rtf_ipv6_db2_320_f0_table', 'ingress_rtf_ipv6_db3_160_f0_table', 'ingress_rtf_ipv6_db3_160_f1_table', 'ingress_rcontrol_hw_table', 'inject_down_select_ene_static_table', 'inject_down_tx_redirect_counter_table', 'inject_mact_ldb_to_output_lr'e', 'ip_fwd_macro_set_fwd_header_static_table', 'ip_inactivity_check_table', 'ip_ingress_cmp_mcid_static_table', 'ip_mc_local_inj'ip_proto_type_mux_static_table', 'ip_relay_to_vni_table', 'ip_rtf_macro_is_skip_rtf_processing_table', 'ip_rx_global_counter_tab', 'ip_uc_and_acl_set_ethertype_static_table', 'ip_uc_first_macro_select_vid2_static_table', 'ip_uc_next_macro_static_table', 'ip_termination_dip_index_tt0_table', 'ipv4_ip_tunnel_termination_dip_tt0_table', 'ipv4_ip_tunnel_termination_sip_dip_index_tt0_tablet_mapping_table', 'ipv4_sgt_em_table', 'ipv4_sgt_lpm_table', 'ipv4_vrf_dip_em_table', 'ipv4_vrf_s_g_table', 'ipv6_acl_sport_stats_static_table', 'ipv6_lpm_table', 'ipv6_lpts_table', 'ipv6_og_pcl_em_table', 'ipv6_og_pcl_lpm_table', 'ipv6_pt_get_interface', 'le', 'ipv6_sip_compression_table', 'ipv6_sip_egress_og_code_table', 'ipv6_tunnel_termination_dip_index_table', 'ipv6_tunnel_termi', 'is_mca_ipv6_routable_static_table', 'issu_enabled_table', 'issu_properties_table', 'l2_dlp_table', 'l2_lp_profile_filter_tablble', 'l2_lpts_skip_p2p_static_table', 'l2_termination_next_macro_static_table', 'l2_tunnel_term_next_macro_static_table', 'l3_dll3_tunnel_termination_next_macro_static_table', 'l3_vxlan_ipv6_overlay_da_table', 'l3_vxlan_ipv6_overlay_sa_table', 'l3_vxlan_ovee', 'large_encap_te_he_tunnel_id_table', 'ldpote_mode_table', 'learn_manager_cfg_max_learn_type_reg', 'light_fi_fabric_table', 'ls_cfg_table', 'light_fi_tm_table', 'link_relay_attributes_table', 'link_relay_id_static_table', 'link_up_vector', 'local_mc_fwd_nwrite_ptr_reg', 'lr_write_ptr_reg', 'mac_ac_and_acl_set_cntr_0_offset_and_comp_static_table', 'mac_af_npp_attributes_table', 'macac_mc_tcam_termination_attributes_table', 'mac_qos_mapping_table', 'mac_relay_g_ipv4_table', 'mac_relay_g_ipv6_table', 'mac_relay_da_em_table', 'mac_termination_tcam_table', 'map_ene_subcode_to8bit_static_table', 'map_inject_ccm_macro_static_table', 'map_pune', 'map_tx_punt_next_macro_static_table', 'map_tx_punt_rcy_next_macro_static_table', 'mc_bitmap_base_voq_lookup_table', 'mc_bitmmc_slice_bitmap_table', 'meg_id_format_static_table', 'mep_address_prefix_table', 'mii_loopback_table', 'mirror_code_2_hw_table',e', 'mpls_control_static_table', 'mpls_encap_control_static_table', 'mpls_forwarding_table', 'mpls_fwd_macro_set_fwd_header_statitable', 'mpls_qos_mapping_table', 'mpls_resolve_service_labels_static_table', 'mpls_rx_term_next_macro_static_table', 'mpls_termible', 'nh_macro_code_to_id_l6_sram_static_table', 'nh_macro_code_to_id_l6_static_table', 'nhlfe_type_mapping_static_table', 'npp_, 'oamp_drop_destination_static_table', 'oamp_redirect_get_counter_table', 'oamp_redirect_punt_eth_hdr_1_table', 'oamp_redirect_p_macro_static_table', 'outer_ip_ecn_static_table', 'outer_tpid_table', 'overlay_ipv4_sip_table', 'pad_mtu_inj_check_static_table''pdvoq_slice_voq_properties_table', 'per_asbr_and_dpe_table', 'per_pe_and_prefix_vpn_key_large_table', 'per_pe_and_vrf_vpn_key_laounter_offset_from_vector_table', 'pfc_ssp_em_mp_table', 'pin_start_offset_macros', 'pma_loopback_table', 'post_fwd_rtf_next_macrta_static_table', 'punt_ethertype_static_table', 'punt_rcy_inject_header_ene_encap_table', 'punt_select_nw_ene_static_table', 'puable2', 'pwe_label_table', 'pwe_to_l3_dest_table', 'pwe_vpls_label_table', 'pwe_vpls_tunnel_label_table', 're_enter_egress_acl_matadata_table', 'redirect_destination_table', 'redirect_enable_exception_rtf_table', 'redirect_rtf_is_enabled_table', 'redirect_rx_next_protocol_bitmap_static_table', 'resolution_set_next_macro_table', 'rewrite_sa_prefix_index_table', 'rmep_last_time_table',  'rtf_conf_set_to_og_pcl_ids_mapping_table', 'rtf_conf_set_to_post_fwd_params_mapping_table', 'rtf_macro_set_fwd_header_type_statolve_sec_action_static_table', 'rtf_vlan_valid_static_table', 'rx_counters_bank_id_map_config', 'rx_counters_block_config_table',ank_offset_map', 'rx_meter_block_meter_attribute_table', 'rx_meter_block_meter_profile_table', 'rx_meter_block_meter_shaper_confier_configuration_table', 'rx_meter_meters_attribute_table', 'rx_meter_rate_limiter_shaper_configuration_table', 'rx_meter_stat_me_static_table', 'rx_redirect_next_macro_static_table', 'rx_term_error_handling_counter_table', 'rx_term_error_handling_destinatio_macro_static_table', 'select_mac_forwarding_static_table', 'service_counters_rx_table', 'service_counters_tx_table', 'service_lpmapping_em0_ac_port_table', 'service_mapping_em0_ac_port_tag_table', 'service_mapping_em0_ac_port_tag_tag_table', 'service_mappintcam_ac_port_tag_tag_table', 'service_mapping_tcam_key_lsb_mapping_table', 'service_mapping_tcam_pwe_tag_table', 'service_relay_abank_table', 'sgacl_ip_fragment_check_table', 'sgacl_l4_protocol_select_table', 'sgacl_next_macro_static_table', 'sgacl_table', 'all_em_key_lsb_mapping_table', 'small_encap_mpls_he_asbr_table', 'small_encap_mpls_he_te_table', 'snoop_code_hw_table', 'snoop_tasr_pm_em_mp_table', 'sr_pm_event_queue_table', 'sr_pm_udp_port_static_table', 'srh_next_header_dscp_static_table', 'srv6_deep_ter6_next_header_check_static_table', 'srv6_per_pe_and_prefix_vpn_key_large_table', 'srv6_pre_edit_command_static_table', 'srv6_sid_ble', 'srv6_tunnel_termination_usid_tt1_table', 'stage0_assoc_data_table', 'stage0_em_table', 'stage0_group_size_table', 'stage0_e_decoding_table', 'stage2_assoc_data_table', 'stage2_em_table', 'stage2_group_size_table', 'stage2_protection_table', 'stage2_tywn_mac_destination_table', 'svl_dspa_or_packet_trace_table', 'svl_is_dsp_remote_or_packet_trace', 'svl_mirror_cmd_remote_dsp_tableadend_lsp_counter_offset_table', 'term_bucket_a_lu_data_selector', 'term_bucket_b_lu_data_selector', 'term_bucket_c_lu_data_sele_ibm_cmd_to_destination', 'transmit_bucket_a_lu_data_selector', 'transmit_bucket_b_lu_data_selector', 'transmit_bucket_c_lu_data_6_sip_qualify_acl_table', 'tunnel_qos_static_table', 'tunnel_udp_port_static_table', 'tx_counters_bank_id_map_config', 'tx_counteect_bytes_to_be_removed_static_table', 'tx_redirect_code_table', 'tx_redirect_per_pif_cntr_offset_table', 'tx_redirect_per_proto_', 'txpp_em_dlp_profile_mapping_table', 'txpp_encap_qos_mapping_table', 'txpp_first_enc_type_to_second_enc_type_offset', 'txpp_fwit_tpid1_profile_hw_table', 'vlan_edit_tpid2_profile_hw_table', 'vlan_format_table', 'vni_table', 'voq_cgm_slice_buffers_consumpt_probability_selector_table', 'voq_cgm_slice_evicted_buffers_consumption_lut_for_enq_table', 'voq_cgm_slice_eviction_ok_lut_for_e'voq_cgm_slice_profile_buff_region_thresholds_table', 'voq_cgm_slice_profile_pkt_enq_time_region_thresholds_table', 'voq_cgm_slicrt_table']
>>> tables.service_mapping_em0_ac_port_table
>>>[<nplapi_tables.npl_service_mapping_em0_ac_port_table_t; proxy of <Swig Object of type 'std::shared_ptr< silicon_one::npl_tablroxy of <Swig Object of type 'std::shared_ptr< silicon_one::npl_table< silicon_one::npl_service_mapping_em0_ac_port_table_functiopl_table< silicon_one::npl_service_mapping_em0_ac_port_table_functional_traits_t > > *' at 0x7f239a24e7b0> >]
```
```
>>>for k,v in t2.entries(0):
>>>...  key = k
>>>...  val = v
>>>...  print("key", key)
>>>...  print("val", val)
>>>...
>>>key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_t
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta

>>>t2=tables.service_mapping_em0_ac_port_table[1]
>>>len(t2.entries(0))
>>>11

>>>for k,v in t2.entries(0):
>>>...   key = k
>>>...   val = v
>>>...   print("key", key)
>>>...   print("val", val)
>>>...
>>>key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_t
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
key <nplapi_base.npl_service_mapping_em0_ac_port_table_key_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_tabl
val <nplapi_base.npl_service_mapping_em0_ac_port_table_value_t; proxy of <Swig Object of type 'npl_service_mapping_em0_ac_port_ta
```

```
t0 = tables.service_mapping_em0_ac_port_table[0]
for index in range(t0.size()):
    print('index', index)
    for k,v in t0.entries(index):
        key = k
        val = v
        print("key.local_slp_id.id", key.local_slp_id.id, "value.action", val.action, "value.payloads.lp_id", val.payloads.write.lp_id.id, "value.payloads.relay_id",val.payloads.write.relay_id.id)
   
>>>key.local_slp_id.id 27 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 28 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 29 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 30 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
key.local_slp_id.id 31 value.action 0 value.payloads.lp_id 13 value.payloads.relay_id 0
key.local_slp_id.id 32 value.action 0 value.payloads.lp_id 15 value.payloads.relay_id 0
key.local_slp_id.id 34 value.action 0 value.payloads.lp_id 17 value.payloads.relay_id 0
key.local_slp_id.id 35 value.action 0 value.payloads.lp_id 19 value.payloads.relay_id 0
key.local_slp_id.id 36 value.action 0 value.payloads.lp_id 21 value.payloads.relay_id 0
key.local_slp_id.id 37 value.action 0 value.payloads.lp_id 23 value.payloads.relay_id 0
key.local_slp_id.id 38 value.action 0 value.payloads.lp_id 25 value.payloads.relay_id 0
key.local_slp_id.id 27 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 27 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 28 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 27 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 28 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 29 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 27 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 28 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 29 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 30 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
key.local_slp_id.id 27 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 28 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 29 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 30 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
key.local_slp_id.id 31 value.action 0 value.payloads.lp_id 13 value.payloads.relay_id 0
key.local_slp_id.id 27 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 28 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 29 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 30 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
key.local_slp_id.id 31 value.action 0 value.payloads.lp_id 13 value.payloads.relay_id 0
key.local_slp_id.id 32 value.action 0 value.payloads.lp_id 15 value.payloads.relay_id 0
key.local_slp_id.id 27 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 28 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 29 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 30 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
key.local_slp_id.id 31 value.action 0 value.payloads.lp_id 13 value.payloads.relay_id 0
key.local_slp_id.id 32 value.action 0 value.payloads.lp_id 15 value.payloads.relay_id 0
key.local_slp_id.id 34 value.action 0 value.payloads.lp_id 17 value.payloads.relay_id 0
key.local_slp_id.id 27 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 28 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 29 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 30 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
key.local_slp_id.id 31 value.action 0 value.payloads.lp_id 13 value.payloads.relay_id 0
key.local_slp_id.id 32 value.action 0 value.payloads.lp_id 15 value.payloads.relay_id 0
key.local_slp_id.id 34 value.action 0 value.payloads.lp_id 17 value.payloads.relay_id 0
key.local_slp_id.id 35 value.action 0 value.payloads.lp_id 19 value.payloads.relay_id 0
key.local_slp_id.id 27 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 28 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 29 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 30 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
key.local_slp_id.id 31 value.action 0 value.payloads.lp_id 13 value.payloads.relay_id 0
key.local_slp_id.id 32 value.action 0 value.payloads.lp_id 15 value.payloads.relay_id 0
key.local_slp_id.id 34 value.action 0 value.payloads.lp_id 17 value.payloads.relay_id 0
key.local_slp_id.id 35 value.action 0 value.payloads.lp_id 19 value.payloads.relay_id 0
key.local_slp_id.id 36 value.action 0 value.payloads.lp_id 21 value.payloads.relay_id 0
key.local_slp_id.id 27 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 28 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 29 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 30 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
key.local_slp_id.id 31 value.action 0 value.payloads.lp_id 13 value.payloads.relay_id 0
key.local_slp_id.id 32 value.action 0 value.payloads.lp_id 15 value.payloads.relay_id 0
key.local_slp_id.id 34 value.action 0 value.payloads.lp_id 17 value.payloads.relay_id 0
key.local_slp_id.id 35 value.action 0 value.payloads.lp_id 19 value.payloads.relay_id 0
key.local_slp_id.id 36 value.action 0 value.payloads.lp_id 21 value.payloads.relay_id 0
key.local_slp_id.id 37 value.action 0 value.payloads.lp_id 23 value.payloads.relay_id 0

for k,v in t0.entries(1):
   key = k
   val = v
   print("key.local_slp_id.id", key.local_slp_id.id, "value.action", val.action, "value.payloads.lp_id", val.payloads.write.lp_id.id, "value.payloads.relay_id",val.payloads.write.relay_id.id)

>>>key.local_slp_id.id 27 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0

>>>index 0
key.local_slp_id.id 6 value.action 0 value.payloads.lp_id 1 value.payloads.relay_id 128
key.local_slp_id.id 11 value.action 0 value.payloads.lp_id 3 value.payloads.relay_id 0
key.local_slp_id.id 19 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 20 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 21 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 22 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
key.local_slp_id.id 23 value.action 0 value.payloads.lp_id 13 value.payloads.relay_id 0
key.local_slp_id.id 24 value.action 0 value.payloads.lp_id 15 value.payloads.relay_id 0
key.local_slp_id.id 25 value.action 0 value.payloads.lp_id 17 value.payloads.relay_id 0
key.local_slp_id.id 26 value.action 0 value.payloads.lp_id 19 value.payloads.relay_id 0
key.local_slp_id.id 33 value.action 0 value.payloads.lp_id 21 value.payloads.relay_id 0
index 1
key.local_slp_id.id 6 value.action 0 value.payloads.lp_id 1 value.payloads.relay_id 128
index 2
key.local_slp_id.id 6 value.action 0 value.payloads.lp_id 1 value.payloads.relay_id 128
key.local_slp_id.id 11 value.action 0 value.payloads.lp_id 3 value.payloads.relay_id 0
index 3
key.local_slp_id.id 6 value.action 0 value.payloads.lp_id 1 value.payloads.relay_id 128
key.local_slp_id.id 11 value.action 0 value.payloads.lp_id 3 value.payloads.relay_id 0
key.local_slp_id.id 19 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
index 4
key.local_slp_id.id 6 value.action 0 value.payloads.lp_id 1 value.payloads.relay_id 128
key.local_slp_id.id 11 value.action 0 value.payloads.lp_id 3 value.payloads.relay_id 0
key.local_slp_id.id 19 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 20 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
index 5
key.local_slp_id.id 6 value.action 0 value.payloads.lp_id 1 value.payloads.relay_id 128
key.local_slp_id.id 11 value.action 0 value.payloads.lp_id 3 value.payloads.relay_id 0
key.local_slp_id.id 19 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 20 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 21 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
index 6
key.local_slp_id.id 6 value.action 0 value.payloads.lp_id 1 value.payloads.relay_id 128
key.local_slp_id.id 11 value.action 0 value.payloads.lp_id 3 value.payloads.relay_id 0
key.local_slp_id.id 19 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 20 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 21 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 22 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
index 7
key.local_slp_id.id 6 value.action 0 value.payloads.lp_id 1 value.payloads.relay_id 128
key.local_slp_id.id 11 value.action 0 value.payloads.lp_id 3 value.payloads.relay_id 0
key.local_slp_id.id 19 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 20 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 21 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 22 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
key.local_slp_id.id 23 value.action 0 value.payloads.lp_id 13 value.payloads.relay_id 0
index 8
key.local_slp_id.id 6 value.action 0 value.payloads.lp_id 1 value.payloads.relay_id 128
key.local_slp_id.id 11 value.action 0 value.payloads.lp_id 3 value.payloads.relay_id 0
key.local_slp_id.id 19 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 20 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 21 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 22 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
key.local_slp_id.id 23 value.action 0 value.payloads.lp_id 13 value.payloads.relay_id 0
key.local_slp_id.id 24 value.action 0 value.payloads.lp_id 15 value.payloads.relay_id 0
index 9
key.local_slp_id.id 6 value.action 0 value.payloads.lp_id 1 value.payloads.relay_id 128
key.local_slp_id.id 11 value.action 0 value.payloads.lp_id 3 value.payloads.relay_id 0
key.local_slp_id.id 19 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 20 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 21 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 22 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
key.local_slp_id.id 23 value.action 0 value.payloads.lp_id 13 value.payloads.relay_id 0
key.local_slp_id.id 24 value.action 0 value.payloads.lp_id 15 value.payloads.relay_id 0
key.local_slp_id.id 25 value.action 0 value.payloads.lp_id 17 value.payloads.relay_id 0
index 10
key.local_slp_id.id 6 value.action 0 value.payloads.lp_id 1 value.payloads.relay_id 128
key.local_slp_id.id 11 value.action 0 value.payloads.lp_id 3 value.payloads.relay_id 0
key.local_slp_id.id 19 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 20 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 21 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 22 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
key.local_slp_id.id 23 value.action 0 value.payloads.lp_id 13 value.payloads.relay_id 0
key.local_slp_id.id 24 value.action 0 value.payloads.lp_id 15 value.payloads.relay_id 0
key.local_slp_id.id 25 value.action 0 value.payloads.lp_id 17 value.payloads.relay_id 0
key.local_slp_id.id 26 value.action 0 value.payloads.lp_id 19 value.payloads.relay_id 0
```
```
>>>t0 = tables.service_mapping_em0_ac_port_table[2]
>>>for index in range(t0.size()):
>>>    print('index', index)
>>>    for k,v in t0.entries(index):
>>>        key = k
>>>        val = v
>>>        print("key.local_slp_id.id", key.local_slp_id.id, "value.action", val.action, "value.payloads.lp_id", val.payloads.write.lp_id.id, "value.payloads.relay_id",val.payloads.write.relay_id.id)... ... ... ... ...
>>>...

>>>index 0
key.local_slp_id.id 7 value.action 0 value.payloads.lp_id 1 value.payloads.relay_id 0
key.local_slp_id.id 8 value.action 0 value.payloads.lp_id 3 value.payloads.relay_id 0
key.local_slp_id.id 9 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
key.local_slp_id.id 10 value.action 0 value.payloads.lp_id 7 value.payloads.relay_id 0
key.local_slp_id.id 12 value.action 0 value.payloads.lp_id 9 value.payloads.relay_id 0
key.local_slp_id.id 13 value.action 0 value.payloads.lp_id 11 value.payloads.relay_id 0
key.local_slp_id.id 14 value.action 0 value.payloads.lp_id 13 value.payloads.relay_id 0
key.local_slp_id.id 15 value.action 0 value.payloads.lp_id 15 value.payloads.relay_id 0
key.local_slp_id.id 16 value.action 0 value.payloads.lp_id 17 value.payloads.relay_id 0
key.local_slp_id.id 17 value.action 0 value.payloads.lp_id 19 value.payloads.relay_id 0
key.local_slp_id.id 18 value.action 0 value.payloads.lp_id 21 value.payloads.relay_id 0
index 1
key.local_slp_id.id 7 value.action 0 value.payloads.lp_id 1 value.payloads.relay_id 0
index 2
key.local_slp_id.id 7 value.action 0 value.payloads.lp_id 1 value.payloads.relay_id 0
key.local_slp_id.id 8 value.action 0 value.payloads.lp_id 3 value.payloads.relay_id 0
......
```
Notice:   
   key.local_slp_id.id 9 value.action 0 value.payloads.lp_id 5 value.payloads.relay_id 0
this entry match the 

   
   
