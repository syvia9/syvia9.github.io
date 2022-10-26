# big_share 环境：
## 1. 修改validation的导入文件leaba_val.py:  

sed -i 's/import debug_utils as hld_debug_utils/import leaba\.debug_tools\.debug_utils as hld_debug_utils/g' /big_share2/pacific/user/yaliuliu/valid/validation-gibraltar-1.54.0.ph2ea4.3/leaba_val.py

## 2. connect device sshpass -p leaba ssh root@10.56.19.108    
## 3. goto SDK path and set environment:
   cd /big_share2/pacific/user/yaliuliu/sdkmas  
   source siliconone_kmodule.sh  
   source test_env.sh  

## 4. modify a sdk file, use pdb to interrupt the code:  
    def _test_route_single_fec(self, disable_rx=False, disable_tx=False):  
        prefix = self.ip_impl.build_prefix(self.DIP, length=16)  

        self.ip_impl.add_route(self.topology.vrf, prefix,  
                               self.l3_port_impl.reg_fec,  
                               ip_routing_base.PRIVATE_DATA)  
        import pdb
        pdb.set_trace()

##  5.run the sdk test:
    validation import command:
    import sys  
    import os  
    sys.LEABA_SDK_PATH = os.getenv('LEABA_SDK_PATH', '')  
    from leaba_val import *  
    import npu_scripts  
    from npu_scripts import *  
    set_dev(self.device)  
    from leaba_val import *   
    npu_sc  
    
    
     /common/pkgs/python/3.6.10/bin/python3 driver/gibraltar/shared/test/api/ip_routing/test_ipv4_l3_ac_routing.py -v test_ipv4_l3_ac_routing.test_destroy_route
     
    then we will stop at the  pdb.set_trace():
    ----------------------------------------------log---------------------------------------------------------------
