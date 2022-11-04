From Tamir:
./scripts/release_candidate.sh -c GB -d 10.56.19.115 -V /proj/pacific_lab/users/tatzil/validation/gibraltar -S /cad/leaba/sdk/gibraltar-sdk-1.55.0.0 -p "-k "test_sa_pfc__uc_bridge_p2p_packet_sweep" --json=./setup/gb_perf_jsons/gibraltar_blacktip_all_100G_in_12_0_1_new_version.json --loopback_mode SERDES  -m uc_single1 --port_flow_control_mode "PFC" --pdb --debug_mode_before_traffic -sv" -f ./tests/non_default/tm_tests/pfc_snake_test.py

env BUILD_TYPE=opt3-debug scripts/release_candidate.sh -c GB -d 10.56.19.115 -V /caelab/users/yaliuliu/valid/validation-gibraltar-1.54.0.ph2ea4.3 -s /big_share2/pacific/user/yaliuliu/sdkmas -p "-k "test_sa_pfc__uc_bridge_p2p_packet_sweep" --json=./setup/regression_jsons/gibraltar_blacktip_all_100G_in_12_0_1_new_version.json --loopback_mode SERDES  -m uc_single1 --port_flow_control_mode "PFC" --pdb --debug_mode_before_traffic -sv" -f ./tests/non_default/tm_tests/pfc_snake_test.py


--------------------------log-------------------------------------------------