[root@localhost /big_share2/pacific/user/yaliuliu/sdkmas]# /common/pkgs/python/3.6.10/bin/python3 driver/gibraltar/shared/test/api/ip_routing/test_ipv4_l3_ac_routing.py -v test_ipv4_l3_ac_routing.test_destroy_route  
WARNING: No route found for IPv6 destination :: (no default route?). This affects only IPv6  
WARNING: Mac address to reach destination not found. Using broadcast.  
WARNING: Mac address to reach destination not found. Using broadcast.  
WARNING: more Mac address to reach destination not found. Using broadcast.  
-I-LLD-1- initialize: device revision=GIBRALTAR_A1  
-I-LLD-1- Using regular LLD implementation, all blocks are enabled by default  
-I-INTERRUPT-1- Loading interrupt tree from /big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/out/opt3-debug/res/gibraltar_interrupt_tree.json: nodes 0, unique 0, registers 0, bits 0  
-I-INTERRUPT-1- Loaded interrupt tree from /big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/out/opt3-debug/res/gibraltar_interrupt_tree.json: nodes 2686, unique 2686, registers 4508, bits 14573  
-I-HLD-1- GB submodel type from eFuse value: GB  
-I-LLD-1- get_core_reset: 0x3ffe1 is_reset = 0  
Setting POLL_MSI=False  
-I-HLD-1- initialize_phase_device: Before init_config_memories dvoq->init_active val: 0xd  
-I-HLD-1- initialize_phase_device: After init_config_memories dvoq->init_active val: 0xd  
-I-HLD-1- FINISHED POST SOFT RESET INIT  
test_destroy_route (__main__.test_ipv4_l3_ac_routing) ... -I-TABLES-1- LPM rebalance triggered.  
> /big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/shared/test/api/ip_routing/ip_routing_base.py(1658)_test_route_single_fec()  
-> U.run_and_compare(self, self.device,  
(Pdb)  
(Pdb) -I-TABLES-1- LPM rebalance triggered.  
-I-MAC_PORT-1- mac_port la_mac_port_base(oid=277)#SerDes 1/1/0# changed state to UP  
-I-MAC_PORT-1- mac_port la_mac_port_base(oid=293)#SerDes 2/1/0# changed state to UP  
-I-MAC_PORT-1- mac_port la_mac_port_base(oid=261)#SerDes 5/0/0# changed state to UP  
-I-MAC_PORT-1- mac_port la_mac_port_base(oid=245)#SerDes 5/1/2# changed state to UP  
-I-MAC_PORT-1- mac_port la_mac_port_base(oid=325)#SerDes 1/1/2# changed state to UP  
-I-MAC_PORT-1- mac_port la_mac_port_base(oid=341)#SerDes 2/1/2# changed state to UP  
-I-MAC_PORT-1- mac_port la_mac_port_base(oid=309)#SerDes 3/1/0# changed state to UP  
-I-MAC_PORT-1- mac_port la_mac_port_base(oid=357)#SerDes 3/1/2# changed state to UP  

## 6.check if la_device is created successfully:  
(Pdb) dir(self.device)  
['ETH_P_ALL', 'POLL_MSI', '__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattr__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', 'calc_num_oq_per_ifg', 'cfg_file_path', 'clear_counters', 'clear_device', 'clear_mc_voqs_cgm_profile', 'clear_routes', 'clear_snoops', 'clear_traps', 'close_sockets', 'destroy', 'device', 'device_family', 'device_path', 'device_revision', 'filter_teardown_list', 'flush', 'get_ethernet_port', 'get_ethernet_port_from_serdes', 'get_inject_packet', 'get_issu_val', 'get_oq_num', 'get_packet', 'get_packets', 'get_pci_serdes', 'get_pci_serdes_for_inject', 'get_snoops_configuraton', 'get_traps_configuraton', 'get_wrapper_headers_len', 'init', 'init_matilda_model', 'inject_db_trigger', 'inject_packet', 'inject_to_rcy_slice', 'll_device', 'm_ll_device', 'matilda_model', 'num_serdes_per_ifg', 'open_sockets', 'pacific_b1_hw_padding_compensation', 'pci_port_interface_index_to_network_interface_name', 'punt_egress_packets', 'rcy_to_inject_slice', 'restore_traps_configuration', 'save_traps_configuration', 'set_matilda_model_frequency', 'set_voqs_to_dropping_state', 'sockets', 'sockets_opened', 'step_learn_notify_packet', 'step_packet', 'step_packet_wait_time', 'strip_std_inject_header', 'system_learn_trigger', 'tearDown', 'tearDownAll', 'tearDownObjects', 'teardown_object', 'warm_boot_disconnected']  

## 7.import validation file:  

(Pdb) import sys  
(Pdb) import os    
(Pdb) sys.LEABA_SDK_PATH = os.getenv('LEABA_SDK_PATH', '')  
(Pdb) from leaba_val import *  
INFO  ============================================================
INFO  ============================================================
INFO  ================= GIBRALTAR VALIDATION LOG =================
INFO  ==================based on 1.54.0.ph2ea4.3==================
INFO  ============================================================
INFO  ============================================================  

(Pdb)  
(Pdb) import npu_scripts  
(Pdb) from npu_scripts import *  
(Pdb) dev_h  
*** NameError: name 'dev_h' is not defined  
(Pdb) set_dev(self.device)  
ERROR: 'hld_debug_utils.lpm_db(la_dev)' FAILED  
ERROR: 'hld_debug_utils.cem_db(la_dev)' FAILED  
ERROR: 'hld_debug_utils.arc_counters(la_dev)' FAILED  
(Pdb) dev_h  
*** NameError: name 'dev_h' is not defined  
(Pdb) npu_sc  
*** NameError: name 'npu_sc' is not defined  
#### if above errors erupt, the possible reason is the leaba_val.py is not modified, and init() in the leaba_val is not completed.    
#### after revising leaba_val.py, do "from leaba_val import * " again, the result would be like below:   
  
(Pdb) from leaba_val import *   
(Pdb)   
(Pdb) dev_h   
<leaba_val.device_handlers_class object at 0x7f7ccf6a0908>  
(Pdb) set_dev(self.device)  
ERROR: 'hld_debug_utils.lpm_db(la_dev)' FAILED  
ERROR: 'hld_debug_utils.cem_db(la_dev)' FAILED  
ERROR: 'hld_debug_utils.arc_counters(la_dev)' FAILED  
(Pdb) npu_sc   
<npu_scripts.npu_scripts object at 0x7f7ccf6a0a58>   

It seems npu_sc has been created correctly  

## debug with NPE
(Pdb) slice = 1
(Pdb) stage = "termination"
(Pdb) npu_sc.npe_stop_and_step_macro(enable=True, step=False, slice=slice, stage=stage, npe_index=0, print_note=True)
0
Slice[1].Stage['termination'].NPE[0] -> Enable Stop macro feature
(Pdb) npu_sc.npe_stop_and_step_macro(enable=True, step=False, slice=slice, stage=stage, npe_index=0, print_note=True)
1
(Pdb) npu_sc.rxpp_term_last_npe_macros(1,0)  
#### NOTES: 1) Max stack depth is 4. Head of the macros stack is entry=0. 2) This register is cleared once read. Since last read, 0 valid macros were performed.
  NPE-macros-stack is empty/cleared  
(Pdb) npu_sc.rxpp_term_last_npe_macros(2,0)  
#### NOTES: 1) Max stack depth is 4. Head of the macros stack is entry=0. 2) This register is cleared once read. Since last read, 0 valid macros were performed.
  NPE-macros-stack is empty/cleared  
(Pdb) npu_sc.rxpp_term_last_npe_macros(3,0)  
#### NOTES: 1) Max stack depth is 4. Head of the macros stack is entry=0. 2) This register is cleared once read. Since last read, 0 valid macros were performed.
  NPE-macros-stack is empty/cleared  
(Pdb) npu_sc.rxpp_term_last_npe_macros(4,0)   
#### NOTES: 1) Max stack depth is 4. Head of the macros stack is entry=0. 2) This register is cleared once read. Since last read, 0 valid macros were performed.
  NPE-macros-stack is empty/cleared  
(Pdb) npu_sc.print_parsed_npe_key("termination", 1, 0, "a")  
Key type: npl_svl_destination_pack_table_key_option_tm_header_type_unicast_flb_t, Value: 0xec925
  const1_4b0_exact_0x0: 0x9
  const2_DESTINATION_DSP_PREFIX_exact_0xb: 0x1d
  device_svl_packet_app_soft_npuh_svl_uc_data_dsp_10_8_: 0x1
  device_svl_packet_app_soft_npuh_svl_uc_data_dsp_7_0_: 0x25  
(Pdb)  
Key type: npl_svl_destination_pack_table_key_option_tm_header_type_unicast_flb_t, Value: 0xec925
  const1_4b0_exact_0x0: 0x9
  const2_DESTINATION_DSP_PREFIX_exact_0xb: 0x1d
  device_svl_packet_app_soft_npuh_svl_uc_data_dsp_10_8_: 0x1
  device_svl_packet_app_soft_npuh_svl_uc_data_dsp_7_0_: 0x25  
(Pdb) npu_sc.get_npe_lookups_and_results(stage="termination", slice=1, npe_index=0, print_note=True)  
|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Key Bucket |                   Key Type                    | Key Value | Result Bucket |                  Result Type                  | Result Value |
|=======================================================================================================================================================|
|     a      |      npl_svl_destination_pack_table_key_      |  0xec925  |       a       |   npl_svl_destination_pack_table_payloads_t   |     0x0      |
|            |      option_tm_header_type_unicast_flb_t      |           |               |                                               |              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|
|     b      |   npl_svl_npu_base_header_pack_table_key_t    | 0x1186c1  |       b       | npl_svl_npu_base_header_pack_table_payloads_t |     0x0      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|
|     d      | npl_qos_tag_muxing_for_inner_header_over_l3_t |    0x9    |       d       |                npl_qos_tags_t                 |     0x0      |
|            | able_key_option_protocol_type_ethernet_vlan_t |           |               |                                               |              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|



For elaboration of keys/results:  
     npu_sc.print_parsed_npe_key(<stage>, <slice>, <npe index>, <bucket a/b/c/d>)  
     npu_sc.print_parsed_npe_result(<stage>, <slice>, <npe index>, <bucket a/b/c/d>)  
Examples:  
     npu_sc.print_parsed_npe_key("termination", 1, 0, "a")  
     npu_sc.print_parsed_npe_result("termination", 1, 0, "a")  
(Pdb)  
|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Key Bucket |                   Key Type                    | Key Value | Result Bucket |                  Result Type                  | Result Value |
|=======================================================================================================================================================|
|     a      |      npl_svl_destination_pack_table_key_      |  0xec925  |       a       |   npl_svl_destination_pack_table_payloads_t   |     0x0      |
|            |      option_tm_header_type_unicast_flb_t      |           |               |                                               |              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|
|     b      |   npl_svl_npu_base_header_pack_table_key_t    | 0x1186c1  |       b       | npl_svl_npu_base_header_pack_table_payloads_t |     0x0      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|
|     d      | npl_qos_tag_muxing_for_inner_header_over_l3_t |    0x9    |       d       |                npl_qos_tags_t                 |     0x0      |
|            | able_key_option_protocol_type_ethernet_vlan_t |           |               |                                               |              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|



For elaboration of keys/results:  
     npu_sc.print_parsed_npe_key(<stage>, <slice>, <npe index>, <bucket a/b/c/d>)  
     npu_sc.print_parsed_npe_result(<stage>, <slice>, <npe index>, <bucket a/b/c/d>)  
Examples:  
     npu_sc.print_parsed_npe_key("termination", 1, 0, "a")  
     npu_sc.print_parsed_npe_result("termination", 1, 0, "a")  


dev_h
<leaba_val.device_handlers_class object at 0x7f7ccf6a0908>

(Pdb) set_dev(self.device)
ERROR: 'hld_debug_utils.lpm_db(la_dev)' FAILED
ERROR: 'hld_debug_utils.cem_db(la_dev)' FAILED
ERROR: 'hld_debug_utils.arc_counters(la_dev)' FAILED
(Pdb) npu_sc
<npu_scripts.npu_scripts object at 0x7f7ccf6a0a58>



(Pdb) npu_sc.print_npe_counters_table()
+----------------------------------------------------------------------------------------------------------------------------------------+
|                                                           NPE COUNTERS TABLE                                                           |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|          |s0-in|s0-out|s0-loop|s1-in|s1-out|s1-loop|s2-in|s2-out|s2-loop|s3-in|s3-out|s3-loop|s4-in|s4-out|s4-loop|s5-in|s5-out|s5-loop|
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
| NPU-Host |  0  |  0   |   0   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Term-NPE-0|  0  |  0   |   0   |  1  |  1   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  1  |  1   |   0   |  1  |  1   |   2   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Term-NPE-1|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Term-NPE-2|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Fwd-NPE-0 |  0  |  0   |   0   |  1  |  1   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  1  |  1   |   0   |  1  |  1   |   1   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Fwd-NPE-1 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Fwd-NPE-2 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
| Tx-NPE-0 |  1  |  1   |   0   |  1  |  1   |   1   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  1  |  1   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
| Tx-NPE-1 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+


    