[root@localhost /big_share2/pacific/user/yaliuliu/sdkmas/fishnet]#
[root@localhost /big_share2/pacific/user/yaliuliu/sdkmas/fishnet]#
[root@localhost /big_share2/pacific/user/yaliuliu/sdkmas/fishnet]# env BUILD_TYPE=opt3-debug scripts/release_candidate.sh -c GB -d 1                                                                  0.56.19.115 -V /caelab/users/yaliuliu/valid/validation-gibraltar-1.54.0.ph2ea4.3 -s /big_share2/pacific/user/yaliuliu/sdkmas -p "-k                                                                   "test_sa_pfc__uc_bridge_p2p_packet_sweep" --json=./setup/regression_jsons/gibraltar_blacktip_all_100G_in_12_0_1_new_version.json --l                                                                  oopback_mode SERDES  -m uc_single1 --port_flow_control_mode "PFC" --pdb --debug_mode_before_traffic -sv" -f ./tests/non_default/tm_t                                                                  ests/pfc_snake_test.py
BSP DIR: /cad/leaba/BSP/BSP-1.0.4
/big_share2/pacific/user/yaliuliu/sdkmas
ntpdate: /cad/leaba/testing_framework/lib/libcrypto.so.10: version `OPENSSL_1.0.2' not found (required by ntpdate)
rmmod: ERROR: Module leaba_module is in use
diff: extra operand '/tmp/leaba_module/leaba_main.c'
diff: Try 'diff --help' for more information.
diff: extra operand '/tmp/leaba_module/gibraltar_leaba_registers.h'
diff: Try 'diff --help' for more information.
diff: /big_share2/pacific/user/yaliuliu/sdkmas/driver//gibraltar/out/opt3-debug/driver/modules/leaba_module/Makefile: No such file o                                                                  r directory
+ insmod /tmp/leaba_module/leaba_module.ko
insmod: ERROR: could not insert module /tmp/leaba_module/leaba_module.ko: File exists
Done leaba module
Done SPI
SDK environment is set to /big_share2/pacific/user/yaliuliu/sdkmas/driver//gibraltar/out/opt3-debug/driver
------------------------ ENVIRONMENT VARIABLES ----------------------------
FRAMEWORK = /big_share2/pacific/user/yaliuliu/sdkmas/fishnet
LEABA_PATH = /big_share2/pacific/user/yaliuliu/sdkmas/driver
BASE_OUTPUT_DIR = /big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/out/opt3-debug
LEABA_SDK_PATH = /big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/out/opt3-debug
LD_LIBRARY_PATH = /common/pkgs/gcc/4.9.4/lib64:/big_share2/pacific/user/yaliuliu/sdkmas/npsuite/lib:/big_share2/pacific/user/yaliuli                                                                  u/sdkmas/driver/gibraltar/out/opt3-debug/lib:/cad/leaba/testing_framework/lib:/big_share2/pacific/user/yaliuliu/sdkmas/driver/gibral                                                                  tar/out/opt3-debug/pylib:/cad/leaba/BSP/BSP-1.0.4/churchill_bsp
PYTHONPATH = /big_share2/pacific/user/yaliuliu/sdkmas/fishnet:/big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/out/opt3-deb                                                                  ug/pylib:/big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/out/opt3-debug/pylib/leaba/debug_tools:/big_share2/pacific/user/y                                                                  aliuliu/sdkmas/driver/gibraltar/out/opt3-debug/test/hld:/big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/out/opt3-debug/tes                                                                  t/api:/big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/out/opt3-debug/test/utils:/big_share2/pacific/user/yaliuliu/sdkmas/d                                                                  river/shared/test/utils:/big_share2/pacific/user/yaliuliu/sdkmas/driver/shared/test/api::/big_share2/pacific/user/yaliuliu/sdkmas/dr                                                                  iver/gibraltar/test/hld:/big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/shared/test/api:/big_share2/pacific/user/yaliuliu/                                                                  sdkmas/driver/gibraltar/shared/test/utils:/big_share2/pacific/user/yaliuliu/sdkmas/fishnet/utils/boards/blacktip:/caelab/users/yaliu                                                                  liu/valid/validation-gibraltar-1.54.0.ph2ea4.3:/cad/leaba/BSP/BSP-1.0.4:/cad/leaba/BSP/BSP-1.0.4/blacktip:/cad/leaba/BSP/BSP-1.0.4/w                                                                  hitetip:/cad/leaba/BSP/BSP-1.0.4/stingray:/cad/leaba/BSP/BSP-1.0.4/churchill_bsp
LAB_PATH = /caelab/users/yaliuliu/valid/validation-gibraltar-1.54.0.ph2ea4.3/validation
---------------------------------------------------------------------------
Starting regression testing...

INFO  ============================================================
INFO  ============================================================
INFO  ================= GIBRALTAR VALIDATION LOG =================
INFO  ==================based on 1.54.0.ph2ea4.3==================
INFO  ============================================================
INFO  ============================================================
--------------------------------------------------------------------------------
BSP code not imported !!!
--- SESSION ATTRIBUTES --- pytest.ASIC: GB
PR LIST ['', '']
======================================================= test session starts ========================================================
platform linux -- Python 3.6.10, pytest-6.2.1, py-1.10.0, pluggy-0.13.1 -- /common/pkgs/python/3.6.10/bin/python3.6
cachedir: .pytest_cache
benchmark: 3.2.2 (defaults: timer=time.perf_counter disable_gc=False min_rounds=5 min_time=0.000005 max_time=1.0 calibration_precisi                                                                  on=10 warmup=False warmup_iterations=100000)
hypothesis profile 'default' -> database=DirectoryBasedExampleDatabase('/big_share2/pacific/user/yaliuliu/sdkmas/fishnet/.hypothesis                                                                  /examples')
metadata: {'Python': '3.6.10', 'Platform': 'Linux-4.9.58-x86_64-with-centos-7.6.1810-Core', 'Packages': {'pytest': '6.2.1', 'py': '1                                                                  .10.0', 'pluggy': '0.13.1'}, 'Plugins': {'benchmark': '3.2.2', 'doc': '0.0.1', 'forked': '0.2', 'jira': '0.3.10', 'leaks': '0.2.2',                                                                   'profiling': '1.7.0', 'pudb': '0.6', 'repeat': '0.7.0', 'test-groups': '1.0.3', 'xdist': '1.22.2', 'ordering': '0.6', 'order': '1.0.                                                                  1', 'hypothesis': '6.31.6', 'metadata': '1.11.0', 'html': '3.1.1'}}
rootdir: /big_share2/pacific/user/yaliuliu/sdkmas/fishnet, configfile: pytest.ini
plugins: benchmark-3.2.2, doc-0.0.1, forked-0.2, jira-0.3.10, leaks-0.2.2, profiling-1.7.0, pudb-0.6, repeat-0.7.0, test-groups-1.0.                                                                  3, xdist-1.22.2, ordering-0.6, order-1.0.1, hypothesis-6.31.6, metadata-1.11.0, html-3.1.1
collected 1 item

tests/non_default/tm_tests/pfc_snake_test.py::TestSaPfcHBM__UcBridgeP2P::test_sa_pfc__uc_bridge_p2p_packet_sweep[single1-PACKET_SIZE                                                                  _10000-TC_0]
loading json file ./setup/regression_jsons/gibraltar_blacktip_all_100G_in_12_0_1_new_version.json
INFO  =========================================================================
INFO  !!! === Failed to fetch JSON data from MongoDB, fallback to local === !!!
INFO  =========================================================================
this is the modified json data:
{'address': '10.56.19.112',
 'board-rev': 1,
 'board-type': 'blacktip',
 'connectivity': {'connection': [['TE:0/1', '0:238']], 'external-loopback': [], 'self-loopback': ['all']},
 'description': 'all 100G from tg',
 'devices': [{'hbm': 'false',
              'id': 0,
              'ifg_swap_lists': [{'ifg': 1,
                                  'serdes_polarity_inverse_rx': [4, 7, 8, 13, 15, 19],
                                  'serdes_polarity_inverse_tx': [1, 2, 9, 11, 12, 13, 14, 16, 19],
                                  'slice': 2,
                                  'swap': [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23]}],
              'ports': [{'ifg': 0, 'pif': [0, 1], 'port-id': 0, 'port-speed': '100:GIGA', 'slice': 0},
                        {'ifg': 0, 'pif': [2, 3], 'port-id': 2, 'port-speed': '100:GIGA', 'slice': 0},
                        {'ifg': 1, 'pif': [8, 11], 'port-id': 238, 'port-speed': '100:GIGA', 'slice': 2}],
              'rev': 1,
              'type': 'gibraltar'}],
 'test-equipment': {'address': '10.56.19.12', 'ports': [{'name': '0/1'}], 'type': 'xena', 'user': 'alexk'}}

Taking module out of reset
Enabling module I2C bus
Busy: 0
Address NACK: 1
Data NACK: 1
Read Timeout: 0
I2C transaction to slave device failed
Taking module out of reset
Enabling module I2C bus
Value = 0x11
QSFP28 is detected
Override low power mode default configuration
Taking module out of reset
Enabling module I2C bus
Busy: 0
Address NACK: 1
Data NACK: 1
Read Timeout: 0
I2C transaction to slave device failed
Taking module out of reset
Enabling module I2C bus
Value = 0x11
QSFP28 is detected
Override low power mode default configuration
Changing VDDC_PS to 0.825
Reading new voltage: 0.826
removes pcie device
reset low
POS low
POS high
TRI_L low, SCAN_MODE high, SCAN_MODE low, TRI_L high
reset high, reset low, POS low, POS high, reset high
rescanning pcie
pcie detected
Blacktip reset device
Blacktip set core frequence to 1.350000
Waiting...
INFO  +=======================================================================================+
INFO  |          Running Tests on SDK version: dev | Test Started at: 2022-11-04 10:04        |
INFO  +=======================================================================================+
MM: suppress SDK logging for devid 288, components: RA, LLD
MM: suppress SDK logging for devid 0, components: PVT

Starting Device Init
===FN debug mode=== Setting Matilda type to NONE
-I-LLD-0- initialize: device revision=GIBRALTAR_A1
-I-LLD-0- Using regular LLD implementation, all blocks are enabled by default
-I-INTERRUPT-0- Loading interrupt tree from /big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/out/opt3-debug/res/gibraltar_i                                                                  nterrupt_tree.json: nodes 0, unique 0, registers 0, bits 0
-I-INTERRUPT-0- Loaded interrupt tree from /big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/out/opt3-debug/res/gibraltar_in                                                                  terrupt_tree.json: nodes 2686, unique 2686, registers 4508, bits 14573
-I-HLD-0- GB submodel type from eFuse value: GB
-I-LLD-0- get_core_reset: 0x3ffe0 is_reset = 1
-I-HLD-0- Device frequency set to 1350000 KHz
=== HBM is force disabled ===
-I-HLD-0- run: PASSED, repair=1, type=BIRA
-I-HLD-0- run: PASSED, repair=1, type=BISR
-I-HLD-0- run: PASSED, repair=1, type=BIST_AFTER_REPAIR
-I-HLD-0- initialize_phase_device: Before init_config_memories dvoq->init_active val: 0xd
-I-HLD-0- initialize_phase_device: After init_config_memories dvoq->init_active val: 0xd
-I-SERDES-0- Chain 0 Rcal success 24, average value 16 (range 15 ~ 19)

-I-SERDES-0- Nothing to override on Chain 0.
-I-SERDES-0- Chain 1 Rcal success 20, average value 16 (range 15 ~ 17)

-I-SERDES-0- Nothing to override on Chain 1.
-I-SERDES-0- Chain 2 Rcal success 20, average value 15 (range 15 ~ 17)

-I-SERDES-0- Nothing to override on Chain 2.
-I-SERDES-0- Chain 3 Rcal success 20, average value 16 (range 16 ~ 17)

-I-SERDES-0- Nothing to override on Chain 3.
-I-SERDES-0- Chain 4 Rcal success 20, average value 16 (range 15 ~ 18)

-I-SERDES-0- Nothing to override on Chain 4.
-I-SERDES-0- Chain 5 Rcal success 24, average value 17 (range 16 ~ 19)

-I-SERDES-0- Nothing to override on Chain 5.
-I-SERDES-0- Rcal average per chain Max 17, Min 15







-I-RA-0- Initializing NPL Resource Mapping from /big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/out/opt3-debug/res/microco                                                                  de_metadata_file.json.
-I-RA-0- Done initializing NPL Resource Mapping.
-I-RA-0- Microcode is loaded successfully. Tables are mapped. Found 645 table records.




-W-RA-0- No placement found for direct table db_access_transmit_per_dest_port_npu_host_macro_stamping_table
-W-RA-0- No placement found for direct table db_access_transmit_per_dest_port_npu_host_macro_stamping_table
-W-RA-0- No placement found for direct table db_access_transmit_per_dest_port_npu_host_macro_stamping_table
-W-RA-0- No placement found for direct table db_access_transmit_per_dest_port_npu_host_macro_stamping_table
-W-RA-0- No placement found for direct table db_access_transmit_per_dest_port_npu_host_macro_stamping_table
-W-RA-0- No placement found for direct table db_access_transmit_per_dest_port_npu_host_macro_stamping_table
-W-RA-0- No placement found for ternary table dlp0_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table dlp0_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table dlp0_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table dlp0_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table dlp0_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table dlp0_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table dlp1_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table dlp1_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table dlp1_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table dlp1_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table dlp1_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table dlp1_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table ip_ingress_cmp_mcid_static_table
-W-RA-0- No placement found for ternary table ip_ingress_cmp_mcid_static_table
-W-RA-0- No placement found for ternary table ip_ingress_cmp_mcid_static_table
-W-RA-0- No placement found for ternary table ip_ingress_cmp_mcid_static_table
-W-RA-0- No placement found for ternary table ip_ingress_cmp_mcid_static_table
-W-RA-0- No placement found for ternary table ip_ingress_cmp_mcid_static_table
-W-RA-0- No placement found for direct table ip_uc_and_acl_set_ethertype_static_table
-W-RA-0- No placement found for direct table ip_uc_and_acl_set_ethertype_static_table
-W-RA-0- No placement found for direct table ip_uc_and_acl_set_ethertype_static_table
-W-RA-0- No placement found for direct table ip_uc_and_acl_set_ethertype_static_table
-W-RA-0- No placement found for direct table ip_uc_and_acl_set_ethertype_static_table
-W-RA-0- No placement found for direct table ip_uc_and_acl_set_ethertype_static_table
-W-RA-0- No placement found for direct table issu_enabled_table
-W-RA-0- No placement found for direct table issu_enabled_table
-W-RA-0- No placement found for direct table issu_enabled_table
-W-RA-0- No placement found for direct table issu_enabled_table
-W-RA-0- No placement found for direct table issu_enabled_table
-W-RA-0- No placement found for direct table issu_enabled_table
-W-RA-0- No placement found for ternary table large_em_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table large_em_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table large_em_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table large_em_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table large_em_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table large_em_key_lsb_mapping_table
-W-RA-0- No placement found for direct table mirror_to_dsp_in_npu_soft_header_table
-W-RA-0- No placement found for direct table mirror_to_dsp_in_npu_soft_header_table
-W-RA-0- No placement found for direct table mirror_to_dsp_in_npu_soft_header_table
-W-RA-0- No placement found for direct table mirror_to_dsp_in_npu_soft_header_table
-W-RA-0- No placement found for direct table mirror_to_dsp_in_npu_soft_header_table
-W-RA-0- No placement found for direct table mirror_to_dsp_in_npu_soft_header_table
-W-RA-0- No placement found for direct table npp_exception_policer_counter_table
-W-RA-0- No placement found for direct table npp_exception_policer_counter_table
-W-RA-0- No placement found for direct table npp_exception_policer_counter_table
-W-RA-0- No placement found for direct table npp_exception_policer_counter_table
-W-RA-0- No placement found for direct table npp_exception_policer_counter_table
-W-RA-0- No placement found for direct table npp_exception_policer_counter_table
-W-RA-0- No placement found for ternary table small_em_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table small_em_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table small_em_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table small_em_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table small_em_key_lsb_mapping_table
-W-RA-0- No placement found for ternary table small_em_key_lsb_mapping_table
-W-RA-0- No placement found for direct table snoop_to_dsp_in_npu_soft_header_table
-W-RA-0- No placement found for direct table snoop_to_dsp_in_npu_soft_header_table
-W-RA-0- No placement found for direct table snoop_to_dsp_in_npu_soft_header_table
-W-RA-0- No placement found for direct table snoop_to_dsp_in_npu_soft_header_table
-W-RA-0- No placement found for direct table snoop_to_dsp_in_npu_soft_header_table
-W-RA-0- No placement found for direct table snoop_to_dsp_in_npu_soft_header_table
-W-RA-0- No placement found for ternary table splitter_lu_d_key_selector
-W-RA-0- No placement found for ternary table splitter_lu_d_key_selector
-W-RA-0- No placement found for ternary table splitter_lu_d_key_selector
-W-RA-0- No placement found for ternary table splitter_lu_d_key_selector
-W-RA-0- No placement found for ternary table splitter_lu_d_key_selector
-W-RA-0- No placement found for ternary table splitter_lu_d_key_selector
-W-RA-0- Key width 1 does not span table size 720 for table vxlan_port_table. Potential resource underutilization
-W-RA-0- No placement found for direct table inject_mact_ldb_to_output_lr
-W-RA-0- No placement found for direct table lr_filter_write_ptr_reg
-W-RA-0- No placement found for direct table lr_write_ptr_reg
-W-RA-0- No placement found for direct table learn_manager_cfg_max_learn_type_reg


-I-HLD-0- FINISHED POST SOFT RESET INIT
***============================================================***
***========= Dumping device properties for device: 0  =========***
***============================================================***
PROPERTY                                          TYPE     VALUE
------------------------------------------------  -------  ------------------------------------
LC_FORCE_FORWARD_THROUGH_FABRIC_MODE              BOOLEAN  False
LC_ADVERTISE_DEVICE_ON_FABRIC_MODE                BOOLEAN  False
LC_TYPE_2_4_T                                     BOOLEAN  True
USING_LEABA_NIC                                   BOOLEAN  True
ENABLE_NSIM_ACCURATE_SCALE_MODEL                  BOOLEAN  False
ENABLE_HBM                                        BOOLEAN  False
ENABLE_FORWARDING_ROUTE_COUNTER                   BOOLEAN  False
TEST_MODE_STACK_ADAPTER                           BOOLEAN  False
TEST_MODE_PUNT_EGRESS_PACKETS_TO_HOST             BOOLEAN  False
TEST_MODE_PACIFIC_A0_ALLOW_RCY_ON_ALL_SLICES      BOOLEAN  False
PROCESS_INTERRUPTS                                BOOLEAN  True
POLL_MSI                                          BOOLEAN  False
RTL_SIMULATION_WORKAROUNDS                        BOOLEAN  False
EMULATED_DEVICE                                   BOOLEAN  False
GB_INITIALIZE_CONFIG_MEMORIES                     BOOLEAN  True
GB_INITIALIZE_OTHER                               BOOLEAN  True
GB_A1_DISABLE_FIXES                               BOOLEAN  False
GB_A2_DISABLE_FIXES                               BOOLEAN  False
ENABLE_HBM_ROUTE_EXTENSION                        BOOLEAN  False
ENABLE_HBM_ROUTE_EXTENSION_CACHING_MODE           BOOLEAN  False
ENABLE_LPM_IP_CACHE                               BOOLEAN  True
ENABLE_LPM_TREE_COMPRESSION                       BOOLEAN  False
DISABLE_ELECTRICAL_IDLE_DETECTION                 BOOLEAN  False
ENABLE_MBIST_REPAIR                               BOOLEAN  True
IGNORE_MBIST_ERRORS                               BOOLEAN  False
SKIP_MBIST                                        BOOLEAN  False
ENABLE_NARROW_COUNTERS                            BOOLEAN  False
ENABLE_MPLS_SR_ACCOUNTING                         BOOLEAN  False
ENABLE_IP_OVER_IPV6_TUNNEL_SCALE_MODE             BOOLEAN  False
ENABLE_MPLS_BINDING_SEGMENT                       BOOLEAN  True
ENABLE_ETHERNET_CONTROL_LIST                      BOOLEAN  False
ENABLE_PBTS                                       BOOLEAN  False
ENABLE_CLASS_ID_ACLS                              BOOLEAN  False
ENABLE_PACIFIC_B0_IFG_CHANGES                     BOOLEAN  False
ENABLE_PACIFIC_OOB_INTERLEAVING                   BOOLEAN  True
INSTANTIATE_REMOTE_SYSTEM_PORTS                   BOOLEAN  False
HBM_MOVE_TO_READ_ON_EMPTY                         BOOLEAN  False
HBM_MOVE_TO_WRITE_ON_EMPTY                        BOOLEAN  False
ENABLE_SERDES_NRZ_FAST_TUNE                       BOOLEAN  False
ENABLE_NETWORK_SERDES_PAM4_FAST_TUNE              BOOLEAN  True
ENABLE_FABRIC_SERDES_PAM4_FAST_TUNE               BOOLEAN  False
ENABLE_FABRIC_FEC_RS_KP4                          BOOLEAN  False
DISABLE_SERDES_POST_ANLT_TUNE                     BOOLEAN  False
ENABLE_SERDES_PRE_ICAL_PRIOR_ANLT                 BOOLEAN  False
SERDES_DFE_EID                                    BOOLEAN  False
ENABLE_SERDES_TX_SLIP                             BOOLEAN  False
MAC_PORT_IGNORE_LONG_TUNE                         BOOLEAN  False
MAC_PORT_ENABLE_25G_DFETAP_CHECK                  BOOLEAN  False
MAC_PORT_ENABLE_SER_CHECK                         BOOLEAN  False
ENABLE_MAC_PORT_DEGRADED_SER_NOTIFICATIONS        BOOLEAN  True
ENABLE_SERDES_LOW_POWER                           BOOLEAN  False
RECONNECT_IGNORE_IN_FLIGHT                        BOOLEAN  False
ENABLE_FE_PER_DEVICE_MIN_LINKS                    BOOLEAN  False
ENABLE_LC_DESTINATION_AWARE_SCHEDULING            BOOLEAN  False
IGNORE_SBUS_MASTER_MBIST_FAILURE                  BOOLEAN  True
ENABLE_SENSOR_POLL                                BOOLEAN  True
ENABLE_PFC_PER_QUEUE_COUNTING                     BOOLEAN  False
ENABLE_PACIFIC_SW_BASED_PFC                       BOOLEAN  False
ENABLE_PFC_DEVICE_TUNING                          BOOLEAN  False
PACIFIC_PFC_HBM_ENABLED                           BOOLEAN  False
SLEEP_IN_SET_MAX_BURST                            BOOLEAN  True
STATISTICAL_METER_COUNTING                        BOOLEAN  False
ENABLE_ECN_QUEUING                                BOOLEAN  False
ENABLE_SERDES_LDO_VOLTAGE_REGULATOR               BOOLEAN  False
ENABLE_SRM_OVERRIDE_PLL_KP_KF                     BOOLEAN  True
IGNORE_COMPONENT_INIT_FAILURES                    BOOLEAN  False
ENABLE_SVL_MODE                                   BOOLEAN  False
DESTINATION_SYSTEM_PORT_IN_IBM_METADATA           BOOLEAN  False
ENABLE_REGISTER_CACHE_COUNTER                     BOOLEAN  False
MAC_PORT_ENABLE_LED                               BOOLEAN  False
MAC_PORT_ENABLE_TRAFFIC_NOTIFICATION              BOOLEAN  False
ENABLE_POWER_SAVING_MODE                          BOOLEAN  False
FORCE_DISABLE_HBM                                 BOOLEAN  True
HBM_SKIP_TRAINING                                 BOOLEAN  False
ENABLE_DUMMY_SERDES_HANDLER                       BOOLEAN  False
SERDES_RCAL_LENIENT_CALIBRATION                   BOOLEAN  False
ENABLE_INGRESS_L2_AC_PORT_COUNTERS                BOOLEAN  True
ENABLE_INGRESS_TUNNEL_COUNTERS                    BOOLEAN  True
ENABLE_INGRESS_ACE_1_COUNTERS                     BOOLEAN  False
ENABLE_INGRESS_RATE_LIMITER_PORT_COUNTERS         BOOLEAN  False
REPURPOSE_RATE_LIMITERS_TO_COUNTERS               BOOLEAN  False
PER_MAC_PORT_PER_PROTOCOL_DISCARD_COUNTERS        BOOLEAN  False
PER_MAC_PORT_PER_TTL123_NPP_COUNTERS              BOOLEAN  False
ENABLE_PER_MAC_PORT_PROTOCOL_CAST_LP_ACCOUNTING   BOOLEAN  False
ENABLE_SERVICE_COUNTERS                           BOOLEAN  False
ENABLE_UNIFIED_ACLS                               BOOLEAN  False
ENABLE_BOOT_OPTIMIZATION                          BOOLEAN  True
ENABLE_RTF_SIP_DIP_COMPRESSION                    BOOLEAN  False
GB_WATCHDOG_OQ_ENABLED                            BOOLEAN  False
GB_FABRIC_INPUT_BLOCKING_SW_WA_ENABLED            BOOLEAN  False
DAS_ENABLE_SHUFFLE_REACHABLE_LCS                  BOOLEAN  True
DISABLE_TRANSMIT_PRE_EDIT                         BOOLEAN  False
ENABLE_EGRESS_TM                                  BOOLEAN  False
NO_SERVICE_MAPPING_AND_SAME_INTERFACE_DROP        BOOLEAN  False
SVI_HOST_BD_MODE                                  BOOLEAN  False
MAC_PORT_CLEAR_FEC_CNT_BEFORE_LINKUP              BOOLEAN  False
DISABLE_URPF                                      BOOLEAN  False
ROUND_UP_SYS_PORT_SCH_PIR_SHAPER                  BOOLEAN  False
ENABLE_INACCURATE_MULTICAST_HITBIT                BOOLEAN  False
ENABLE_VXLAN_SCALE_MODE                           BOOLEAN  False
INCREASE_L2_AC_SCALE                              BOOLEAN  False
BFD_FULL_OFFLOAD                                  BOOLEAN  False
TRAP_LPTS_AFTER_POST_FWD_ACL                      BOOLEAN  False
DUMMY_BOOL_PROPERTY                               BOOLEAN  True
POLL_INTERVAL_MILLISECONDS                        INTEGER  0
POLL_FAST_INTERVAL_MILLISECONDS                   INTEGER  0
RESTORE_INTERRUPT_MASKS_INTERVAL_MILLISECONDS     INTEGER  1000
POLL_NON_WIRED_INTERRUPTS_INTERVAL_MILLISECONDS   INTEGER  1000
MSI_DAMPENING_INTERVAL_MILLISECONDS               INTEGER  100
MSI_DAMPENING_THRESHOLD                           INTEGER  10
SENSOR_POLL_INTERVAL_MILLISECONDS                 INTEGER  100
MINIMUM_FABRIC_PORTS_FOR_CONNECTIVITY             INTEGER  1
SERDES_FW_REVISION                                INTEGER  37
SERDES_FW_BUILD                                   INTEGER  2778
SBUS_MASTER_FW_REVISION                           INTEGER  4129
SBUS_MASTER_FW_BUILD                              INTEGER  8193
MAC_PORT_TUNE_TIMEOUT                             INTEGER  30
MAC_PORT_PAM4_MAX_TUNE_RETRY                      INTEGER  0
MAC_PORT_PAM4_MIN_EYE_HEIGHT                      INTEGER  16
MAC_PORT_NRZ_MIN_EYE_HEIGHT                       INTEGER  5
MAC_PORT_10G_NRZ_MIN_EYE_HEIGHT                   INTEGER  5
MAC_PORT_CDR_LOCK_AFTER_TUNE_TIMEOUT              INTEGER  10
MAC_PORT_PCS_LOCK_TIME                            INTEGER  1000
MAC_PORT_SAVE_STATE_SM_STATE_TRANSITION_CAPTURES  INTEGER  30
MAC_PORT_LINK_DEBOUNCE_PERIOD_MILLISECONDS        INTEGER  0
MAC_PORT_BAD_LINK_CHECK_ITERATIONS                INTEGER  6000
NETWORK_MAC_PORT_TUNE_AND_PCS_LOCK_ITER           INTEGER  1
FABRIC_MAC_PORT_TUNE_AND_PCS_LOCK_ITER            INTEGER  1
MAC_PORT_AUTO_NEGOTIATION_TIMEOUT                 INTEGER  500
MAC_PORT_LINK_TRAINING_TIMEOUT                    INTEGER  3
MAC_PORT_NRZ_LINK_TRAINING_TIMEOUT                INTEGER  1000
MAC_PORT_PAM4_LINK_TRAINING_TIMEOUT               INTEGER  3000
MAC_PORT_FAST_LINKUP_POLL_TIME                    INTEGER  20
SERDES_RXA_POWER_SEQUENCE_MODE                    INTEGER  1
SERDES_CL136_PRESET_TYPE                          INTEGER  1
SERDES_LOG_FILTER                                 INTEGER  4736
SERDES_LOG_ENTRIES                                INTEGER  500
LPM_REBALANCE_INTERVAL_MILLISECONDS               INTEGER  50
LPM_REBALANCE_START_FAIRNESS_THRESHOLD_PERCENT    INTEGER  80
LPM_REBALANCE_END_FAIRNESS_THRESHOLD_PERCENT      INTEGER  90
LPM_TCAM_SINGLE_WIDTH_KEY_WEIGHT                  INTEGER  1
LPM_TCAM_DOUBLE_WIDTH_KEY_WEIGHT                  INTEGER  2
LPM_TCAM_QUAD_WIDTH_KEY_WEIGHT                    INTEGER  4
LPM_L2_MAX_SRAM_BUCKETS                           INTEGER  4096
LPM_TCAM_NUM_BANKSETS                             INTEGER  2
LPM_TCAM_MAX_QUAD_ENTRIES                         INTEGER  512
LPM_TCAM_BANK_SIZE                                INTEGER  512
LPM_TREE_COMPRESSION_UPDATE_MODE                  INTEGER  4
LPM_TREE_COMPRESSION_INTERVAL                     INTEGER  100
LPM_TREE_COMPRESSION_CEILING_LENGTH               INTEGER  0
CEM_NUM_BANKS                                     INTEGER  19
DEVICE_FREQUENCY                                  INTEGER  1350000
TCK_FREQUENCY                                     INTEGER  5
RESET_INTERRUPT_COUNTERS_INTERVAL_SECONDS         INTEGER  86400
INTERRUPT_THRESHOLD_MEM_CONFIG_ECC_1B             INTEGER  100
INTERRUPT_THRESHOLD_MEM_CONFIG_ECC_2B             INTEGER  100
INTERRUPT_THRESHOLD_MEM_CONFIG_PARITY             INTEGER  100
INTERRUPT_THRESHOLD_MEM_VOLATILE_ECC_1B           INTEGER  100
INTERRUPT_THRESHOLD_MEM_VOLATILE_ECC_2B           INTEGER  10
INTERRUPT_THRESHOLD_MEM_VOLATILE_PARITY           INTEGER  10
INTERRUPT_THRESHOLD_LPM_SRAM_ECC_1B               INTEGER  100
INTERRUPT_THRESHOLD_LPM_SRAM_ECC_2B               INTEGER  10
INTERRUPT_THRESHOLD_PACKET_LOSS                   INTEGER  10
MAX_COUNTER_THRESHOLD                             INTEGER  1073741824
HBM_READ_CYCLES                                   INTEGER  512
HBM_WRITE_CYCLES                                  INTEGER  512
HBM_MIN_MOVE_TO_READ                              INTEGER  0
HBM_LPM_FAVOR_MODE                                INTEGER  2
MAX_NUMBER_OF_PERIODIC_SAVE_STATE_FILES           INTEGER  10
HBM_PHY_T_RDLAT_OFFSET                            INTEGER  7
MULTICAST_MCID_SCALE_THRESHOLD                    INTEGER  65536
MAX_NUM_PCL_GIDS                                  INTEGER  0
SGACL_MAX_CELL_COUNTERS                           INTEGER  0
MATILDA_MODEL_TYPE                                INTEGER  0
OOB_INJ_CREDITS                                   INTEGER  1
CREDIT_SIZE_IN_BYTES                              INTEGER  2048
VOQ_PREFETCH_SIZE_IN_CREDITS                      INTEGER  0
COUNTERS_SHADOW_AGE_OUT                           INTEGER  0
METER_BUCKET_REFILL_POLLING_DELAY                 INTEGER  20000
VOQ_FLUSH_RATE                                    INTEGER  400
SERVICE_COUNTERS_RTF_STEP                         INTEGER  0
INGRESS_REPLICATION_MAX_TX_COPIES_PER_SLICE       INTEGER  2000
HEALTH_MONITOR_DISCRIMINATOR_BASE                 INTEGER  65793
DUMMY_INT_PROPERTY                                INTEGER  1
FIRST_STRING_PROPERTY                             STRING   res/srm_app_fw_image_0_37_1_2778.txt
SBUS_MASTER_FW_FILE_NAME                          STRING   res/sbus_master.0x1024_2001.rom
DUMMY_STRING_PROPERTY                             STRING   dummy_gibraltar
***============================================================***
***=========================== Done ===========================***
***============================================================***
Initializing gibraltar memories...






loading performance csv file /big_share2/pacific/user/yaliuliu/sdkmas/fishnet/setup/gb_perf_jsons/gibraltar_1350.csv

loading apps performance json file /big_share2/pacific/user/yaliuliu/sdkmas/fishnet/setup/apps_performance.json
INFO  ----------------------------------
INFO  Setup Description:all 100G from tg
INFO  ----------------------------------

Creating port handlers
 serdes params /big_share2/pacific/user/yaliuliu/sdkmas/driver/shared/examples/sanity/blacktip_serdes_settings.json
MIN_PKT_SIZE = 214, frequency = 1.35
MIN_PKT_SIZE = 64, largest ifg rate = 200, frequency = 1.35

Initializing ports
--- ACLS --- created key profile IPV4, INGRESS, on tcam_interface E_0
--- ACLS --- created key profile IPV4, INGRESS, on tcam_interface E_1
--- ACLS --- created key profile IPV4, INGRESS, on tcam_interface E_0_AND_1
--- ACLS --- created key profile IPV6, INGRESS, on tcam_interface E_0
--- ACLS --- created key profile IPV6, INGRESS, on tcam_interface E_1
--- ACLS --- created key profile IPV6, INGRESS, on tcam_interface E_0_AND_1
--- ACLS --- created key profile ETHERNET, INGRESS, on tcam_interface E_0
--- ACLS --- created key profile ETHERNET, INGRESS, on tcam_interface E_0
--- ACLS --- created key profile IPV4, EGRESS, on tcam_interface E_0_AND_1
--- ACLS --- created key profile IPV6, EGRESS, on tcam_interface E_0_AND_1
--- ACLS --- created command profile
USE SDK LBR
Trying to load serdes param file /big_share2/pacific/user/yaliuliu/sdkmas/driver/shared/examples/sanity/blacktip_serdes_settings.jso                                                                  n
--- NOTIFICATION HANDLER --- Notifications and port state listener thread started
--- NOTIFICATION HANDLER --- : Adding MEM_PROTECT, block: 0xeb, addr: -0x1, bit: -1, ALL to ignore list - expected number of interru                                                                  pts in range: [None,None]
creating ports (MAC, Sys, Eth) on    0 (slice:0, ifg:0, pif: 0)
Setting port 0 into LoopbackMode.SERDES
creating ports (MAC, Sys, Eth) on    2 (slice:0, ifg:0, pif: 2)
Setting port 2 into LoopbackMode.SERDES
creating ports (MAC, Sys, Eth) on  238 (slice:2, ifg:1, pif: 8)
--- NOTIFICATION HANDLER --- : Adding LINK, link_status: ALL, port_id: None, type: None to ignore list - expected number of interrup                                                                  ts in range: [None,None]
Started activating mac ports
-I-SERDES-0- Serdes 0/0/0 PLL baud rate will be reconfigured. Die 0x0 - Current baud rate configured to 0x0. New baud rate to set 0x                                                                  1954fc4.
-I-SERDES-0- Serdes 0/0/2 PLL baud rate will be reconfigured. Die 0x100 - Current baud rate configured to 0x0. New baud rate to set                                                                   0x1954fc4.
-I-SERDES-0- Serdes 2/1/8 PLL baud rate will be reconfigured. Die 0x5400 - Current baud rate configured to 0x0. New baud rate to set                                                                   0x1896402.
-I-SERDES-0- Serdes 2/1/8 PLL baud rate will be reconfigured. Die 0x5500 - Current baud rate configured to 0x0. New baud rate to set                                                                   0x1896402.
DEBUG Starting new HTTPS connection (1): jira-eng-sjc1.cisco.com:443
-I-MAC_PORT-0- mac_port la_mac_port_base(oid=374)#SerDes 0/0/0# changed state to UP
-I-MAC_PORT-0- mac_port la_mac_port_base(oid=390)#SerDes 0/0/2# changed state to UP
--- EXPECTED LINK NOTIFICATION ---: --- Notification ---:Fri Nov  4 10:07:17 2022 (1): LINK: UP: Port 0, Slice 0, IFG 0, SerDes 0
--- EXPECTED LINK NOTIFICATION ---: --- Notification ---:Fri Nov  4 10:07:17 2022 (2): LINK: UP: Port 2, Slice 0, IFG 0, SerDes 2
DEBUG https://jira-eng-sjc1.cisco.com:443 "GET /jira/rest/api/2/issue/FNET-367 HTTP/1.1" 200 None
DEBUG Starting new HTTPS connection (1): jira-eng-sjc1.cisco.com:443
-I-MAC_PORT-0- mac_port la_mac_port_base(oid=406)#SerDes 2/1/8# changed state to UP
--- EXPECTED LINK NOTIFICATION ---: --- Notification ---:Fri Nov  4 10:07:17 2022 (3): LINK: UP: Port 238, Slice 2, IFG 1, SerDes 8
DEBUG https://jira-eng-sjc1.cisco.com:443 "GET /jira/rest/api/2/mypermissions HTTP/1.1" 200 None
DEBUG Starting new HTTPS connection (1): jira-eng-sjc1.cisco.com:443
DEBUG https://jira-eng-sjc1.cisco.com:443 "GET /jira/rest/api/2/issue/FNET-367 HTTP/1.1" 200 None
--- NOTIFICATION HANDLER --- : Removing LINK, link_status: ALL, port_id: None, type: None from ignore list
--- verify ports are up --- all mac ports are activated and up after 5.007081237999955 sec. Waited 4.503381340007763 sec after ports                                                                   activation for link up notifications
Link [0] name 2x56G, FC 2, FEC 3, (slice 0,IFG 0, SerDes 0), link True, pcs True
Link [2] name 2x56G, FC 2, FEC 3, (slice 0,IFG 0, SerDes 2), link True, pcs True
Link [238] name 4x56G, FC 2, FEC 2, (slice 2,IFG 1, SerDes 8), link True, pcs True
Link [0] name 2x56G, (slice 0, IFG 0, SerDes 0), BER 0.000e+00, FLR 0.000e+00, FLR_R 0.0 Codewords [68064320, 0, 0, 0, 0, 0, 0, 0, 0                                                                  , 0, 0, 0, 0, 0, 0, 0], Uncorrectable 0, Symbol bursts [0, 0, 0, 0, 0, 0, 0]
Link [2] name 2x56G, (slice 0, IFG 0, SerDes 2), BER 0.000e+00, FLR 0.000e+00, FLR_R 0.0 Codewords [68040354, 0, 0, 0, 0, 0, 0, 0, 0                                                                  , 0, 0, 0, 0, 0, 0, 0], Uncorrectable 0, Symbol bursts [0, 0, 0, 0, 0, 0, 0]
Link [238] name 4x56G, (slice 2, IFG 1, SerDes 8), BER 0.000e+00, FLR 0.000e+00, FLR_R 0.0 Codewords [54326451, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0, 0, 0, 0, 0, 0], Uncorrectable 0, Symbol bursts [0, 0, 0, 0, 0, 0, 0]
fabric ports tune Done # 0 fabric_mac_ports.
***============================================================***
***=== Applying validation ENV - set debug device handlers  ===***
***============================================================***

Initializing gibraltar memories...

Starting tests...

Test results are not stored in DB.
--- NOTIFICATION HANDLER --- : Adding LINK, link_status: ALL, port_id: None, type: None to ignore list - expected number of interrup                                                                  ts in range: [None,None]
Send()         : ; ######################################
Send() received:
Send()         : ; Logon and Reserve
Send() received:
Send()         : ; ######################################
Send() received:
SendExpect(<OK>): c_logon "xena"
SendExpect(<OK>): c_owner "alexk"
SendExpect(<OK>): C_TIMEOUT 259200
===> MM: [DEBUG] get_te_speed(): te_id = 238
In PortReserve
1
Send()         : 0/1 p_reservation ?
Send() received: 0/1  P_RESERVATION  RESERVED_BY_OTHER
finish reservation ports=0/1
Port 0/1 is reserved by other - relinquish
SendExpect(<OK>): 0/1 p_reservation relinquish
SendExpect(<OK>): 0/1 p_reservation reserve
SendExpect(<OK>): 0/1 PP_FECMODE ON
SendExpect(<OK>): 0/1 P_RESET
SendExpect(<OK>): 0/1 PT_CLEAR
SendExpect(<OK>): 0/1 PR_CLEAR
SendExpect(<OK>): 0/1 p_traffic off
Waiting for Traffic Generator links up state ...
--- NOTIFICATION HANDLER --- : Removing LINK, link_status: ALL, port_id: None, type: None from ignore list
INFO  is_simulator = False
INFO  debug_mode = True

+======================================================================================================+
|  Running : [10:09:16.951498] test_sa_pfc__uc_bridge_p2p_packet_sweep[single1-PACKET_SIZE_10000-TC_0] |
+======================================================================================================+
Description:

        The purpose of this test is to check PFC mechanism in HBM.
        SDK is not yet ready, RxCGM confiuration is done by writing to configuration registers.
        In this test port shapers are used to evict queues to DRAM.
        RxCGM is configured to send PFC messages before DRAM queue reaches its limit.
        Execute tests with HBM, single flow snake of Bridge P2P.
        packet sweep of random distance between sizes
        Packet sizes -1, -2, -3 are IMIX
----------------------------------------------------------------------------------------------------------------------------------
--- NOTIFICATION HANDLER --- pre test dump and reset notifications
--- NOTIFICATION HANDLER --- Dumping ignored notifications
dump_notifications_db: device_id=0, total notifications=3
--- Notification ---:Fri Nov  4 10:07:17 2022 (1): LINK: UP: Port 0, Slice 0, IFG 0, SerDes 0, count=1
--- Notification ---:Fri Nov  4 10:07:17 2022 (2): LINK: UP: Port 2, Slice 0, IFG 0, SerDes 2, count=1
--- Notification ---:Fri Nov  4 10:07:17 2022 (3): LINK: UP: Port 238, Slice 2, IFG 1, SerDes 8, count=1
--- NOTIFICATION HANDLER ---  All notifications are now cleared

--> Clean errors log
---- Clear debug counters: Pre test ----
INFO  ___________________Slice0_____________________|____________Slice1___________|___________Slice2____________|___________Slice3__                                                                  __________|___________Slice4____________|_____________Slice5___________|
INFO  IFG_RX0 packets          =               0    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =                                                                                 0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFG_RX1 packets          =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =                                                                                 0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  IFG_RX0 bytes            =               0    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =                                                                                 0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFG_RX1 bytes            =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =                                                                                 0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  IFGB_RX0 packets         =               0    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =                                                                                 0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFGB_RX1 packets         =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =                                                                                 0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  RXPP IFG0 input packets  =               0    |RXPP2   =               0    |RXPP4   =               0    |RXPP6   =                                                                                 0    |RXPP8   =               0    |RXPP10   =               0    |
INFO  RXPP IFG1 input packets  =               0    |RXPP3   =               0    |RXPP5   =               0    |RXPP7   =                                                                                 0    |RXPP9   =               0    |RXPP11   =               0    |
INFO  RXPP IFG0 output packets =               0    |RXPP2   =               0    |RXPP4   =               0    |RXPP6   =                                                                                 0    |RXPP8   =               0    |RXPP10   =               0    |
INFO  RXPP IFG1 output packets =               0    |RXPP3   =               0    |RXPP5   =               0    |RXPP7   =                                                                                 0    |RXPP9   =               0    |RXPP11   =               0    |
INFO  SMS IFG0 write packets   =               0    |SMS2    =               0    |SMS4    =               0    |SMS6    =                                                                                 0    |SMS8    =               0    |SMS 10   =               0    |
INFO  SMS IFG1 write packets   =               0    |SMS3    =               0    |SMS5    =               0    |SMS7    =                                                                                 0    |SMS9    =               0    |SMS 11   =               0    |
INFO  REASSEMBLY Slc0 packets  =               0    |REAS1   =               0    |REAS2   =               0    |REAS3   =                                                                                 0    |REAS4   =               0    |REAS5    =               0    |
INFO  PDVOQ Slice0 packets     =               0    |PDVOQ1  =               0    |PDVOQ2  =               0    |PDVOQ3  =                                                                                 0    |PDVOQ4  =               0    |PDVOQ5   =               0    |
INFO  PDVOQ Slice0 bytes       =               0    |PDVOQ1  =               0    |PDVOQ2  =               0    |PDVOQ3  =                                                                                 0    |PDVOQ4  =               0    |PDVOQ5   =               0    |
INFO  FILB Slice0 packets      =               0    |FILB1   =               0    |FILB2   =               0    |FILB3   =                                                                                 0    |FILB4   =               0    |FILB5    =               0    |
INFO  FILB Slice0 bytes        =               0    |FILB1   =               0    |FILB2   =               0    |FILB3   =                                                                                 0    |FILB4   =               0    |FILB5    =               0    |
INFO  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX--C--R--O--S--S--XXXXXXXXXX--B--A--R--XXXXXX                                                                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX|
INFO  TXPDR Slice0 packets     =               0    |TXPDR1  =               0    |TXPDR2  =               0    |TXPDR3  =                                                                                 0    |TXPDR4  =               0    |TXPDR5   =               0    |
INFO  TXCGM Slice0 packets     =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =                                                                                 0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 bytes       =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =                                                                                 0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 UC packets  =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =                                                                                 0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 MC packets  =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =                                                                                 0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  SMS IFG0 read packets    =               0    |SMS2    =               0    |SMS4    =               0    |SMS6    =                                                                                 0    |SMS8    =               0    |SMS 10   =               0    |
INFO  SMS IFG1 read packets    =               0    |SMS3    =               0    |SMS5    =               0    |SMS7    =                                                                                 0    |SMS9    =               0    |SMS 11   =               0    |
INFO  TXPP0 packets            =               0    |TXPP2   =               0    |TXPP4   =               0    |TXPP6   =                                                                                 0    |TXPP8   =               0    |TXPP10   =               0    |
INFO  TXPP1 packets            =               0    |TXPP3   =               0    |TXPP5   =               0    |TXPP7   =                                                                                 0    |TXPP9   =               0    |TXPP11   =               0    |
INFO  IFGB_TX0 packets         =               0    |IFGB2   =               0    |IFGB4   =               0    |IFGB6   =                                                                                 0    |IFGB8   =               0    |IFGB10   =               0    |
INFO  IFGB_TX1 packets         =               0    |IFGB3   =               0    |IFGB5   =               0    |IFGB7   =                                                                                 0    |IFGB9   =               0    |IFGB11   =               0    |
INFO  IFG_TX0 good packets     =               0    |IFG_TX2 =               0    |IFG_TX4 =               0    |IFG_TX6 =                                                                                 0    |IFG_TX8 =               0    |IFG_TX10 =               0    |
INFO  IFG_TX1 good packets     =               0    |IFG_TX3 =               0    |IFG_TX5 =               0    |IFG_TX7 =                                                                                 0    |IFG_TX9 =               0    |IFG_TX11 =               0    |
INFO  IFG_TX0 good bytes       =               0    |IFG_TX2 =               0    |IFG_TX4 =               0    |IFG_TX6 =                                                                                 0    |IFG_TX8 =               0    |IFG_TX10 =               0    |
INFO  IFG_TX1 good bytes       =               0    |IFG_TX3 =               0    |IFG_TX5 =               0    |IFG_TX7 =                                                                                 0    |IFG_TX9 =               0    |IFG_TX11 =               0    |
INFO  (*) = counter overflow
+-----------------------------------------------------------------------------------------------------------------------------------                                                                  -----+
|                                                           NPE COUNTERS TABLE                                                                                                                             |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+--                                                                  -----+
|          |s0-in|s0-out|s0-loop|s1-in|s1-out|s1-loop|s2-in|s2-out|s2-loop|s3-in|s3-out|s3-loop|s4-in|s4-out|s4-loop|s5-in|s5-out|s5                                                                  -loop|
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+--                                                                  -----+
| NPU-Host |  0  |  0   |   0   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |                                                                     -   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+--                                                                  -----+
|Term-NPE-0|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |                                                                     0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+--                                                                  -----+
|Term-NPE-1|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |                                                                     0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+--                                                                  -----+
|Term-NPE-2|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |                                                                     0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+--                                                                  -----+
|Fwd-NPE-0 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |                                                                     0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+--                                                                  -----+
|Fwd-NPE-1 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |                                                                     0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+--                                                                  -----+
|Fwd-NPE-2 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |                                                                     0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+--                                                                  -----+
| Tx-NPE-0 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |                                                                     0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+--                                                                  -----+
| Tx-NPE-1 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |                                                                     0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+--                                                                  -----+
CAUTION: THIS CLI IS RESOURCE INTENSIVE AND CAN CAUSE ROUTE UPDATES TO GET BLOCKED TEMPORARILY, DO NOT RUN IT PERIODICALLY. THIS IS                                                                   A DEBUG CLI AND SHOULD BE RUN ONLY WHEN NECESSARY.
+---------------------------------------------------------+--------+--------+--------+--------+--------+--------+--------+--------+-                                                                  -------+--------+---------+---------+---------+---------+---------+---------+---------+
| Metric / Core                                           | Core 0 | Core 1 | Core 2 | Core 3 | Core 4 | Core 5 | Core 6 | Core 7 |                                                                   Core 8 | Core 9 | Core 10 | Core 11 | Core 12 | Core 13 | Core 14 | Core 15 | Tot/Avg |
+---------------------------------------------------------+--------+--------+--------+--------+--------+--------+--------+--------+-                                                                  -------+--------+---------+---------+---------+---------+---------+---------+---------+
| Entries                                                 | 2      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 2       |
| IPv4 Entries                                            | 1      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 1       |
| IPv6 Entries                                            | 1      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 1       |
| IPv4 SRAM Entries                                       | 1      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 1       |
| IPv4 HBM Entries                                        | 0      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 0       |
| IPv6 SRAM Entries                                       | 1      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 1       |
| IPv6 HBM Entries                                        | 0      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 0       |
| TCAM Occupied Rows                                      | 3      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 3       |
| TCAM Free Rows                                          | 4089   | 4092   | 4092   | 4092   | 4092   | 4092   | 4092   | 4092   |                                                                   4092   | 4092   | 4092    | 4092    | 4092    | 4092    | 4092    | 4092    | 65469   |
| IPv4 TCAM Entries                                       | 1      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 1       |
| IPv6 double TCAM Entries                                | 1      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 1       |
| IPv6 quad TCAM Entries                                  | 0      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 0       |
| L1 Rows                                                 | 1      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 1       |
| L1 Entries                                              | 2      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 2       |
| L2 SRAM Rows                                            | 1      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 1       |
| L2 HBM Rows                                             | 0      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 0       |
| L2 SRAM Single Entries                                  | 2      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 2       |
| L2 SRAM Double Entries                                  | 0      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 0       |
| L2 HBM Entries                                          | 0      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |                                                                   0      | 0      | 0       | 0       | 0       | 0       | 0       | 0       | 0       |
| TCAM Occupancy                                          | 0.1%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   |                                                                   0.0%   | 0.0%   | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    |
| L1 Occupancy (% Rows used)                              | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   |                                                                   0.0%   | 0.0%   | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    |
| L2 SRAM Occupancy (% Rows used)                         | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   |                                                                   0.0%   | 0.0%   | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    |
| L2 HBM Occupancy (% Rows used)                          | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   |                                                                   0.0%   | 0.0%   | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    |
| TCAM Entries Utilization (of occupied single entries)   | 66.7%  | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   |                                                                   0.0%   | 0.0%   | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 66.7%   |
| L1 Utilization (of occupied buckets)                    | 25.0%  | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   |                                                                   0.0%   | 0.0%   | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 25.0%   |
| L2 SRAM Entries Utilization (of occupied buckets)       | 11.1%  | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   |                                                                   0.0%   | 0.0%   | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 11.1%   |
| L2 HBM Entries Utilization (of occupied buckets)        | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   |                                                                   0.0%   | 0.0%   | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    |
| L2 Total Entries Utilization (include SRAM and HBM)     | 11.1%  | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   |                                                                   0.0%   | 0.0%   | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 11.1%   |
| L2 SRAM Space Utilization (of occupied buckets)         | 11.1%  | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   |                                                                   0.0%   | 0.0%   | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 11.1%   |
| L2 HBM Space Utilization (of occupied buckets)          | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   |                                                                   0.0%   | 0.0%   | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    |
| L2 Total Space Utilization (include SRAM and HBM)       | 11.1%  | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   |                                                                   0.0%   | 0.0%   | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 11.1%   |
| Total Entries Utilization (% used out of max potential) | 1.9%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   | 0.0%   |                                                                   0.0%   | 0.0%   | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 0.0%    | 1.9%    |
+---------------------------------------------------------+--------+--------+--------+--------+--------+--------+--------+--------+-                                                                  -------+--------+---------+---------+---------+---------+---------+---------+---------+
+------+------+-------+--------+-------+------+------------------------+------------------------+------------+-----------+
| Line | Type | Width | Prefix | Group | Core | Key                    | Mask                   | Group (hw) | Core (hw) |
+------+------+-------+--------+-------+------+------------------------+------------------------+------------+-----------+
| 0    | ipv4 | 1     | 0x0    | 64    | 0    | 0x00000000000000000000 | 0x80000000000000000000 | 64         | 0         |
| 127  | ipv6 | 1     | 0x1    | 0     | 0    | 0x80000000000000000000 | 0xc0000000000000000000 | 0          | 0         |
+------+------+-------+--------+-------+------+------------------------+------------------------+------------+-----------+
Printing CEM and ARC counters
--> Printing arc debug counters
main_loop                                   = 33114
cpu_command                                 = 1
response_to_cpu                             = 1
learn_new_events                            = 0
learn_update_events                         = 0
learn_refresh_events                        = 0
learn_new                                   = 0
simple_insert                               = 0
cpu_simple_insert                           = 0
warm_boot_eresource                         = 0
cpu_double_insert                           = 0
relocate                                    = 0
relocate_for_double                         = 0
relocate_double_entries                     = 0
cam_insert                                  = 0
cpu_erase                                   = 0
cpu_erase_not_found                         = 0
new_insert_fail                             = 0
update_lookup_fail                          = 0
update_conflicts                            = 0
poll_timeout                                = 0
read_request                                = 0
static_MAC                                  = 0
dynamic_MAC                                 = 0
age_sweep                                   = 0
age_configs                                 = 0
age_interval                                = 0
aged_entries                                = 0
age_ecc_error                               = 0
age_read_retry                              = 0
age_read_mismatches                         = 0
age_write_mismatches                        = 0
age_static_mismatches                       = 0
age_dynamic_mismatches                      = 0
age_value_mismatches                        = 0
age_check_invalid_entries                   = 0
age_check_retries                           = 0
age_check_failures                          = 0
update_limit_exceeds                        = 0
limit_counter_underflow                     = 0
occupancy_ctr_underflow                     = 0
cpu_lookups                                 = 0
cpu_lookups_location                        = 0
cpu_lookup_not_found                        = 0
cpu_entry_overwrite                         = 0
cpu_read_not_found                          = 0
double_relocation_EM_FFE                    = 0
double_relocation_EM_READ                   = 0
double_relocation_EM_READ_fails             = 0
double_relocation_EM_STORE                  = 0
double_relocation_EM_STORE_fails            = 0
double_insert_EM_FFE                        = 0
double_insert_EM_READ                       = 0
double_insert_EM_READ_fails                 = 0
double_insert_single_relocation_fails       = 0
double_relocation_parent-node_backwalks     = 0
double_relocation_BST_loops_detected        = 0
total_evacuation_tries                      = 0
features_not_found                          = 0
em_lookup_fail                              = 0
em_write_fail                               = 0
em_ffe_fail                                 = 0
em_read_fail                                = 0
em_pop_fail                                 = 0
em_delete_fail                              = 0
em_age_write_fail                           = 0
em_age_read_fail                            = 0
em_quick_insert_fail                        = 0
--> Printing EM cores total entries counters (SRAM+CAM)
{'total': 0}
--> Printing EM cores CAM entries counters (subset of the total per core)
{0: 0, 1: 0, 2: 0, 3: 0, 4: 0, 5: 0, 6: 0, 7: 0, 8: 0, 9: 0, 10: 0, 11: 0, 12: 0, 13: 0, 14: 0, 15: 0, 'total': 0}
applying trap LA_EVENT_ETHERNET_FIRST
applying trap LA_EVENT_ETHERNET_DOT1X_DROP
applying trap LA_EVENT_ETHERNET_ACL_DROP
applying trap LA_EVENT_ETHERNET_ACL_FORCE_PUNT
applying trap LA_EVENT_ETHERNET_ACCEPTABLE_FORMAT
applying trap LA_EVENT_ETHERNET_NO_SERVICE_MAPPING
applying trap LA_EVENT_ETHERNET_NO_TERMINATION_ON_L3_PORT
applying trap LA_EVENT_ETHERNET_NO_SIP_MAPPING
applying trap LA_EVENT_ETHERNET_NO_VNI_MAPPING
applying trap LA_EVENT_ETHERNET_NO_VSID_MAPPING
applying trap LA_EVENT_ETHERNET_ARP
applying trap LA_EVENT_ETHERNET_SA_DA_ERROR
applying trap LA_EVENT_ETHERNET_SA_ERROR
applying trap LA_EVENT_ETHERNET_DA_ERROR
applying trap LA_EVENT_ETHERNET_SA_MULTICAST
applying trap LA_EVENT_ETHERNET_DHCPV4_SERVER
applying trap LA_EVENT_ETHERNET_DHCPV4_CLIENT
applying trap LA_EVENT_ETHERNET_DHCPV6_SERVER
applying trap LA_EVENT_ETHERNET_DHCPV6_CLIENT
applying trap LA_EVENT_ETHERNET_INGRESS_STP_BLOCK
applying trap LA_EVENT_ETHERNET_PTP_OVER_ETH
applying trap LA_EVENT_ETHERNET_ISIS_OVER_L2
applying trap LA_EVENT_ETHERNET_L2CP0
applying trap LA_EVENT_ETHERNET_L2CP1
applying trap LA_EVENT_ETHERNET_L2CP2
applying trap LA_EVENT_ETHERNET_L2CP3
applying trap LA_EVENT_ETHERNET_L2CP4
applying trap LA_EVENT_ETHERNET_L2CP5
applying trap LA_EVENT_ETHERNET_L2CP6
applying trap LA_EVENT_ETHERNET_L2CP7
applying trap LA_EVENT_ETHERNET_LACP
applying trap LA_EVENT_ETHERNET_CISCO_PROTOCOLS
applying trap LA_EVENT_ETHERNET_MACSEC
applying trap LA_EVENT_ETHERNET_UNKNOWN_L3
applying trap LA_EVENT_ETHERNET_TEST_OAM_AC_MEP
applying trap LA_EVENT_ETHERNET_TEST_OAM_AC_MIP
applying trap LA_EVENT_ETHERNET_TEST_OAM_CFM_LINK_MDL0
applying trap LA_EVENT_ETHERNET_SYSTEM_MYMAC
applying trap LA_EVENT_ETHERNET_UNKNOWN_BC
applying trap LA_EVENT_ETHERNET_UNKNOWN_MC
applying trap LA_EVENT_ETHERNET_UNKNOWN_UC
applying trap LA_EVENT_ETHERNET_LEARN_PUNT
applying trap LA_EVENT_ETHERNET_BCAST_PKT
applying trap LA_EVENT_ETHERNET_PFC_SAMPLE
applying trap LA_EVENT_ETHERNET_SMAC_MISS
applying trap LA_EVENT_ETHERNET_HOP_BY_HOP
applying trap LA_EVENT_ETHERNET_MC_SNOOP_LOOKUP_MISS
applying trap LA_EVENT_ETHERNET_UNPROTECTED_DATA_PKT_ON_MACSEC_EN_PORT
applying trap LA_EVENT_ETHERNET_MACSEC_PROCESSING_ERR
applying trap LA_EVENT_ETHERNET_L2_DLP_NOT_FOUND
applying trap LA_EVENT_ETHERNET_SAME_INTERFACE
applying trap LA_EVENT_ETHERNET_DSPA_MC_TRIM
applying trap LA_EVENT_ETHERNET_EGRESS_STP_BLOCK
applying trap LA_EVENT_ETHERNET_SPLIT_HORIZON
applying trap LA_EVENT_ETHERNET_DISABLED
applying trap LA_EVENT_ETHERNET_INCOMPATIBLE_EVE_CMD
applying trap LA_EVENT_ETHERNET_PADDING_RESIDUE_IN_SECOND_LINE
applying trap LA_EVENT_ETHERNET_PFC_DIRECT_SAMPLE
applying trap LA_EVENT_ETHERNET_SVI_EGRESS_DHCP
applying trap LA_EVENT_ETHERNET_NO_PWE_L3_DEST
applying trap LA_EVENT_ETHERNET_LAST
applying trap LA_EVENT_IPV4_IIC_CHECK_FAIL
applying trap LA_EVENT_IPV4_MC_FORWARDING_DISABLED
applying trap LA_EVENT_IPV4_UC_FORWARDING_DISABLED
applying trap LA_EVENT_IPV4_CHECKSUM
applying trap LA_EVENT_IPV4_HEADER_ERROR
applying trap LA_EVENT_IPV4_UNKNOWN_PROTOCOL
applying trap LA_EVENT_IPV4_OPTIONS_EXIST
applying trap LA_EVENT_IPV4_NON_COMP_MC
applying trap LA_EVENT_IPV6_MC_FORWARDING_DISABLED
applying trap LA_EVENT_IPV6_UC_FORWARDING_DISABLED
applying trap LA_EVENT_IPV6_HOP_BY_HOP
applying trap LA_EVENT_IPV6_HEADER_ERROR
applying trap LA_EVENT_IPV6_ILLEGAL_DIP
applying trap LA_EVENT_IPV6_ZERO_PAYLOAD
applying trap LA_EVENT_IPV6_DESTINATION_OPTIONS_HEADER
applying trap LA_EVENT_IPV6_NON_COMP_MC
applying trap LA_EVENT_MPLS_UNKNOWN_PROTOCOL_AFTER_BOS
applying trap LA_EVENT_MPLS_TTL_IS_ZERO
applying trap LA_EVENT_MPLS_MPLS_TP_OVER_LSP
applying trap LA_EVENT_MPLS_OAM_ALERT_LABEL
applying trap LA_EVENT_MPLS_EXTENSION_LABEL
applying trap LA_EVENT_MPLS_ROUTER_ALERT_LABEL
applying trap LA_EVENT_MPLS_UNEXPECTED_RESERVED_LABEL
applying trap LA_EVENT_MPLS_FORWARDING_DISABLED
applying trap LA_EVENT_MPLS_ILM_MISS
applying trap LA_EVENT_MPLS_IPV4_OVER_IPV6_EXPLICIT_NULL
applying trap LA_EVENT_MPLS_INVALID_TTL
applying trap LA_EVENT_MPLS_TE_MIDPOINT_LDP_LABELS_MISS
applying trap LA_EVENT_MPLS_ILM_VRF_LABEL_MISS
applying trap LA_EVENT_MPLS_PWE_PWACH
applying trap LA_EVENT_MPLS_VPN_TTL_ONE
applying trap LA_EVENT_MPLS_MLDP_HEADEND_COPY_SNOOP
applying trap LA_EVENT_L3_IP_UNICAST_RPF
applying trap LA_EVENT_L3_IP_MULTICAST_RPF
applying trap LA_EVENT_L3_IP_MC_DROP
applying trap LA_EVENT_L3_IP_MC_PUNT_DC_PASS
applying trap LA_EVENT_L3_IP_MC_SNOOP_DC_PASS
applying trap LA_EVENT_L3_IP_MC_SNOOP_RPF_FAIL
applying trap LA_EVENT_L3_IP_MC_PUNT_RPF_FAIL
applying trap LA_EVENT_L3_IP_MC_SNOOP_LOOKUP_MISS
applying trap LA_EVENT_L3_IP_MULTICAST_NOT_FOUND
applying trap LA_EVENT_L3_IP_MC_S_G_PUNT_MEMBER
applying trap LA_EVENT_L3_IP_MC_G_PUNT_MEMBER
applying trap LA_EVENT_L3_IP_MC_EGRESS_PUNT
applying trap LA_EVENT_L3_ISIS_OVER_L3
applying trap LA_EVENT_L3_ISIS_DRAIN
applying trap LA_EVENT_L3_NO_HBM_ACCESS_DIP
applying trap LA_EVENT_L3_NO_HBM_ACCESS_SIP
applying trap LA_EVENT_L3_LPM_ERROR
applying trap LA_EVENT_L3_LPM_DROP
applying trap LA_EVENT_L3_LOCAL_SUBNET
applying trap LA_EVENT_L3_ICMP_REDIRECT
applying trap LA_EVENT_L3_NO_LP_OVER_LAG_MAPPING
applying trap LA_EVENT_L3_INGRESS_MONITOR
applying trap LA_EVENT_L3_EGRESS_MONITOR
applying trap LA_EVENT_L3_INT_HOP_LIMIT
applying trap LA_EVENT_L3_ACL_DROP
applying trap LA_EVENT_L3_ACL_FORCE_PUNT
applying trap LA_EVENT_L3_GLEAN_ADJ
applying trap LA_EVENT_L3_DROP_ADJ
applying trap LA_EVENT_L3_DROP_ADJ_NON_INJECT
applying trap LA_EVENT_L3_NULL_ADJ
applying trap LA_EVENT_L3_USER_TRAP1
applying trap LA_EVENT_L3_USER_TRAP2
applying trap LA_EVENT_L3_LPM_DEFAULT_DROP
applying trap LA_EVENT_L3_BFD_MICRO_IP_DISABLED
applying trap LA_EVENT_L3_NO_VNI_MAPPING
applying trap LA_EVENT_L3_NO_HBM_ACCESS_OG
applying trap LA_EVENT_L3_ASBR_TABLE_MISS
applying trap LA_EVENT_L3_NO_L3_DLP_MAPPING
applying trap LA_EVENT_L3_L3_DLP_DISABLED
applying trap LA_EVENT_L3_SPLIT_HORIZON
applying trap LA_EVENT_L3_MC_SAME_INTERFACE
applying trap LA_EVENT_L3_NO_VPN_LABEL_FOUND
applying trap LA_EVENT_L3_TTL_OR_HOP_LIMIT_IS_ONE
applying trap LA_EVENT_L3_TX_MTU_FAILURE
applying trap LA_EVENT_L3_TX_FRR_DROP
applying trap LA_EVENT_L3_ENCAP_TABLE_MISS
applying trap LA_EVENT_L3_GLEAN_ACI_PROXY
applying trap LA_EVENT_L3_TUNNEL_SIP_INVALID
applying trap LA_EVENT_L3_INVALID_SPI
applying trap LA_EVENT_L3_L3_SAME_TUNNEL_INTF
applying trap LA_EVENT_L3_PACKET_FROM_TUNNEL
------- Applying all devices traps -------
## NOTE:Skipping trap LA_EVENT_ETHERNET_L2CP4, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_L2CP5, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_L2CP6, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_L2CP7, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_MACSEC, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_TEST_OAM_AC_MEP, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_TEST_OAM_AC_MIP, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_TEST_OAM_CFM_LINK_MDL0, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_SMAC_MISS, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_HOP_BY_HOP, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_IPV4_UNKNOWN_PROTOCOL, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_IPV4_OPTIONS_EXIST, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_IPV6_HOP_BY_HOP, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_IPV6_ZERO_PAYLOAD, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_L3_USER_TRAP1, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_L3_USER_TRAP2, Verify this is intended !! ##
***============================================================***
***=========== Dump la_objects scale for device: 0  ===========***
***============================================================***
la_object TYPE                                Count
------------------------------------------  -------
object_type_e_ACL_COMMAND_PROFILE                 1
object_type_e_ACL_KEY_PROFILE                    10
object_type_e_AC_PROFILE                          1
object_type_e_COUNTER_SET                       151
object_type_e_DEVICE                              1
object_type_e_EGRESS_QOS_PROFILE                  1
object_type_e_ELEPHANT_FLOW_HANDLER               1
object_type_e_ETHERNET_PORT                       3
object_type_e_FILTER_GROUP                        1
object_type_e_FLOW_CACHE_HANDLER                  1
object_type_e_FORUS_DESTINATION                   1
object_type_e_HBM_HANDLER                         1
object_type_e_IFG_SCHEDULER                      12
object_type_e_INGRESS_QOS_PROFILE                 1
object_type_e_INTERFACE_SCHEDULER                23
object_type_e_ITC_OSTC_PROFILE                  144
object_type_e_LED_INTERFACE_HANDLER               1
object_type_e_LOGICAL_PORT_SCHEDULER             15
object_type_e_LSR                                 1
object_type_e_MAC_PORT                            3
object_type_e_METER_ACTION_PROFILE                1
object_type_e_METER_PROFILE                       2
object_type_e_NEXT_HOP                            1
object_type_e_NPU_HOST_PORT                       8
object_type_e_OUTPUT_QUEUE_SCHEDULER            144
object_type_e_PCI_PORT                            6
object_type_e_PTP_HANDLER                         1
object_type_e_PUNT_INJECT_PORT                    6
object_type_e_RECYCLE_PORT                        6
object_type_e_RX_CGM_SQ_PROFILE                   1
object_type_e_SYSTEM_PORT                        15
object_type_e_SYSTEM_PORT_SCHEDULER              15
object_type_e_TC_PROFILE                          2
object_type_e_THROUGHPUT_MEASURING_UTILITY        1
object_type_e_UNIFIED_STATE_DUMP_MANAGER          1
object_type_e_VOQ_CGM_EVICTED_PROFILE             1
object_type_e_VOQ_CGM_PROFILE                     3
object_type_e_VOQ_SET                            21
***============================================================***
***=============================  =============================***
***============================================================***
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV4, EGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, EGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV4, EGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, EGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created ETHERNET, INGRESS ACL - TCAM: E_0
--- ACLS --- Created L2 Ingress security ACL
--- ACLS --- Created ETHERNET, INGRESS ACL - TCAM: E_0
--- ACLS --- Created L2 Ingress QOS ACL
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_1
--- ACLS --- Created IPV4, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, INGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV4, EGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created IPV6, EGRESS ACL - TCAM: E_0_AND_1
--- ACLS --- Created ETHERNET, INGRESS ACL - TCAM: E_0
--- ACLS --- Created L2 Ingress security ACL
--- ACLS --- Created ETHERNET, INGRESS ACL - TCAM: E_0
--- ACLS --- Created L2 Ingress QOS ACL
--- ACLS --- Created ETHERNET, INGRESS ACL - TCAM: E_0
--- ACLS --- Created L2 Ingress security ACL
--- ACLS --- Created ETHERNET, INGRESS ACL - TCAM: E_0
--- ACLS --- Created L2 Ingress QOS ACL
--- get_no_drop_rate --- 99.99% (expected_npu_utilization: 99.99, pkt_size: 10000)
PFC test, packet size = 10000, in rate = 99.990000, stream_type = single1
***============================================================***
***=================== PRINTING TEST PARAMS ===================***
***============================================================***
=== GENERAL PARAMS ===
{   'apply_reinit_after_current_test_in_this_group': False,
    'apply_reinit_after_last_test_in_the_group': False,
    'apply_warm_boot': False,
    'common_params': {'ifg_logging_mode': False, 'te_speed_factor': 1},
    'ifg_logging_mode': False,
    'sdk_logging_levels': [8],
    'sdk_logging_type': {<enum 'SdkLoggingType'>: 'NONE'}}
=== INJECT_PARAMS ===
{   'base_pkt_size': 10000,
    'common_params': {'ifg_logging_mode': False, 'te_speed_factor': 1},
    'imix_packet_size': False,
    'inject_checksum_error': False,
    'inject_checksum_error_streams': [0],
    'inject_mpps_rate': None,
    'max_inject_rate': 99.99,
    'packet_limit': 0,
    'pause_rate_ratio': 0,
    'payload_type_per_stream': {},
    'per_stream_inject_rate_ratio': array([1.]),
    'per_stream_inject_rate_weights': [1],
    'rand_range': [0, 300],
    'randomize_packet_size': False}
=== TRAFFIC_PATTERN_PARAMS ===
{   'additional_streams_per_application': 0,
    'allow_flows_per_stream': False,
    'app_list': ['UC_Bridge_P2P'],
    'bridge': {   'add_additional_inner_headers': False,
                  'egress_acl_mode': [<AclType.NONE: 0>],
                  'fwd_model_type': {<enum 'BridgeFwdModelType'>: 'RELAY'},
                  'ingress_acl_mode': [<AclType.NONE: 0>],
                  'mac_learning_type': {<enum 'MacLearningType'>: 'NONE'},
                  'resolution_lb_level': {<enum 'ResolutionLbLevel'>: 'LevelNone'},
                  'vlan_enable': True,
                  'vlan_sub_type': None},
    'common_params': {'ifg_logging_mode': False, 'te_speed_factor': 1},
    'compact_acl': False,
    'customize_en': False,
    'exact_metering_params': {},
    'first_snake_type': {<enum 'SnakeType'>: 'SAME_SLICE'},
    'first_stream_tc': 0,
    'ingress_acl_sequence_params': {},
    'ip': {   'add_additional_inner_headers': False,
              'egress_acl_mode': {<enum 'AclType'>: 'NONE'},
              'fwd_model_type': {<enum 'IpFwdModelType'>: 'NH'},
              'ingress_acl_mode': {<enum 'AclType'>: 'NONE'},
              'is_IPv4': True,
              'l4_inner_header_type': {<enum 'L4InnerHeaderType'>: 'NONE'},
              'mc_config_db': {<enum 'IpMCConfigDB'>: 'VRF_G'},
              'mc_group_sharing': True,
              'resolution_lb_level': {<enum 'ResolutionLbLevel'>: 'LevelNone'},
              'rpf_mode': {<enum 'RpfMode'>: 'NONE'},
              'v4_prefix_length': 24,
              'v6_prefix_length': 24,
              'vlan_sub_type': None,
              'vrf_global': False},
    'ip_over_mpls': {   'ecmp_resolution_level': {<enum 'ResolutionLbLevel'>: 'Level1'},
                        'egress_acl_mode': {<enum 'AclType'>: 'NONE'},
                        'enable_tx_oversubscription': False,
                        'fwd_model_type': {<enum 'IpOvrMplsFwdModelType'>: 'IP6PE'},
                        'ingress_acl_mode': {<enum 'AclType'>: 'NONE'},
                        'is_IPv4': False,
                        'rpf_mode': {<enum 'RpfMode'>: 'NONE'},
                        'v4_prefix_length': 24,
                        'v6_prefix_length': 24,
                        'vlan_sub_type': None},
    'ip_svi': {   'egress_acl_mode': [<AclType.NONE: 0>],
                  'fwd_model_type': {<enum 'IpFwdModelType'>: 'NH'},
                  'ingress_acl_mode': [<AclType.NONE: 0>],
                  'is_IPv4': True,
                  'v4_prefix_length': 24,
                  'v6_prefix_length': 24,
                  'vlan_sub_type': None},
    'ip_tunnel': {   'egress_acl_mode': [<AclType.NONE: 0>],
                     'fwd_model_type': {<enum 'IpTunnelFwdModelType'>: 'NONE'},
                     'ingress_acl_mode': [<AclType.NONE: 0>],
                     'vlan_sub_type': None},
    'is_capture': False,
    'max_num_of_rounds': 1,
    'metering_enable': False,
    'mpls': {   'egress_acl_mode': [<AclType.NONE: 0>],
                'fwd_model_type': {<enum 'MPLSFwdModelType'>: 'Default'},
                'ingress_acl_mode': [<AclType.NONE: 0>],
                'vlan_sub_type': None},
    'num_of_flows_per_stream': 1,
    'num_of_snake_groups': 1,
    'num_of_snake_types': 1,
    'num_of_streams_per_application': 1,
    'num_of_sub_flows': 0,
    'num_of_tg_ports': 1,
    'num_of_traffic_classes': 1,
    'number_of_voqs_to_evict': 2,
    'per_snake_params': {   'app_name': '',
                            'egress_counters_enable': True,
                            'force_address': None,
                            'force_vrf': None,
                            'ingress_counters_enable': True,
                            'priority': 0,
                            'snake_group': 0,
                            'snake_ports_list': (),
                            'snake_type': {<enum 'SnakeType'>: 'SAME_SLICE'},
                            'stream_num': 0,
                            'stream_weight': 1,
                            'traffic_class': 0},
    'per_stream_force_addresses': {},
    'per_stream_force_vrf': {},
    'per_stream_priority_setting': {},
    'snake_types_list': [],
    'total_number_of_streams': 1,
    'udc': {   'egress_acl_mode': [<AclType.NONE: 0>],
               'fwd_model_type': {<enum 'UDCFwdModelType'>: 'nop'},
               'ingress_acl_mode': [<AclType.NONE: 0>],
               'vlan_sub_type': None},
    'udc_db_access': {   'access_cem': False,
                         'egress_acl_mode': [<AclType.NONE: 0>],
                         'fwd_db_access_bitmap': [],
                         'fwd_db_access_key_indexes': [0, 0, 0, 0],
                         'fwd_model_type': {<enum 'UDCFwdModelType'>: 'nop'},
                         'hcam_join': 0,
                         'hcam_key': 0,
                         'ingress_acl_mode': [<AclType.NONE: 0>],
                         'num_of_ene_instructions': [],
                         'num_of_macros_at_fwd_npe': [],
                         'num_of_macros_at_term_npe': [],
                         'num_of_macros_at_trans_npe': [],
                         'skip_lpm_dist_config': False,
                         'splitter_default_action': 1,
                         'term_db_access_bitmap': [],
                         'trans_db_access_bitmap': [],
                         'vlan_sub_type': None},
    'vxlan': {   'egress_acl_mode': [<AclType.NONE: 0>],
                 'enable_rx_oversubscription': False,
                 'fwd_model_type': {<enum 'VxLANFwdModelType'>: 'Bridge'},
                 'ingress_acl_mode': [<AclType.NONE: 0>],
                 'mac_learning_type': {<enum 'MacLearningType'>: 'NONE'},
                 'v4_prefix_length': 24,
                 'vlan_sub_type': None}}
=== PRE_CONFIG_PARAMS ===
{   'common_params': {'ifg_logging_mode': False, 'te_speed_factor': 1},
    'npu': {'cem_oversubscription_mode': False, 'central_database_banks_mode': {<enum 'CdbBanksMode'>: 'SYMMETRIC_LPM_CEM'}},
    'tm': {'todo': True}}
=== POST_CONFIG_PARAMS ===
{   'common_params': {'ifg_logging_mode': False, 'te_speed_factor': 1},
    'lm': {'set_lm_read_counters': False},
    'npu': {   'disable_flc_verifier': False,
               'disable_lpm_cache_activity_deletes': False,
               'disable_lpm_cache_aging_deletes': False,
               'disabled_traps_list': [],
               'enable_mac_aging': False,
               'flc_em_cam_extreme_threshold': False,
               'flc_em_hash_seed_zero': False,
               'flow_cache_enable': False,
               'force_fi_mode': {<enum 'ForceFiMode'>: 'NONE'},
               'force_flc_delete_activity': False,
               'force_flc_delete_aging': False,
               'force_flc_delete_random': False,
               'force_flc_delete_ser': False,
               'force_internal_lpm_cache_mode': {<enum 'CdbCacheMode'>: 'BOTH_ENABLE'},
               'force_lpm_rebalance': True,
               'force_lpm_tcam_or_em_mode': {<enum 'LpmEntriesForceCachingMode'>: 'NONE'},
               'ifgb_packet_shaper_force_mode': {<enum 'ForceIfgbPacketShaper'>: 'NONE'},
               'ifgb_packet_shaper_force_val': 95,
               'internal_lpm_cache_tcam_mode': {<enum 'LpmCacheTcamMode'>: 'SDK_DEFAULT'},
               'lpm_hbm_percentage': 0,
               'mac_aging_interval': 5,
               'mac_learning_device_mode': {<enum 'MacLearningDeviceMode'>: 'LOCAL_CDB_ONLY'},
               'reassembly_packet_shaper_force_mode': {<enum 'ForceReassemblyPacketShaper'>: 'NONE'},
               'reassembly_packet_shaper_force_val': 95,
               'rxpp_packet_shaper_force_mode': {<enum 'ForceRxppPacketShaper'>: 'NONE'},
               'rxpp_packet_shaper_force_val': 95,
               'set_cdb_cache_extreme_params': False,
               'set_flc_delete_activity_val': 25,
               'set_flc_delete_aging_val': 500000,
               'set_flc_delete_random_val': 1,
               'set_trap_destination': {<enum 'TrapDest'>: 'Drop'}},
    'tm': {'force_fabric': False, 'todo': True},
    'warm_boot': {'current_test_item': None, 'current_test_name': '', 'device_state_path': '', 'dta_num_of_steps': 2, 'perform_warm_                                                                  boot': False}}
=== SDK_TEMP_FIXES_PARAMS ===
{'common_params': {'ifg_logging_mode': False, 'te_speed_factor': 1}, 'force_lpm_rebalance': True}
=== END_OF_TEST_PARAMS ===
{   'adjust_line_rate_allow_drops': True,
    'allow_fwd_lookup_errors_drops': False,
    'allow_ifgb_drops': False,
    'allow_ostc_drops': False,
    'allow_pdvoq_drops': True,
    'allowed_traps': [197, 0],
    'check_flow_cache_hit_miss_counters': False,
    'check_lb_distribution': False,
    'check_logical_ports_counters': False,
    'check_metering': False,
    'check_per_stream_misordered_errors': True,
    'check_per_stream_payload_errors': True,
    'check_per_stream_rx_equal_0': True,
    'check_per_stream_rx_equal_tx': False,
    'check_port_rate_bps': False,
    'check_queue_rate_bps': False,
    'check_rate_bps': False,
    'check_rate_pps': False,
    'check_rx_equal_tx': False,
    'check_test_payload': False,
    'check_traffic_received_to_te': True,
    'check_traps': True,
    'check_voq_counters': False,
    'common_params': {'ifg_logging_mode': False, 'te_speed_factor': 1},
    'detail_level': 'heavy',
    'exp_err_stream_l': [],
    'expected_max_tolerance_tx_bps': 1,
    'expected_minimum_rx_div_tx_pps': 1,
    'expected_minimum_rx_packets': 1,
    'expected_minimum_tx_packets': 1,
    'expected_num_of_active_streams': 1,
    'expected_port_min_chk_en': [   0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0, 0, 0, 0, 0, 0, 0,
                                    0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0, 0, 0, 0, 0, 0, 0,
                                    0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0, 0, 0, 0, 0, 0, 0,
                                    0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0, 0, 0, 0, 0, 0, 0,
                                    0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0, 0, 0, 0, 0, 0, 0,
                                    0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0, 0, 0, 0, 0, 0, 0,
                                    0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0, 0, 0, 0, 0, 0, 0,
                                    0],
    'expected_port_rate_bps': [   0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0, 0, 0, 0, 0, 0, 0,
                                  0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0, 0, 0, 0, 0, 0, 0,
                                  0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0, 0, 0, 0, 0, 0, 0,
                                  0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0, 0, 0, 0, 0, 0, 0,
                                  0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0, 0, 0, 0, 0, 0, 0,
                                  0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0, 0, 0, 0, 0, 0, 0,
                                  0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,                                                                   0, 0, 0],
    'expected_queue_rate_bps': [0, 0, 0, 0, 0, 0, 0, 0],
    'expected_rate_per_metering_flow': 0,
    'ifg_exp_ostc_drops_ports': {},
    'ifg_exp_ostc_full_drops_only': False,
    'ifg_skip_port_chk_l': [],
    'ifg_skip_te_chk': False,
    'ignore_intr_l': ['ifg_interrupt_summary', 'rsf_rx_degraded_ser_interrupt_register', 'rx_pma_sig_ok_loss_interrupt_register', 'r                                                                  x_link_status_down'],
    'imix_packet_size': False,
    'lb_vector_permutations_amount': 1,
    'llfc_checker_enable': False,
    'max_expected_dropped_packets': 0,
    'max_per_stream_misordered_errors': 0,
    'meter_rate_results': None,
    'npu_end_of_test_params': {   'check_flc_cache_occ_wmk': False,
                                  'check_flc_ongoing_deletes': False,
                                  'check_flc_ongoing_hits': False,
                                  'check_flc_total_dont_use_cache': False,
                                  'check_learn_updates': False,
                                  'check_lpm_cache_em_cam_entries': True,
                                  'check_lpm_cache_tcam_flush': True,
                                  'check_lri_counter': False,
                                  'check_mac_age_table': False,
                                  'check_mac_aging': False,
                                  'check_new_learns': False,
                                  'expected_learn_updates': 0,
                                  'expected_lri_counter': 0,
                                  'expected_new_learns': 0,
                                  'print_tx_counters_read_responses': False,
                                  'set_flc_cache_occ_max_val': 12288,
                                  'validate_cem_cores_full_occupancy': False},
    'num_of_lb_eligible_ports': 0,
    'ostc_counter': None,
    'pass_ratio_hp': {},
    'per_test_expected_result_type': {<enum 'PerTestResultType'>: 'ExpectedPass'},
    'performance_envelope_baseline': False,
    'pfc_checker_tc': 0,
    'pfc_hbm_congestion_test_checker_enable': False,
    'pfc_snake_test_checker_enable': True,
    'pkt_size': 10000,
    'pkt_validation_params': {   'compare_payload_content': False,
                                 'compare_payload_size': False,
                                 'mirror_port_index': 0,
                                 'num_pkts_to_validate': 100,
                                 'pkt_validator': None,
                                 'validate_captured_pkts': False},
    'print_mac_port_counters': True,
    'print_streams_stats': True,
    'run_cpu_pkts_extraction': False,
    'run_npu_end_of_test': True,
    'run_validation_end_of_test': True,
    'show_cpu_trapped_packets': 0,
    'show_last_packets': 0,
    'skip_acl_counters_check': False,
    'skip_ifg_eot_checks': True,
    'streams_for_validation': [],
    'user_defined_checker': None,
    'user_defined_per_stream_stats': {},
    'warm_boot_checker_params': {   'during_action_results': {},
                                    'end_of_test_check': False,
                                    'max_wb_latency': 30,
                                    'sdk_objects': None,
                                    'tgen_orig_paused_ports_config': [],
                                    'wb_execution_time': 0}}
***============================================================***
***===================== APPLY PRE-CONFIG =====================***
***============================================================***
--> Done
***============================================================***
***===================== CREATING SNAKES  =====================***
***============================================================***
===> MM: [DEBUG] snake_params: num_of_snake_types=1, first_snake_type.value:0, per_type_next_tc:[0]
---> Creating snake stream[0] - application is: UC_Bridge_P2P, using snake_group[0], SnakeType.SAME_SLICE (0), num of flows in this                                                                   stream: 1, traffic class: 0
ports {0: {0: {'slice': 0, 'pif': 0, 'ifg': 0}, 2: {'slice': 0, 'pif': 2, 'ifg': 0}, 238: {'slice': 2, 'pif': 8, 'ifg': 1}}}
 loops: ['0:0', '0:2']
get_snake_according_to_rate:
 Full pair_list (before truncating):
 [((0, 238), (0, 2)), ((0, 2), (0, 0)), ((0, 0), (0, 238))]

--- Resource Manager --- Allocate new L2_AC BASE element, idx = 106495
--- Resource Manager --- Allocate new L2_AC BASE element, idx = 106494
--- Resource Manager --- Allocate new L2_AC BASE element, idx = 106493
--- Resource Manager --- Allocate new L2_AC BASE element, idx = 106492
--- Resource Manager --- Allocate new L2_AC BASE element, idx = 106491
--- Resource Manager --- Allocate new L2_AC BASE element, idx = 106490
***============================================================***
***=================== APPLY SDK-TEMP-FIXES ===================***
***============================================================***
Performing LPM rebalance x32 times (Occupancy load balancing alghorithm is still not mature enough yet, Rate load balancing is not y                                                                  et implemented)
--> Done
***============================================================***
***================= CONFIGURING TRAFFIC GEN  =================***
***============================================================***
--- NOTIFICATION HANDLER --- : Adding LINK, link_status: DOWN, port_id: None, type: None to ignore list - expected number of interru                                                                  pts in range: [None,None]
Send()         : 0/1 P_CHECKSUM ?
Send() received: 0/1  P_CHECKSUM  OFF
SendExpect(<OK>): 0/1 PP_FECMODE ON
SendExpect(<OK>): 0/1 P_RESET
SendExpect(<OK>): 0/1 P_CHECKSUM 0
--> Configuring TE: stream[0], base_pkt_size: 10000[B], inject_rate_percentage: 99.99%, number of modifiers: 0
  Inject packet's header (before modifiers!) is: b'10ff8018000014ff8018000081000208ffff'
SendExpect(<OK>): 0/1 PS_CREATE [0]
SendExpect(<OK>): 0/1 PS_PAYLOAD [0] RANDOM
SendExpect(<OK>): 0/1 PS_TPLDID [0] 0
SendExpect(<OK>): 0/1 PS_PACKETLENGTH [0] FIXED 10000 10000
[('Ethernet', '0x10ff8018000014ff801800008100'), ('VLAN', '0x0208ffff')]
SendExpect(<OK>): 0/1 PS_HEADERPROTOCOL [0] Ethernet
SendExpect(<OK>): 0/1 PS_PACKETHEADER [0] 0x10ff8018000014ff801800008100
SendExpect(<OK>): 0/1 PS_HEADERPROTOCOL [0] Ethernet VLAN
SendExpect(<OK>): 0/1 PS_PACKETHEADER [0] 0x10ff8018000014ff8018000081000208ffff
SendExpect(<OK>): 0/1 PS_RATEFRACTION [0] 999900
SendExpect(<OK>): 0/1 PS_ENABLE [0] ON
SendExpect(<OK>): 0/1 P_CHECKSUM 18
SendExpect(<OK>): 0/1 PS_MODIFIERCOUNT [0] 0
SendExpect(<OK>): 0/1 PS_MODIFIEREXTCOUNT [0] 0
SendExpect(<OK>): 0/1 PT_CLEAR
SendExpect(<OK>): 0/1 PR_CLEAR
--- NOTIFICATION HANDLER --- : Removing LINK, link_status: DOWN, port_id: None, type: None from ignore list
***============================================================***
***==================== APPLY POST-CONFIG  ====================***
***============================================================***
===> MM: IFG Interrupts Cleared
Setting splitter cache mode to enable on slice[0]
Setting splitter cache mode to enable on slice[1]
Setting splitter cache mode to enable on slice[2]
Setting splitter cache mode to enable on slice[3]
Setting splitter cache mode to enable on slice[4]
Setting splitter cache mode to enable on slice[5]
Setting lpm cache mode to enable on slice[0]
Setting lpm cache mode to enable on slice[1]
Setting lpm cache mode to enable on slice[2]
Setting lpm cache mode to enable on slice[3]
Setting lpm cache mode to enable on slice[4]
Setting lpm cache mode to enable on slice[5]
=== TM POST CONFIG: PFC SNAKE TEST ===
PFC enabled ports list = [238, 0]
set port shaper: slice 2, ifg 1, port 8, rate 69
--> Done
***============================================================***
***================= APPLY PRE-TRAFFIC TASKS  =================***
***============================================================***
***============================================================***
***=========== Dump la_objects scale for device: 0  ===========***
***============================================================***
Dumping only la_devices created for current test (diff from start of test)
For the base la_objects scales please see logging at start of test
la_object TYPE                   Count
-----------------------------  -------
object_type_e_ACL                   84
object_type_e_COUNTER_SET           12
object_type_e_L2_SERVICE_PORT        6
***============================================================***
***=============================  =============================***
***============================================================***
Starting debugger before traffic...

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>> PDB set_trace >>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
> /big_share2/pacific/user/yaliuliu/sdkmas/fishnet/tests/fwd_base_test.py(506)_run_test()
-> te.start_all_traffic()
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb)
(Pdb) get_counters()
INFO  ___________________Slice0_____________________|____________Slice1___________|___________Slice2____________|___________Slice3__                                                                  __________|___________Slice4____________|_____________Slice5___________|
INFO  IFG_RX0 packets          =               0    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =                                                                                 0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFG_RX1 packets          =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =                                                                                 0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  IFG_RX0 bytes            =      2998843328    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =                                                                                 0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFG_RX1 bytes            =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =                                                                                 0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  IFG_RX0 flow control     =        46856927    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =                                                                                 0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFG_RX1 flow control     =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =                                                                                 0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  IFGB_RX0 packets         =               0    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =                                                                                 0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFGB_RX1 packets         =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =                                                                                 0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  RXPP IFG0 input packets  =               0    |RXPP2   =               0    |RXPP4   =               0    |RXPP6   =                                                                                 0    |RXPP8   =               0    |RXPP10   =               0    |
INFO  RXPP IFG1 input packets  =               0    |RXPP3   =               0    |RXPP5   =               0    |RXPP7   =                                                                                 0    |RXPP9   =               0    |RXPP11   =               0    |
INFO  RXPP IFG0 output packets =               0    |RXPP2   =               0    |RXPP4   =               0    |RXPP6   =                                                                                 0    |RXPP8   =               0    |RXPP10   =               0    |
INFO  RXPP IFG1 output packets =               0    |RXPP3   =               0    |RXPP5   =               0    |RXPP7   =                                                                                 0    |RXPP9   =               0    |RXPP11   =               0    |
INFO  SMS IFG0 write packets   =               0    |SMS2    =               0    |SMS4    =               0    |SMS6    =               0    |SMS8    =               0    |SMS 10   =               0    |
INFO  SMS IFG1 write packets   =               0    |SMS3    =               0    |SMS5    =               0    |SMS7    =               0    |SMS9    =               0    |SMS 11   =               0    |
INFO  REASSEMBLY Slc0 packets  =               0    |REAS1   =               0    |REAS2   =               0    |REAS3   =               0    |REAS4   =               0    |REAS5    =               0    |
INFO  PDVOQ Slice0 packets     =               0    |PDVOQ1  =               0    |PDVOQ2  =               0    |PDVOQ3  =               0    |PDVOQ4  =               0    |PDVOQ5   =               0    |
INFO  PDVOQ Slice0 bytes       =               0    |PDVOQ1  =               0    |PDVOQ2  =               0    |PDVOQ3  =               0    |PDVOQ4  =               0    |PDVOQ5   =               0    |
INFO  FILB Slice0 packets      =               0    |FILB1   =               0    |FILB2   =               0    |FILB3   =               0    |FILB4   =               0    |FILB5    =               0    |
INFO  FILB Slice0 bytes        =               0    |FILB1   =               0    |FILB2   =               0    |FILB3   =               0    |FILB4   =               0    |FILB5    =               0    |
INFO  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX--C--R--O--S--S--XXXXXXXXXX--B--A--R--XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX|
INFO  TXPDR Slice0 packets     =               0    |TXPDR1  =               0    |TXPDR2  =               0    |TXPDR3  =               0    |TXPDR4  =               0    |TXPDR5   =               0    |
INFO  TXCGM Slice0 packets     =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 bytes       =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 UC packets  =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 MC packets  =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  SMS IFG0 read packets    =               0    |SMS2    =               0    |SMS4    =               0    |SMS6    =               0    |SMS8    =               0    |SMS 10   =               0    |
INFO  SMS IFG1 read packets    =               0    |SMS3    =               0    |SMS5    =               0    |SMS7    =               0    |SMS9    =               0    |SMS 11   =               0    |
INFO  TXPP0 packets            =               0    |TXPP2   =               0    |TXPP4   =               0    |TXPP6   =               0    |TXPP8   =               0    |TXPP10   =               0    |
INFO  TXPP1 packets            =               0    |TXPP3   =               0    |TXPP5   =               0    |TXPP7   =               0    |TXPP9   =               0    |TXPP11   =               0    |
^[[AINFO  IFGB_TX0 packets         =               0    |IFGB2   =               0    |IFGB4   =               0    |IFGB6   =               0    |IFGB8   =               0    |IFGB10   =               0    |
INFO  IFGB_TX1 packets         =               0    |IFGB3   =               0    |IFGB5   =               0    |IFGB7   =               0    |IFGB9   =               0    |IFGB11   =               0    |
INFO  IFG_TX0 good packets     =               0    |IFG_TX2 =               0    |IFG_TX4 =               0    |IFG_TX6 =               0    |IFG_TX8 =               0    |IFG_TX10 =               0    |
INFO  IFG_TX1 good packets     =               0    |IFG_TX3 =               0    |IFG_TX5 =               0    |IFG_TX7 =               0    |IFG_TX9 =               0    |IFG_TX11 =               0    |
INFO  IFG_TX0 good bytes       =      2998843328    |IFG_TX2 =               0    |IFG_TX4 =               0    |IFG_TX6 =               0    |IFG_TX8 =               0    |IFG_TX10 =               0    |
INFO  IFG_TX1 good bytes       =               0    |IFG_TX3 =               0    |IFG_TX5 =      1499505408    |IFG_TX7 =               0    |IFG_TX9 =               0    |IFG_TX11 =               0    |
INFO  IFG_TX0 flow control     =        46856927    |IFG_TX2 =               0    |IFG_TX4 =               0    |IFG_TX6 =               0    |IFG_TX8 =               0    |IFG_TX10 =               0    |
INFO  IFG_TX1 flow control     =               0    |IFG_TX3 =               0    |IFG_TX5 =        23429772    |IFG_TX7 =               0    |IFG_TX9 =               0    |IFG_TX11 =               0    |
INFO  (*) = counter overflow
(Pdb) get_counters()
INFO  ___________________Slice0_____________________|____________Slice1___________|___________Slice2____________|___________Slice3____________|___________Slice4____________|_____________Slice5___________|
INFO  IFG_RX0 packets          =               0    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =               0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFG_RX1 packets          =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =               0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  IFG_RX0 bytes            =         6801792    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =               0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFG_RX1 bytes            =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =               0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  IFG_RX0 flow control     =          106278    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =               0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFG_RX1 flow control     =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =               0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  IFGB_RX0 packets         =               0    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =               0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFGB_RX1 packets         =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =               0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  RXPP IFG0 input packets  =               0    |RXPP2   =               0    |RXPP4   =               0    |RXPP6   =               0    |RXPP8   =               0    |RXPP10   =               0    |
INFO  RXPP IFG1 input packets  =               0    |RXPP3   =               0    |RXPP5   =               0    |RXPP7   =               0    |RXPP9   =               0    |RXPP11   =               0    |
INFO  RXPP IFG0 output packets =               0    |RXPP2   =               0    |RXPP4   =               0    |RXPP6   =               0    |RXPP8   =               0    |RXPP10   =               0    |
INFO  RXPP IFG1 output packets =               0    |RXPP3   =               0    |RXPP5   =               0    |RXPP7   =               0    |RXPP9   =               0    |RXPP11   =               0    |
INFO  SMS IFG0 write packets   =               0    |SMS2    =               0    |SMS4    =               0    |SMS6    =               0    |SMS8    =               0    |SMS 10   =               0    |
INFO  SMS IFG1 write packets   =               0    |SMS3    =               0    |SMS5    =               0    |SMS7    =               0    |SMS9    =               0    |SMS 11   =               0    |
INFO  REASSEMBLY Slc0 packets  =               0    |REAS1   =               0    |REAS2   =               0    |REAS3   =               0    |REAS4   =               0    |REAS5    =               0    |
INFO  PDVOQ Slice0 packets     =               0    |PDVOQ1  =               0    |PDVOQ2  =               0    |PDVOQ3  =               0    |PDVOQ4  =               0    |PDVOQ5   =               0    |
INFO  PDVOQ Slice0 bytes       =               0    |PDVOQ1  =               0    |PDVOQ2  =               0    |PDVOQ3  =               0    |PDVOQ4  =               0    |PDVOQ5   =               0    |
INFO  FILB Slice0 packets      =               0    |FILB1   =               0    |FILB2   =               0    |FILB3   =               0    |FILB4   =               0    |FILB5    =               0    |
INFO  FILB Slice0 bytes        =               0    |FILB1   =               0    |FILB2   =               0    |FILB3   =               0    |FILB4   =               0    |FILB5    =               0    |
INFO  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX--C--R--O--S--S--XXXXXXXXXX--B--A--R--XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX|
INFO  TXPDR Slice0 packets     =               0    |TXPDR1  =               0    |TXPDR2  =               0    |TXPDR3  =               0    |TXPDR4  =               0    |TXPDR5   =               0    |
INFO  TXCGM Slice0 packets     =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 bytes       =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 UC packets  =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 MC packets  =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  SMS IFG0 read packets    =               0    |SMS2    =               0    |SMS4    =               0    |SMS6    =               0    |SMS8    =               0    |SMS 10   =               0    |
INFO  SMS IFG1 read packets    =               0    |SMS3    =               0    |SMS5    =               0    |SMS7    =               0    |SMS9    =               0    |SMS 11   =               0    |
INFO  TXPP0 packets            =               0    |TXPP2   =               0    |TXPP4   =               0    |TXPP6   =               0    |TXPP8   =               0    |TXPP10   =               0    |
INFO  TXPP1 packets            =               0    |TXPP3   =               0    |TXPP5   =               0    |TXPP7   =               0    |TXPP9   =               0    |TXPP11   =               0    |
INFO  IFGB_TX0 packets         =               0    |IFGB2   =               0    |IFGB4   =               0    |IFGB6   =               0    |IFGB8   =               0    |IFGB10   =               0    |
INFO  IFGB_TX1 packets         =               0    |IFGB3   =               0    |IFGB5   =               0    |IFGB7   =               0    |IFGB9   =               0    |IFGB11   =               0    |
INFO  IFG_TX0 good packets     =               0    |IFG_TX2 =               0    |IFG_TX4 =               0    |IFG_TX6 =               0    |IFG_TX8 =               0    |IFG_TX10 =               0    |
INFO  IFG_TX1 good packets     =               0    |IFG_TX3 =               0    |IFG_TX5 =               0    |IFG_TX7 =               0    |IFG_TX9 =               0    |IFG_TX11 =               0    |
INFO  IFG_TX0 good bytes       =         6801792    |IFG_TX2 =               0    |IFG_TX4 =               0    |IFG_TX6 =               0    |IFG_TX8 =               0    |IFG_TX10 =               0    |
INFO  IFG_TX1 good bytes       =               0    |IFG_TX3 =               0    |IFG_TX5 =         3394112    |IFG_TX7 =               0    |IFG_TX9 =               0    |IFG_TX11 =               0    |
INFO  IFG_TX0 flow control     =          106278    |IFG_TX2 =               0    |IFG_TX4 =               0    |IFG_TX6 =               0    |IFG_TX8 =               0    |IFG_TX10 =               0    |
INFO  IFG_TX1 flow control     =               0    |IFG_TX3 =               0    |IFG_TX5 =           53033    |IFG_TX7 =               0    |IFG_TX9 =               0    |IFG_TX11 =               0    |
INFO  (*) = counter overflow
(Pdb) mac_port
*** NameError: name 'mac_port' is not defined
(Pdb) mp0 = la_device.get_mac_port(2,1,0)
*** NameError: name 'la_device' is not defined
(Pdb) debug_device.read_register(gibraltar_tree.slice[4].ifg[1].ifgb.fc_cfg0)
*** NameError: name 'debug_device' is not defined
(Pdb) import sys
(Pdb) import os
(Pdb) sys.LEABA_SDK_PATH = os.getenv('LEABA_SDK_PATH', '')
(Pdb) from leaba_val import *
(Pdb) import npu_scripts
(Pdb) from npu_scripts import *
(Pdb) set_dev(self.device)
*** AttributeError: 'TestSaPfcHBM__UcBridgeP2P' object has no attribute 'device'
(Pdb) npu_sc
<npu_scripts.npu_scripts object at 0x7ff48dbbc668>
(Pdb) debug_device.read_register(gibraltar_tree.slice[4].ifg[1].ifgb.fc_cfg0)
periodic_int_en [23:0] = 0x0ffffff

(Pdb) debug_device.read_register(gibraltar_tree.slice[2].ifg[1].ifgb.fc_cfg0)
periodic_int_en [23:0] = 0x0ffffff

(Pdb) debug_device.read_register(gibraltar_tree.slice[0].ifg[1].ifgb.fc_cfg0)
periodic_int_en [23:0] = 0x0ffffff

(Pdb) npu_sc.print_npe_counters_table()
+----------------------------------------------------------------------------------------------------------------------------------------+
|                                                           NPE COUNTERS TABLE                                                           |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|          |s0-in|s0-out|s0-loop|s1-in|s1-out|s1-loop|s2-in|s2-out|s2-loop|s3-in|s3-out|s3-loop|s4-in|s4-out|s4-loop|s5-in|s5-out|s5-loop|
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
| NPU-Host |  0  |  0   |   0   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Term-NPE-0|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Term-NPE-1|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Term-NPE-2|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Fwd-NPE-0 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Fwd-NPE-1 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Fwd-NPE-2 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
| Tx-NPE-0 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
| Tx-NPE-1 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
(Pdb) npu_sc.print_npe_counters_table()
+----------------------------------------------------------------------------------------------------------------------------------------+
|                                                           NPE COUNTERS TABLE                                                           |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|          |s0-in|s0-out|s0-loop|s1-in|s1-out|s1-loop|s2-in|s2-out|s2-loop|s3-in|s3-out|s3-loop|s4-in|s4-out|s4-loop|s5-in|s5-out|s5-loop|
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
| NPU-Host |  0  |  0   |   0   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Term-NPE-0|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Term-NPE-1|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Term-NPE-2|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Fwd-NPE-0 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Fwd-NPE-1 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
|Fwd-NPE-2 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
| Tx-NPE-0 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
| Tx-NPE-1 |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+-----+------+-------+
(Pdb) debug_device.read_register(gibraltar_tree.slice[2].ifg[1].ifgb.fc_cfg0)
periodic_int_en [23:0] = 0x0ffffff

(Pdb) get_counters()
INFO  ___________________Slice0_____________________|____________Slice1___________|___________Slice2____________|___________Slice3____________|___________Slice4____________|_____________Slice5___________|

INFO  IFG_RX0 packets          =               0    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =               0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFG_RX1 packets          =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =               0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  IFG_RX0 bytes            =       308636352    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =               0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFG_RX1 bytes            =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =               0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  IFG_RX0 flow control     =         4822443    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =               0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFG_RX1 flow control     =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =               0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  IFGB_RX0 packets         =               0    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =               0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFGB_RX1 packets         =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =               0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  RXPP IFG0 input packets  =               0    |RXPP2   =               0    |RXPP4   =               0    |RXPP6   =               0    |RXPP8   =               0    |RXPP10   =               0    |
INFO  RXPP IFG1 input packets  =               0    |RXPP3   =               0    |RXPP5   =               0    |RXPP7   =               0    |RXPP9   =               0    |RXPP11   =               0    |
INFO  RXPP IFG0 output packets =               0    |RXPP2   =               0    |RXPP4   =               0    |RXPP6   =               0    |RXPP8   =               0    |RXPP10   =               0    |
INFO  RXPP IFG1 output packets =               0    |RXPP3   =               0    |RXPP5   =               0    |RXPP7   =               0    |RXPP9   =               0    |RXPP11   =               0    |
INFO  SMS IFG0 write packets   =               0    |SMS2    =               0    |SMS4    =               0    |SMS6    =               0    |SMS8    =               0    |SMS 10   =               0    |
INFO  SMS IFG1 write packets   =               0    |SMS3    =               0    |SMS5    =               0    |SMS7    =               0    |SMS9    =               0    |SMS 11   =               0    |
INFO  REASSEMBLY Slc0 packets  =               0    |REAS1   =               0    |REAS2   =               0    |REAS3   =               0    |REAS4   =               0    |REAS5    =               0    |
INFO  PDVOQ Slice0 packets     =               0    |PDVOQ1  =               0    |PDVOQ2  =               0    |PDVOQ3  =               0    |PDVOQ4  =               0    |PDVOQ5   =               0    |
INFO  PDVOQ Slice0 bytes       =               0    |PDVOQ1  =               0    |PDVOQ2  =               0    |PDVOQ3  =               0    |PDVOQ4  =               0    |PDVOQ5   =               0    |
INFO  FILB Slice0 packets      =               0    |FILB1   =               0    |FILB2   =               0    |FILB3   =               0    |FILB4   =               0    |FILB5    =               0    |
INFO  FILB Slice0 bytes        =               0    |FILB1   =               0    |FILB2   =               0    |FILB3   =               0    |FILB4   =               0    |FILB5    =               0    |
INFO  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX--C--R--O--S--S--XXXXXXXXXX--B--A--R--XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX|
INFO  TXPDR Slice0 packets     =               0    |TXPDR1  =               0    |TXPDR2  =               0    |TXPDR3  =               0    |TXPDR4  =               0    |TXPDR5   =               0    |
INFO  TXCGM Slice0 packets     =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 bytes       =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 UC packets  =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 MC packets  =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  SMS IFG0 read packets    =               0    |SMS2    =               0    |SMS4    =               0    |SMS6    =               0    |SMS8    =               0    |SMS 10   =               0    |
INFO  SMS IFG1 read packets    =               0    |SMS3    =               0    |SMS5    =               0    |SMS7    =               0    |SMS9    =               0    |SMS 11   =               0    |
INFO  TXPP0 packets            =               0    |TXPP2   =               0    |TXPP4   =               0    |TXPP6   =               0    |TXPP8   =               0    |TXPP10   =               0    |
INFO  TXPP1 packets            =               0    |TXPP3   =               0    |TXPP5   =               0    |TXPP7   =               0    |TXPP9   =               0    |TXPP11   =               0    |
INFO  IFGB_TX0 packets         =               0    |IFGB2   =               0    |IFGB4   =               0    |IFGB6   =               0    |IFGB8   =               0    |IFGB10   =               0    |
INFO  IFGB_TX1 packets         =               0    |IFGB3   =               0    |IFGB5   =               0    |IFGB7   =               0    |IFGB9   =               0    |IFGB11   =               0    |
INFO  IFG_TX0 good packets     =               0    |IFG_TX2 =               0    |IFG_TX4 =               0    |IFG_TX6 =               0    |IFG_TX8 =               0    |IFG_TX10 =               0    |
INFO  IFG_TX1 good packets     =               0    |IFG_TX3 =               0    |IFG_TX5 =               0    |IFG_TX7 =               0    |IFG_TX9 =               0    |IFG_TX11 =               0    |
INFO  IFG_TX0 good bytes       =       308636352    |IFG_TX2 =               0    |IFG_TX4 =               0    |IFG_TX6 =               0    |IFG_TX8 =               0    |IFG_TX10 =               0    |
INFO  IFG_TX1 good bytes       =               0    |IFG_TX3 =               0    |IFG_TX5 =       154317952    |IFG_TX7 =               0    |IFG_TX9 =               0    |IFG_TX11 =               0    |
INFO  IFG_TX0 flow control     =         4822443    |IFG_TX2 =               0    |IFG_TX4 =               0    |IFG_TX6 =               0    |IFG_TX8 =               0    |IFG_TX10 =               0    |
INFO  IFG_TX1 flow control     =               0    |IFG_TX3 =               0    |IFG_TX5 =         2411218    |IFG_TX7 =               0    |IFG_TX9 =               0    |IFG_TX11 =               0    |
INFO  (*) = counter overflow
(Pdb)
INFO  ___________________Slice0_____________________|____________Slice1___________|___________Slice2____________|___________Slice3____________|___________Slice4____________|_____________Slice5___________|
INFO  IFG_RX0 packets          =               0    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =               0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFG_RX1 packets          =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =               0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  IFG_RX0 bytes            =         5856384    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =               0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFG_RX1 bytes            =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =               0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  IFG_RX0 flow control     =           91506    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =               0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFG_RX1 flow control     =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =               0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  IFGB_RX0 packets         =               0    |IFG_RX2 =               0    |IFG_RX4 =               0    |IFG_RX6 =               0    |IFG_RX8 =               0    |IFG_RX10 =               0    |
INFO  IFGB_RX1 packets         =               0    |IFG_RX3 =               0    |IFG_RX5 =               0    |IFG_RX7 =               0    |IFG_RX9 =               0    |IFG_RX11 =               0    |
INFO  RXPP IFG0 input packets  =               0    |RXPP2   =               0    |RXPP4   =               0    |RXPP6   =               0    |RXPP8   =               0    |RXPP10   =               0    |
INFO  RXPP IFG1 input packets  =               0    |RXPP3   =               0    |RXPP5   =               0    |RXPP7   =               0    |RXPP9   =               0    |RXPP11   =               0    |
INFO  RXPP IFG0 output packets =               0    |RXPP2   =               0    |RXPP4   =               0    |RXPP6   =               0    |RXPP8   =               0    |RXPP10   =               0    |
INFO  RXPP IFG1 output packets =               0    |RXPP3   =               0    |RXPP5   =               0    |RXPP7   =               0    |RXPP9   =               0    |RXPP11   =               0    |
INFO  SMS IFG0 write packets   =               0    |SMS2    =               0    |SMS4    =               0    |SMS6    =               0    |SMS8    =               0    |SMS 10   =               0    |
INFO  SMS IFG1 write packets   =               0    |SMS3    =               0    |SMS5    =               0    |SMS7    =               0    |SMS9    =               0    |SMS 11   =               0    |
INFO  REASSEMBLY Slc0 packets  =               0    |REAS1   =               0    |REAS2   =               0    |REAS3   =               0    |REAS4   =               0    |REAS5    =               0    |
INFO  PDVOQ Slice0 packets     =               0    |PDVOQ1  =               0    |PDVOQ2  =               0    |PDVOQ3  =               0    |PDVOQ4  =               0    |PDVOQ5   =               0    |
INFO  PDVOQ Slice0 bytes       =               0    |PDVOQ1  =               0    |PDVOQ2  =               0    |PDVOQ3  =               0    |PDVOQ4  =               0    |PDVOQ5   =               0    |
INFO  FILB Slice0 packets      =               0    |FILB1   =               0    |FILB2   =               0    |FILB3   =               0    |FILB4   =               0    |FILB5    =               0    |
INFO  FILB Slice0 bytes        =               0    |FILB1   =               0    |FILB2   =               0    |FILB3   =               0    |FILB4   =               0    |FILB5    =               0    |
INFO  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX--C--R--O--S--S--XXXXXXXXXX--B--A--R--XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX|
INFO  TXPDR Slice0 packets     =               0    |TXPDR1  =               0    |TXPDR2  =               0    |TXPDR3  =               0    |TXPDR4  =               0    |TXPDR5   =               0    |
INFO  TXCGM Slice0 packets     =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 bytes       =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 UC packets  =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  TXCGM Slice0 MC packets  =               0    |TXCGM1  =               0    |TXCGM2  =               0    |TXCGM3  =               0    |TXCGM4  =               0    |TXCGM5   =               0    |
INFO  SMS IFG0 read packets    =               0    |SMS2    =               0    |SMS4    =               0    |SMS6    =               0    |SMS8    =               0    |SMS 10   =               0    |
INFO  SMS IFG1 read packets    =               0    |SMS3    =               0    |SMS5    =               0    |SMS7    =               0    |SMS9    =               0    |SMS 11   =               0    |
INFO  TXPP0 packets            =               0    |TXPP2   =               0    |TXPP4   =               0    |TXPP6   =               0    |TXPP8   =               0    |TXPP10   =               0    |
INFO  TXPP1 packets            =               0    |TXPP3   =               0    |TXPP5   =               0    |TXPP7   =               0    |TXPP9   =               0    |TXPP11   =               0    |
INFO  IFGB_TX0 packets         =               0    |IFGB2   =               0    |IFGB4   =               0    |IFGB6   =               0    |IFGB8   =               0    |IFGB10   =               0    |
INFO  IFGB_TX1 packets         =               0    |IFGB3   =               0    |IFGB5   =               0    |IFGB7   =               0    |IFGB9   =               0    |IFGB11   =               0    |
INFO  IFG_TX0 good packets     =               0    |IFG_TX2 =               0    |IFG_TX4 =               0    |IFG_TX6 =               0    |IFG_TX8 =               0    |IFG_TX10 =               0    |
INFO  IFG_TX1 good packets     =               0    |IFG_TX3 =               0    |IFG_TX5 =               0    |IFG_TX7 =               0    |IFG_TX9 =               0    |IFG_TX11 =               0    |
INFO  IFG_TX0 good bytes       =         5856384    |IFG_TX2 =               0    |IFG_TX4 =               0    |IFG_TX6 =               0    |IFG_TX8 =               0    |IFG_TX10 =               0    |
INFO  IFG_TX1 good bytes       =               0    |IFG_TX3 =               0    |IFG_TX5 =         2928256    |IFG_TX7 =               0    |IFG_TX9 =               0    |IFG_TX11 =               0    |
INFO  IFG_TX0 flow control     =           91506    |IFG_TX2 =               0    |IFG_TX4 =               0    |IFG_TX6 =               0    |IFG_TX8 =               0    |IFG_TX10 =               0    |
INFO  IFG_TX1 flow control     =               0    |IFG_TX3 =               0    |IFG_TX5 =           45754    |IFG_TX7 =               0    |IFG_TX9 =               0    |IFG_TX11 =               0    |
INFO  (*) = counter overflow
(Pdb) debug_device.read_register(gibraltar_tree.slice[2].ifg[1].ifgb.fcm_wd_expired_counter[0])
port_wd_expired [31:0] = 0x000000000

(Pdb) debug_device.read_register(gibraltar_tree.slice[2].ifg[1].ifgb.fcm_wd_expired_counter[0])
port_wd_expired [31:0] = 0x000000000

(Pdb)
port_wd_expired [31:0] = 0x000000000

(Pdb) n
***============================================================***
***================== STARTING TRAFFIC ...   ==================***
***============================================================***
SendExpect(<OK>): 0/1 p_traffic on
Traffic started on port 0/1
> /big_share2/pacific/user/yaliuliu/sdkmas/fishnet/tests/fwd_base_test.py(509)_run_test()
-> self.during_traffic_results = self._apply_during_traffic_actions(init_device_and_ports, te,
(Pdb) debug_device.read_register(gibraltar_tree.slice[2].ifg[1].ifgb.fcm_wd_expired_counter[0])
port_wd_expired [31:0] = 0x000000000

(Pdb) n
> /big_share2/pacific/user/yaliuliu/sdkmas/fishnet/tests/fwd_base_test.py(510)_run_test()
-> fwd_generation_class, p.during_traffic_actions)
(Pdb) debug_device.read_register(gibraltar_tree.slice[2].ifg[1].ifgb.fcm_wd_expired_counter[0])
port_wd_expired [31:0] = 0x000000000

(Pdb) n
Passed   5[sec] out of total 120[sec]. remained: 115[sec]
package_mode  default

INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.28[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.80[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.02 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790098950 1247376 478623080000 47862308
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877037780 866811 332039898304 59750161
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3013710 5885 1709898304 26717161
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  14247750
Passed  10[sec] out of total 120[sec]. remained: 110[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.80[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.02 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790105080 1247376 796619200000 79661920
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877213920 866812 551527191312 81847977
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3013230 5885 1719501312 26867208
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  24099490
Passed  15[sec] out of total 120[sec]. remained: 105[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.80[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.03 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790050150 1247376 1058495060000 105849506
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877168630 866812 732279209344 100045951
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3013210 5884 1727409344 26990771
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  32212584
Passed  20[sec] out of total 120[sec]. remained: 100[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.28[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.80[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.03 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790093590 1247376 1332836780000 133283678
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877221230 866816 921635903952 119110239
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3014370 5887 1735693952 27120218
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  40711952
Passed  25[sec] out of total 120[sec]. remained:  95[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.02[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.28[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.81[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|

INFO  IFG_TX0 BitRate= 169.02[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.01 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.03 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790114540 1247376 1594711710000 159471171
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877101790 866813 1102387322112 137308155
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3013550 5886 1743602112 27243783
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  48825073
Passed  30[sec] out of total 120[sec]. remained:  90[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.28[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.80[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.02 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790100300 1247376 1856581260000 185658126
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877212870 866815 1283134910080 155505685
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3014160 5886 1751510080 27367345
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  56938190
Passed  35[sec] out of total 120[sec]. remained:  85[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.81[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.02 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790064180 1247376 2124694080000 212469408
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68876936880 866811 1468191786528 174137070
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3013620 5885 1759606528 27493852
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  65244567
Passed  40[sec] out of total 120[sec]. remained:  80[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.81[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.03 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790046680 1247376 2411507890000 241150789
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877161050 866812 1666156347776 194067992
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3013290 5884 1768267776 27629184
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  74130553
Passed  45[sec] out of total 120[sec]. remained:  75[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.02[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.80[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.41[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.02[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.01 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.04 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790079100 1247376 2667149060000 266714906
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877098340 866812 1842604977648 211832706
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3014040 5887 1775987648 27749807
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  82050206
Passed  50[sec] out of total 120[sec]. remained:  70[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.28[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.80[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.03 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790070470 1247376 2929025310000 292902531
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877183200 866813 2023356505808 230030633
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3013620 5886 1783895808 27873372
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  90163436
Passed  55[sec] out of total 120[sec]. remained:  65[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.28[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.80[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.02 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790111450 1247376 3190898070000 319089807
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877002890 866811 2204106833840 248228438
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3013860 5885 1791803840 27996935
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  98276747
Passed  60[sec] out of total 120[sec]. remained:  60[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.80[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.03 (Gbps), 2.99 (Mpps)
INFO  --- TEMPERATURE SENSORS --- GIBRALTAR_SENSOR_0 - 44.85913848876953C
INFO  --- TEMPERATURE SENSORS --- GIBRALTAR_SENSOR_1 - 43.48524856567383C
INFO  --- TEMPERATURE SENSORS --- GIBRALTAR_SENSOR_2 - 46.50656509399414C
INFO  --- TEMPERATURE SENSORS --- GIBRALTAR_SENSOR_3 - 45.68301773071289C
INFO  --- TEMPERATURE SENSORS --- GIBRALTAR_SENSOR_4 - 43.48524856567383C
INFO  --- TEMPERATURE SENSORS --- GIBRALTAR_SENSOR_5 - 42.93543243408203C
INFO  --- TEMPERATURE SENSORS --- GIBRALTAR_SENSOR_6 - 37.98030471801758C
INFO  --- TEMPERATURE SENSORS --- GIBRALTAR_SENSOR_7 - 37.15326690673828C
INFO  --- TEMPERATURE SENSORS --- GIBRALTAR_SENSOR_8 - 36.32589340209961C
INFO  --- TEMPERATURE SENSORS --- GIBRALTAR_SENSOR_9 - 35.222190856933594C
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790025050 1247375 3452777250000 345277725
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877144200 866812 2384860471936 266426575
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3012810 5885 1799711936 28120499
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  106389807
Passed  65[sec] out of total 120[sec]. remained:  55[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.81[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.02 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790076970 1247376 3721166360000 372116636
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877156470 866813 2570108427024 285077202
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3014560 5888 1807817024 28247141
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  114696157
Passed  70[sec] out of total 120[sec]. remained:  50[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.02[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.28[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.80[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.41[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.02[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.01 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.04 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790042030 1247376 3982762730000 398276273
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877006770 866808 2750667716544 303255771
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3012800 5884 1815716608 28370572
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  122809261
Passed  75[sec] out of total 120[sec]. remained:  45[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.02[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.80[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.02[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.01 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.04 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790067850 1247376 4244634430000 424463443
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877017190 866811 2931416894704 321453463
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3013880 5887 1823624704 28494136
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  130922418
Passed  80[sec] out of total 120[sec]. remained:  40[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.80[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.03 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790035440 1247375 4568866060000 456886606
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68876968780 866812 3155207295936 343984512
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3014190 5888 1833415936 28647124
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  140967356
Passed  85[sec] out of total 120[sec]. remained:  35[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.28[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.81[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.03 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790065620 1247376 4893087960000 489308796
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877245160 866812 3378992516720 366515036
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3012540 5883 1843206720 28800105
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  151012087
Passed  90[sec] out of total 120[sec]. remained:  30[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.81[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.01 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.03 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790029660 1247375 5154963600000 515496360
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877017430 866811 3559744174944 384712977
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3013380 5885 1851114944 28923671
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  159125475
Passed  95[sec] out of total 120[sec]. remained:  25[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.81[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.02 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790012520 1247375 5423072340000 542307234
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877146060 866812 3744798741200 403344128
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3013400 5884 1859211200 29050175
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  167431683
Passed 100[sec] out of total 120[sec]. remained:  20[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.80[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.41[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.02 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790032300 1247375 5697419270000 569741927
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877097930 866812 3934157146064 422408591
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3013150 5885 1867684416 29182569
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  176124592
Passed 105[sec] out of total 120[sec]. remained:  15[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.02[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.81[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.02[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.01 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.03 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790082260 1247376 5959297670000 595929767
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68876889960 866807 4114910824160 440606732
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3012800 5884 1875404160 29303190
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  184044636
Passed 110[sec] out of total 120[sec]. remained:  10[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.01[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.81[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.42[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.01[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.00 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.03 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790065080 1247376 6227404810000 622740481
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877670870 866818 4299963730480 459237718
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3012770 5884 1883500480 29429695
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  192350813
Passed 115[sec] out of total 120[sec]. remained:   5[sec]
package_mode  default
INFO  Got show_npu_host_rate == False -> do not check NPU_HOST Rate
INFO  |__________Slice0_____________|_____________Slice1___________|_____________Slice2___________|_____________Slice3___________|______________Slice4__________|_____________Slice5___________|
INFO  IFG_RX0 BitRate= 169.02[Gbps] |IFG_RX2 BitRate=   0.00[Gbps] |IFG_RX4 BitRate=   0.00[Gbps] |IFG_RX6 BitRate=   0.00[Gbps] |IFG_RX8 BitRate=   0.00[Gbps] |IFG_RX10 BitRate=   0.00[Gbps]|
INFO  IFG_RX1 BitRate=   0.00[Gbps] |IFG_RX3 BitRate=   0.00[Gbps] |IFG_RX5 BitRate=  99.99[Gbps] |IFG_RX7 BitRate=   0.00[Gbps] |IFG_RX9 BitRate=   0.00[Gbps] |IFG_RX11 BitRate=   0.00[Gbps]|
INFO  IFG_RX0 PktRate=   2.12[Mpps] |IFG_RX2 PktRate=   0.00[Mpps] |IFG_RX4 PktRate=   0.00[Mpps] |IFG_RX6 PktRate=   0.00[Mpps] |IFG_RX8 PktRate=   0.00[Mpps] |IFG_RX10 PktRate=   0.00[Mpps]|
INFO  IFG_RX1 PktRate=   0.00[Mpps] |IFG_RX3 PktRate=   0.00[Mpps] |IFG_RX5 PktRate=   1.25[Mpps] |IFG_RX7 PktRate=   0.00[Mpps] |IFG_RX9 PktRate=   0.00[Mpps] |IFG_RX11 PktRate=   0.00[Mpps]|
INFO  Reas  0 PktRate=   2.11[Mpps] |Reas  1 PktRate=   0.00[Mpps] |Reas  2 PktRate=   1.25[Mpps] |Reas  3 PktRate=   0.00[Mpps] |Reas  4 PktRate=   0.00[Mpps] |Reas   5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 BitRate= 169.27[Gbps] |TXCGM 1 BitRate=   0.00[Gbps] |TXCGM 2 BitRate=  69.12[Gbps] |TXCGM 3 BitRate=   0.00[Gbps] |TXCGM 4 BitRate=   0.00[Gbps] |TXCGM  5 BitRate=   0.00[Gbps]|
INFO  TXCGM 0 PktRate=   2.11[Mpps] |TXCGM 1 PktRate=   0.00[Mpps] |TXCGM 2 PktRate=   0.86[Mpps] |TXCGM 3 PktRate=   0.00[Mpps] |TXCGM 4 PktRate=   0.00[Mpps] |TXCGM  5 PktRate=   0.00[Mpps]|
INFO  TXCGM 0 DrpRate=   4.97[Gbps] |TXCGM 1 DrpRate=   4.80[Gbps] |TXCGM 2 DrpRate=   4.68[Gbps] |TXCGM 3 DrpRate=   5.29[Gbps] |TXCGM 4 DrpRate=   5.86[Gbps] |TXCGM  5 DrpRate=   5.41[Gbps]|
INFO  TXCGM 0 TtlRate=   2.17[Mpps] |TXCGM 1 TtlRate=   0.06[Mpps] |TXCGM 2 TtlRate=   0.92[Mpps] |TXCGM 3 TtlRate=   0.07[Mpps] |TXCGM 4 TtlRate=   0.07[Mpps] |TXCGM  5 TtlRate=   0.07[Mpps]|
INFO  IFG_TX0 BitRate= 169.02[Gbps] |IFG_TX2 BitRate=   0.00[Gbps] |IFG_TX4 BitRate=   0.00[Gbps] |IFG_TX6 BitRate=   0.00[Gbps] |IFG_TX8 BitRate=   0.00[Gbps] |IFG_TX10 BitRate=   0.00[Gbps]|
INFO  IFG_TX1 BitRate=   0.00[Gbps] |IFG_TX3 BitRate=   0.00[Gbps] |IFG_TX5 BitRate=  69.02[Gbps] |IFG_TX7 BitRate=   0.00[Gbps] |IFG_TX9 BitRate=   0.00[Gbps] |IFG_TX11 BitRate=   0.00[Gbps]|
INFO  IFG_TX0 PktRate=   2.12[Mpps] |IFG_TX2 PktRate=   0.00[Mpps] |IFG_TX4 PktRate=   0.00[Mpps] |IFG_TX6 PktRate=   0.00[Mpps] |IFG_TX8 PktRate=   0.00[Mpps] |IFG_TX10 PktRate=   0.00[Mpps]|
INFO  IFG_TX1 PktRate=   0.00[Mpps] |IFG_TX3 PktRate=   0.00[Mpps] |IFG_TX5 PktRate=   0.87[Mpps] |IFG_TX7 PktRate=   0.00[Mpps] |IFG_TX9 PktRate=   0.00[Mpps] |IFG_TX11 PktRate=   0.00[Mpps]|
INFO  HBM Write Rate = 0.00 (Mpps), 0.00 (Gbps)
INFO  HBM Read  Rate = 0.00 (Mpps)
INFO  Total Rx rate = 269.01 (Gbps), 3.37 (Mpps)
INFO  Total Tx rate = 238.04 (Gbps), 2.99 (Mpps)
Send()         : 0/1 PT_TOTAL ?
Send() received: 0/1  PT_TOTAL  99790075020 1247376 6489281290000 648928129
Send()         : 0/1 PR_TOTAL ?
Send() received: 0/1  PR_TOTAL  68877138830 866812 4480716188640 477435738
Send()         : 0/1 PR_NOTPLD ?
Send() received: 0/1  PR_NOTPLD  3013060 5884 1891408640 29553260
Send()         : 0/1 P_ERRORS ?
Send() received: 0/1  P_ERRORS  200463929
Passed 120[sec] out of total 120[sec]. remained:   0[sec]






get_counters()


^C



quit




^C^C
Calling 'app_config.snake_basic' class destroy

Destroy l2_snake objects
--- ACLS --- destroying ACLs
--- ACLS --- destroying ACLs
--- ACLS --- cleared acl groups from all ac ports
--- ACLS --- destroyed ingress sequence acl groups
--- ACLS --- destroyed sequence acls
Deleted 0 mac entries (in bridge destroy process)
--- Resource Manager --- Remove L2_AC BASE element idx: 106495 from allocated elements list
--- Resource Manager --- Destroy L2_AC BASE element obj, idx = 106495
--- Resource Manager --- Remove L2_AC BASE element idx: 106493 from allocated elements list
--- Resource Manager --- Destroy L2_AC BASE element obj, idx = 106493
--- Resource Manager --- Remove L2_AC BASE element idx: 106491 from allocated elements list
--- Resource Manager --- Destroy L2_AC BASE element obj, idx = 106491

rxp ports destroy done

mc destroy done
--- Resource Manager --- Remove L2_AC BASE element idx: 106494 from allocated elements list
--- Resource Manager --- Destroy L2_AC BASE element obj, idx = 106494
--- Resource Manager --- Remove L2_AC BASE element idx: 106492 from allocated elements list
--- Resource Manager --- Destroy L2_AC BASE element obj, idx = 106492
--- Resource Manager --- Remove L2_AC BASE element idx: 106490 from allocated elements list
--- Resource Manager --- Destroy L2_AC BASE element obj, idx = 106490

txp ports destroy done

Calling 'app_config.snake_basic' class destroy

Destroy l2_snake objects
--- ACLS --- destroying ACLs
--- ACLS --- destroying ACLs
--- ACLS --- cleared acl groups from all ac ports
--- ACLS --- destroyed ingress sequence acl groups
--- ACLS --- destroyed sequence acls
Deleted 0 mac entries (in bridge destroy process)

rxp ports destroy done

mc destroy done

txp ports destroy done

Calling 'app_config.snake_basic' class destroy
Destroy IP snake objects
--- ACLS --- destroying ACLs
--- ACLS --- cleared acl groups from all ac ports
--- ACLS --- destroyed ingress sequence acl groups
--- ACLS --- destroyed sequence acls

Calling 'app_config.snake_basic' class destroy
Destroy IP snake objects
--- ACLS --- destroying ACLs
--- ACLS --- cleared acl groups from all ac ports
--- ACLS --- destroyed ingress sequence acl groups
--- ACLS --- destroyed sequence acls

Calling 'app_config.snake_basic' class destroy
Destroy l3_snake objects
--- ACLS --- destroying ACLs
--- ACLS --- destroying ACLs
--- ACLS --- cleared acl groups from all ac ports
--- ACLS --- destroyed ingress sequence acl groups
--- ACLS --- destroyed sequence acls

Calling 'app_config.snake_basic' class destroy
Reset vxlan decap_vni objects
Reset vxlan encap_vni objects then destroy vxlan_snake objects
Reset vxlan encap/decap_vni objects then destroy vxlan_snake objects

Calling 'app_config.snake_basic' class destroy

Calling 'app_config.snake_basic' class destroy
Destroy l3_snake objects
--- ACLS --- destroying ACLs
--- ACLS --- cleared acl groups from all ac ports
--- ACLS --- destroyed ingress sequence acl groups
--- ACLS --- destroyed sequence acls

Calling 'app_config.snake_basic' class destroy
Destroy l3_snake objects

Calling 'app_config.snake_basic' class destroy

Calling 'app_config.snake_basic' class destroy

Calling 'app_config.snake_basic' class destroy
eSendExpect(<OK>): 0/1 p_traffic off
x***============================================================***
***===================== STOPPED TRAFFIC  =====================***
***============================================================***
## NOTE:Skipping trap LA_EVENT_ETHERNET_L2CP4, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_L2CP5, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_L2CP6, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_L2CP7, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_MACSEC, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_TEST_OAM_AC_MEP, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_TEST_OAM_AC_MIP, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_TEST_OAM_CFM_LINK_MDL0, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_SMAC_MISS, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_ETHERNET_HOP_BY_HOP, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_IPV4_UNKNOWN_PROTOCOL, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_IPV4_OPTIONS_EXIST, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_IPV6_HOP_BY_HOP, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_IPV6_ZERO_PAYLOAD, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_L3_USER_TRAP1, Verify this is intended !! ##
## NOTE:Skipping trap LA_EVENT_L3_USER_TRAP2, Verify this is intended !! ##

--- TRAP COUNTERS for device[0] ---
Trap LA_EVENT_ETHERNET_NO_SERVICE_MAPPING[Trap-ID: 5 (0x5)] -> count = 357124
Trap LA_EVENT_ETHERNET_L2_DLP_NOT_FOUND[Trap-ID: 49 (0x31)] -> count = 1254
---------------------
clearing trap LA_EVENT_L3_PACKET_FROM_TUNNEL
clearing trap LA_EVENT_L3_L3_SAME_TUNNEL_INTF
clearing trap LA_EVENT_L3_INVALID_SPI
clearing trap LA_EVENT_L3_TUNNEL_SIP_INVALID
clearing trap LA_EVENT_L3_GLEAN_ACI_PROXY
clearing trap LA_EVENT_L3_ENCAP_TABLE_MISS
clearing trap LA_EVENT_L3_TX_FRR_DROP
clearing trap LA_EVENT_L3_TX_MTU_FAILURE
clearing trap LA_EVENT_L3_TTL_OR_HOP_LIMIT_IS_ONE                                                                                                                                                    clearing trap LA_EVENT_L3_NO_VPN_LABEL_FOUND
clearing trap LA_EVENT_L3_MC_SAME_INTERFACE
clearing trap LA_EVENT_L3_SPLIT_HORIZON
clearing trap LA_EVENT_L3_L3_DLP_DISABLED
clearing trap LA_EVENT_L3_NO_L3_DLP_MAPPING
clearing trap LA_EVENT_L3_ASBR_TABLE_MISS
clearing trap LA_EVENT_L3_NO_HBM_ACCESS_OG
clearing trap LA_EVENT_L3_NO_VNI_MAPPING
clearing trap LA_EVENT_L3_BFD_MICRO_IP_DISABLED
clearing trap LA_EVENT_L3_LPM_DEFAULT_DROP
clearing trap LA_EVENT_L3_NULL_ADJ
clearing trap LA_EVENT_L3_DROP_ADJ_NON_INJECT
clearing trap LA_EVENT_L3_DROP_ADJ
clearing trap LA_EVENT_L3_GLEAN_ADJ
clearing trap LA_EVENT_L3_ACL_FORCE_PUNT
clearing trap LA_EVENT_L3_ACL_DROP
clearing trap LA_EVENT_L3_INT_HOP_LIMIT
clearing trap LA_EVENT_L3_EGRESS_MONITOR
clearing trap LA_EVENT_L3_INGRESS_MONITOR
clearing trap LA_EVENT_L3_NO_LP_OVER_LAG_MAPPING
clearing trap LA_EVENT_L3_ICMP_REDIRECT
clearing trap LA_EVENT_L3_LOCAL_SUBNET
clearing trap LA_EVENT_L3_LPM_DROP
clearing trap LA_EVENT_L3_LPM_ERROR
clearing trap LA_EVENT_L3_NO_HBM_ACCESS_SIP
clearing trap LA_EVENT_L3_NO_HBM_ACCESS_DIP
clearing trap LA_EVENT_L3_ISIS_DRAIN
clearing trap LA_EVENT_L3_ISIS_OVER_L3
clearing trap LA_EVENT_L3_IP_MC_EGRESS_PUNT
clearing trap LA_EVENT_L3_IP_MC_G_PUNT_MEMBER
clearing trap LA_EVENT_L3_IP_MC_S_G_PUNT_MEMBER
clearing trap LA_EVENT_L3_IP_MULTICAST_NOT_FOUND
clearing trap LA_EVENT_L3_IP_MC_SNOOP_LOOKUP_MISS
clearing trap LA_EVENT_L3_IP_MC_PUNT_RPF_FAIL
clearing trap LA_EVENT_L3_IP_MC_SNOOP_RPF_FAIL
clearing trap LA_EVENT_L3_IP_MC_SNOOP_DC_PASS
clearing trap LA_EVENT_L3_IP_MC_PUNT_DC_PASS
clearing trap LA_EVENT_L3_IP_MC_DROP
clearing trap LA_EVENT_L3_IP_MULTICAST_RPF
clearing trap LA_EVENT_L3_IP_UNICAST_RPF
clearing trap LA_EVENT_MPLS_MLDP_HEADEND_COPY_SNOOP
clearing trap LA_EVENT_MPLS_VPN_TTL_ONE
clearing trap LA_EVENT_MPLS_PWE_PWACH
clearing trap LA_EVENT_MPLS_ILM_VRF_LABEL_MISS
clearing trap LA_EVENT_MPLS_TE_MIDPOINT_LDP_LABELS_MISS
clearing trap LA_EVENT_MPLS_INVALID_TTL
clearing trap LA_EVENT_MPLS_IPV4_OVER_IPV6_EXPLICIT_NULL
clearing trap LA_EVENT_MPLS_ILM_MISS
clearing trap LA_EVENT_MPLS_FORWARDING_DISABLED
clearing trap LA_EVENT_MPLS_UNEXPECTED_RESERVED_LABEL
clearing trap LA_EVENT_MPLS_ROUTER_ALERT_LABEL
clearing trap LA_EVENT_MPLS_EXTENSION_LABEL
clearing trap LA_EVENT_MPLS_OAM_ALERT_LABEL
clearing trap LA_EVENT_MPLS_MPLS_TP_OVER_LSP
clearing trap LA_EVENT_MPLS_TTL_IS_ZERO
clearing trap LA_EVENT_MPLS_UNKNOWN_PROTOCOL_AFTER_BOS
clearing trap LA_EVENT_IPV6_NON_COMP_MC
clearing trap LA_EVENT_IPV6_DESTINATION_OPTIONS_HEADER
clearing trap LA_EVENT_IPV6_ILLEGAL_DIP
clearing trap LA_EVENT_IPV6_HEADER_ERROR
clearing trap LA_EVENT_IPV6_UC_FORWARDING_DISABLED
clearing trap LA_EVENT_IPV6_MC_FORWARDING_DISABLED
clearing trap LA_EVENT_IPV4_NON_COMP_MC
clearing trap LA_EVENT_IPV4_HEADER_ERROR
clearing trap LA_EVENT_IPV4_CHECKSUM
clearing trap LA_EVENT_IPV4_UC_FORWARDING_DISABLED
clearing trap LA_EVENT_IPV4_MC_FORWARDING_DISABLED
clearing trap LA_EVENT_IPV4_IIC_CHECK_FAIL
clearing trap LA_EVENT_ETHERNET_LAST
clearing trap LA_EVENT_ETHERNET_NO_PWE_L3_DEST
clearing trap LA_EVENT_ETHERNET_SVI_EGRESS_DHCP
clearing trap LA_EVENT_ETHERNET_PFC_DIRECT_SAMPLE
clearing trap LA_EVENT_ETHERNET_PADDING_RESIDUE_IN_SECOND_LINE
clearing trap LA_EVENT_ETHERNET_INCOMPATIBLE_EVE_CMD
clearing trap LA_EVENT_ETHERNET_DISABLED
clearing trap LA_EVENT_ETHERNET_SPLIT_HORIZON
clearing trap LA_EVENT_ETHERNET_EGRESS_STP_BLOCK
clearing trap LA_EVENT_ETHERNET_DSPA_MC_TRIM
clearing trap LA_EVENT_ETHERNET_SAME_INTERFACE
clearing trap LA_EVENT_ETHERNET_L2_DLP_NOT_FOUND
clearing trap LA_EVENT_ETHERNET_MACSEC_PROCESSING_ERR
clearing trap LA_EVENT_ETHERNET_UNPROTECTED_DATA_PKT_ON_MACSEC_EN_PORT
clearing trap LA_EVENT_ETHERNET_MC_SNOOP_LOOKUP_MISS
clearing trap LA_EVENT_ETHERNET_PFC_SAMPLE
clearing trap LA_EVENT_ETHERNET_BCAST_PKT
clearing trap LA_EVENT_ETHERNET_LEARN_PUNT
clearing trap LA_EVENT_ETHERNET_UNKNOWN_UC
clearing trap LA_EVENT_ETHERNET_UNKNOWN_MC
clearing trap LA_EVENT_ETHERNET_UNKNOWN_BC
clearing trap LA_EVENT_ETHERNET_SYSTEM_MYMAC
clearing trap LA_EVENT_ETHERNET_UNKNOWN_L3
clearing trap LA_EVENT_ETHERNET_CISCO_PROTOCOLS
clearing trap LA_EVENT_ETHERNET_LACP
clearing trap LA_EVENT_ETHERNET_L2CP3
clearing trap LA_EVENT_ETHERNET_L2CP2
clearing trap LA_EVENT_ETHERNET_L2CP1
clearing trap LA_EVENT_ETHERNET_L2CP0
clearing trap LA_EVENT_ETHERNET_ISIS_OVER_L2
clearing trap LA_EVENT_ETHERNET_PTP_OVER_ETH
clearing trap LA_EVENT_ETHERNET_INGRESS_STP_BLOCK
clearing trap LA_EVENT_ETHERNET_DHCPV6_CLIENT
clearing trap LA_EVENT_ETHERNET_DHCPV6_SERVER
clearing trap LA_EVENT_ETHERNET_DHCPV4_CLIENT
clearing trap LA_EVENT_ETHERNET_DHCPV4_SERVER
clearing trap LA_EVENT_ETHERNET_SA_MULTICAST
clearing trap LA_EVENT_ETHERNET_DA_ERROR
clearing trap LA_EVENT_ETHERNET_SA_ERROR
clearing trap LA_EVENT_ETHERNET_SA_DA_ERROR
clearing trap LA_EVENT_ETHERNET_ARP
clearing trap LA_EVENT_ETHERNET_NO_VSID_MAPPING
clearing trap LA_EVENT_ETHERNET_NO_VNI_MAPPING
clearing trap LA_EVENT_ETHERNET_NO_SIP_MAPPING
clearing trap LA_EVENT_ETHERNET_NO_TERMINATION_ON_L3_PORT
clearing trap LA_EVENT_ETHERNET_NO_SERVICE_MAPPING
clearing trap LA_EVENT_ETHERNET_ACCEPTABLE_FORMAT
clearing trap LA_EVENT_ETHERNET_ACL_FORCE_PUNT
clearing trap LA_EVENT_ETHERNET_ACL_DROP
clearing trap LA_EVENT_ETHERNET_DOT1X_DROP
clearing trap LA_EVENT_ETHERNET_FIRST
------- All devices traps are now cleared -------
---- Clear debug counters: Post test ----
+------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                                                                     NPE COUNTERS TABLE                                                                     |
+----------+----------+----------+---------+-----+------+-------+---------+---------+---------+-----+------+-------+-----+------+-------+-----+------+-------+
|          |  s0-in   |  s0-out  | s0-loop |s1-in|s1-out|s1-loop|  s2-in  |  s2-out | s2-loop |s3-in|s3-out|s3-loop|s4-in|s4-out|s4-loop|s5-in|s5-out|s5-loop|
+----------+----------+----------+---------+-----+------+-------+---------+---------+---------+-----+------+-------+-----+------+-------+-----+------+-------+
| NPU-Host |    0     |    0     |    0    |  -  |  -   |   -   |    -    |    -    |    -    |  -  |  -   |   -   |  -  |  -   |   -   |  -  |  -   |   -   |
+----------+----------+----------+---------+-----+------+-------+---------+---------+---------+-----+------+-------+-----+------+-------+-----+------+-------+
|Term-NPE-0|916936749 |916936749 |916936749|  0  |  0   |   0   |542625285|542625285|542624866|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+----------+----------+---------+-----+------+-------+---------+---------+---------+-----+------+-------+-----+------+-------+-----+------+-------+
|Term-NPE-1|916936749 |916936749 |916936749|  0  |  0   |   0   |542625285|542625285|542624868|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+----------+----------+---------+-----+------+-------+---------+---------+---------+-----+------+-------+-----+------+-------+-----+------+-------+
|Term-NPE-2|916936749 |916936749 |916936749|  0  |  0   |   0   |542625284|542625284|542624866|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+----------+----------+---------+-----+------+-------+---------+---------+---------+-----+------+-------+-----+------+-------+-----+------+-------+
|Fwd-NPE-0 |916936749 |916936749 |916936749|  0  |  0   |   0   |542625285|542625285|542624869|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+----------+----------+---------+-----+------+-------+---------+---------+---------+-----+------+-------+-----+------+-------+-----+------+-------+
|Fwd-NPE-1 |916936749 |916936749 |916936749|  0  |  0   |   0   |542625285|542625285|542624862|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+----------+----------+---------+-----+------+-------+---------+---------+---------+-----+------+-------+-----+------+-------+-----+------+-------+
|Fwd-NPE-2 |916936749 |916936749 |916936749|  0  |  0   |   0   |542625284|542625284|542624869|  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+----------+----------+---------+-----+------+-------+---------+---------+---------+-----+------+-------+-----+------+-------+-----+------+-------+
| Tx-NPE-0 |1375405124|1375405124|    0    |  0  |  0   |   0   |561648179|561648179|   1230  |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+----------+----------+---------+-----+------+-------+---------+---------+---------+-----+------+-------+-----+------+-------+-----+------+-------+
| Tx-NPE-1 |1375405123|1375405123|    0    |  0  |  0   |   0   |561648178|561648178|   1278  |  0  |  0   |   0   |  0  |  0   |   0   |  0  |  0   |   0   |
+----------+----------+----------+---------+-----+------+-------+---------+---------+---------+-----+------+-------+-----+------+-------+-----+------+-------+
--- NOTIFICATION HANDLER --- post test dump and reset notifications
--- NOTIFICATION HANDLER ---  All notifications are now cleared
SendExpect(<OK>): 0/1 p_traffic off
***============================================================***
***===================== STOPPED TRAFFIC  =====================***
***============================================================***
INFO  ===  LEAKED MEMORY INFO DURING TEST ITEM EXECUTION  ===

Destroy ports
--- NOTIFICATION HANDLER --- : Adding LINK, link_status: ALL, port_id: None, type: None to ignore list - expected number of interrupts in range: [None,None]
-I-MAC_PORT-0- mac_port la_mac_port_base(oid=374)#SerDes 0/0/0# changed state to DOWN (MAC linkLocal faultPCS linkAlignment markerPCS high BER)
-I-MAC_PORT-0- mac_port la_mac_port_base(oid=390)#SerDes 0/0/2# changed state to DOWN (MAC linkLocal faultPCS linkAlignment markerPCS high BER)
-I-MAC_PORT-0- mac_port la_mac_port_base(oid=406)#SerDes 2/1/8# changed state to DOWN (MAC linkLocal faultPCS linkAlignment marker,Signal OK loss on SerDes 0 1)
Destroy ETH...PI...NPUH...SYS PCI...SYS RCY...SYS MAC...SYS REMOTE_MAC...VOQ...MAC...--- EXPECTED LINK NOTIFICATION ---: --- Notification ---:Fri Nov  4 11:46:31 2022 (4): LINK: DOWN: Port 0, Slice 0, IFG 0, SerDes 0 due to: MAC link,PCS link,Alignment marker,PCS high BER
PCI...--- EXPECTED LINK NOTIFICATION ---: --- Notification ---:Fri Nov  4 11:46:31 2022 (5): LINK: DOWN: Port 2, Slice 0, IFG 0, SerDes 2 due to: MAC link,PCS link,Alignment marker,PCS high BER
RCY
--- EXPECTED LINK NOTIFICATION ---: --- Notification ---:Fri Nov  4 11:46:32 2022 (6): LINK: DOWN: Port 238, Slice 2, IFG 1, SerDes 8 due to: MAC link,PCS link,Alignment marker,Signal OK loss [True, True, False, False, False, False, False, False]
--- NOTIFICATION HANDLER --- : Removing LINK, link_status: ALL, port_id: None, type: None from ignore list
Closing notification listener...
--- NOTIFICATION HANDLER --- Dumping ignored notifications
dump_notifications_db: device_id=0, total notifications=3
--- Notification ---:Fri Nov  4 11:46:31 2022 (4): LINK: DOWN: Port 0, Slice 0, IFG 0, SerDes 0 due to: MAC link,PCS link,Alignment marker,PCS high BER, count=1
--- Notification ---:Fri Nov  4 11:46:31 2022 (5): LINK: DOWN: Port 2, Slice 0, IFG 0, SerDes 2 due to: MAC link,PCS link,Alignment marker,PCS high BER, count=1
--- Notification ---:Fri Nov  4 11:46:32 2022 (6): LINK: DOWN: Port 238, Slice 2, IFG 1, SerDes 8 due to: MAC link,PCS link,Alignment marker,Signal OK loss [True, True, False, False, False, False, False, False], count=1

Destroy devices and Shared elements pool

Calling app_config.shared_elements class destroy
Done destroy app_config.shared_elements
Closing sockets
Flush device
Destroy device
-I-HLD-0- Shutting down debug shell...


========================================================================================== warnings summary ==========================================================================================
../driver/shared/test/api/npu_host_packet_gen.py:23
  /big_share2/pacific/user/yaliuliu/sdkmas/driver/shared/test/api/npu_host_packet_gen.py:23: DeprecationWarning: the imp module is deprecated in favour of importlib; see the module's documentation for alternative uses
    import imp

tests/conftest.py:201
  /big_share2/pacific/user/yaliuliu/sdkmas/fishnet/tests/conftest.py:201: DeprecationWarning: `type` argument to addoption() is the string 'string',  but when supplied should be a type (for example `str` or `int`). (options: ('--marker-expr',))
    help="marker expression - can contain several markers, seperated by comma (without spaces)")

tests/non_default/tm_tests/pfc_snake_test.py::TestSaPfcHBM__UcBridgeP2P::test_sa_pfc__uc_bridge_p2p_packet_sweep[single1-PACKET_SIZE_10000-TC_0]
tests/non_default/tm_tests/pfc_snake_test.py::TestSaPfcHBM__UcBridgeP2P::test_sa_pfc__uc_bridge_p2p_packet_sweep[single1-PACKET_SIZE_10000-TC_0]
tests/non_default/tm_tests/pfc_snake_test.py::TestSaPfcHBM__UcBridgeP2P::test_sa_pfc__uc_bridge_p2p_packet_sweep[single1-PACKET_SIZE_10000-TC_0]
  /common/pkgs/python/3.6.10/lib/python3.6/site-packages/urllib3/connectionpool.py:851: InsecureRequestWarning: Unverified HTTPS request is being made. Adding certificate verification is strongly advised. See: https://urllib3.readthedocs.io/en/latest/advanced-usage.html#ssl-warnings
    InsecureRequestWarning)

-- Docs: https://docs.pytest.org/en/stable/warnings.html
----------------------------------------------------------- generated xml file: /big_share2/pacific/user/yaliuliu/sdkmas/fishnet/junit.xml -----------------------------------------------------------
================================================================================== 5 warnings in 6171.72s (1:42:51) ==================================================================================
Traceback (most recent call last):
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/main.py", line 269, in wrap_session
    session.exitstatus = doit(config, session) or 0
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/main.py", line 323, in _main
    config.hook.pytest_runtestloop(session=session)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/hooks.py", line 286, in __call__
    return self._hookexec(self, self.get_hookimpls(), kwargs)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/manager.py", line 93, in _hookexec
    return self._inner_hookexec(hook, methods, kwargs)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/manager.py", line 87, in <lambda>
    firstresult=hook.spec.opts.get("firstresult") if hook.spec else False,
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 187, in _multicall
    res = hook_impl.function(*args)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 80, in get_result
    raise ex[1].with_traceback(ex[2])
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 187, in _multicall
    res = hook_impl.function(*args)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/main.py", line 348, in pytest_runtestloop
    item.config.hook.pytest_runtest_protocol(item=item, nextitem=nextitem)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/hooks.py", line 286, in __call__
    return self._hookexec(self, self.get_hookimpls(), kwargs)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/manager.py", line 93, in _hookexec
    return self._inner_hookexec(hook, methods, kwargs)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/manager.py", line 87, in <lambda>
    firstresult=hook.spec.opts.get("firstresult") if hook.spec else False,
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 187, in _multicall
    res = hook_impl.function(*args)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 80, in get_result
    raise ex[1].with_traceback(ex[2])
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 187, in _multicall
    res = hook_impl.function(*args)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/runner.py", line 109, in pytest_runtest_protocol
    runtestprotocol(item, nextitem=nextitem)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/runner.py", line 126, in runtestprotocol
    reports.append(call_and_report(item, "call", log))
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/runner.py", line 215, in call_and_report
    call = call_runtest_hook(item, when, **kwds)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/hooks.py", line 286, in __call__
    return self._hookexec(self, self.get_hookimpls(), kwargs)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/manager.py", line 93, in _hookexec
    return self._inner_hookexec(hook, methods, kwargs)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/manager.py", line 87, in <lambda>
    firstresult=hook.spec.opts.get("firstresult") if hook.spec else False,
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 203, in _multicall
    gen.send(outcome)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/skipping.py", line 272, in pytest_runtest_makereport
    rep = outcome.get_result()
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 80, in get_result
    raise ex[1].with_traceback(ex[2])
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 187, in _multicall
    res = hook_impl.function(*args)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/runner.py", line 337, in pytest_runtest_makereport
    return TestReport.from_item_and_call(item, call)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/reports.py", line 322, in from_item_and_call
    longrepr = item.repr_failure(excinfo)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/python.py", line 1677, in repr_failure
    return self._repr_failure_py(excinfo, style=style)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/nodes.py", line 404, in _repr_failure_py
    truncate_locals=truncate_locals,
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/code.py", line 648, in getrepr
    return fmt.repr_excinfo(self)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/code.py", line 905, in repr_excinfo
    reprtraceback = self.repr_traceback(excinfo_)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/code.py", line 846, in repr_traceback
    reprentry = self.repr_traceback_entry(entry, einfo)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/code.py", line 790, in repr_traceback_entry
    source = self._getentrysource(entry)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/code.py", line 698, in _getentrysource
    source = entry.getsource(self.astcache)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/code.py", line 253, in getsource
    self.lineno, source, astnode=astnode
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/source.py", line 182, in getstatementrange_ast
    start, end = get_statement_startend2(lineno, astnode)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/source.py", line 154, in get_statement_startend2
    val: Optional[List[ast.stmt]] = getattr(x, name, None)
KeyboardInterrupt

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/common/pkgs/python/3.6.10/bin/pytest", line 11, in <module>
    sys.exit(console_main())
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/config/__init__.py", line 185, in console_main
    code = main()
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/config/__init__.py", line 163, in main
    config=config
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/hooks.py", line 286, in __call__
    return self._hookexec(self, self.get_hookimpls(), kwargs)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/manager.py", line 93, in _hookexec
    return self._inner_hookexec(hook, methods, kwargs)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/manager.py", line 87, in <lambda>
    firstresult=hook.spec.opts.get("firstresult") if hook.spec else False,
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 187, in _multicall
    res = hook_impl.function(*args)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 80, in get_result
    raise ex[1].with_traceback(ex[2])
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 187, in _multicall
    res = hook_impl.function(*args)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/main.py", line 316, in pytest_cmdline_main
    return wrap_session(config, _main)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/main.py", line 269, in wrap_session
    session.exitstatus = doit(config, session) or 0
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/hooks.py", line 286, in __call__
    return self._hookexec(self, self.get_hookimpls(), kwargs)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/manager.py", line 93, in _hookexec
    return self._inner_hookexec(hook, methods, kwargs)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/manager.py", line 87, in <lambda>
    firstresult=hook.spec.opts.get("firstresult") if hook.spec else False,
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 208, in _multicall
    return outcome.get_result()
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 80, in get_result
    raise ex[1].with_traceback(ex[2])
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/pluggy/callers.py", line 187, in _multicall
    res = hook_impl.function(*args)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/terminal.py", line 837, in pytest_keyboard_interrupt
    self._keyboardinterrupt_memo = excinfo.getrepr(funcargs=True)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/code.py", line 648, in getrepr
    return fmt.repr_excinfo(self)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/code.py", line 905, in repr_excinfo
    reprtraceback = self.repr_traceback(excinfo_)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/code.py", line 846, in repr_traceback
    reprentry = self.repr_traceback_entry(entry, einfo)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/code.py", line 790, in repr_traceback_entry
    source = self._getentrysource(entry)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/code.py", line 698, in _getentrysource
    source = entry.getsource(self.astcache)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/code.py", line 253, in getsource
    self.lineno, source, astnode=astnode
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/source.py", line 182, in getstatementrange_ast
    start, end = get_statement_startend2(lineno, astnode)
  File "/common/pkgs/python/3.6.10/lib/python3.6/site-packages/_pytest/_code/source.py", line 150, in get_statement_startend2
    for x in ast.walk(node):
  File "/common/pkgs/python/3.6.10/lib/python3.6/ast.py", line 225, in walk
    todo.extend(iter_child_nodes(node))
  File "/common/pkgs/python/3.6.10/lib/python3.6/ast.py", line 183, in iter_child_nodes
    for name, field in iter_fields(node):
KeyboardInterrupt
!!--FAIL--!!
End of regression testing...
[root@localhost /big_share2/pacific/user/yaliuliu/sdkmas/fishnet]# e
-bash: e: command not found
[root@localhost /big_share2/pacific/user/yaliuliu/sdkmas/fishnet]#
Network error: Software caused connection abort



-----------------------------------------debug------------------------------------------------
PFC enabled ports list = [238, 0]
set port shaper: slice 2, ifg 1, port 8, rate 69

debug_device.read_register(gibraltar_tree.slice[2].ifg[1].ifgb.fcm_wd_expired_counter[8])
