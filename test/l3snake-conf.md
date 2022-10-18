Device config:           
                          ______________________________
      ____________________|___________________        |
|     |                   |        |         |         |
|Ethernet0|        |Ethernet2|    |        |port7    port8|
|Ethernet1|        |Ethernet3|    |        |      IXIA    |
|      |___________________|                  




sudo config vrf add Vrf203
sudo config interface vrf bind Ethernet2 Vrf203
sudo config interface vrf bind Ethernet3 Vrf203

sudo config vrf add Vrf100
sudo config interface vrf bind Ethernet0 Vrf100
sudo config interface vrf bind Ethernet1 Vrf100



sudo config int ip add Ethernet0 10.0.0.10/24
sudo config int ip add Ethernet2 20.0.0.10/24
sudo config int ip add Ethernet1 103.0.0.11/24
sudo config int ip add Ethernet3 103.0.0.33/24



sudo config route add prefix vrf Vrf100 20.0.0.0/24 nexthop vrf Vrf100 103.0.0.33
sudo config route add prefix vrf Vrf203 10.0.0.0/24 nexthop vrf Vrf203 103.0.0.11

for s in range(6):
    for i in range(8):
        debug_device.write_register(gibraltar_tree.slice[s].npu.rxpp_term.fi_eng[i].ethernet_error_checks, 0)

ping -I Vrf100 103.0.0.33
ping -I Vrf203 103.0.0.11

ping -I Vrf203 20.0.0.100

IxIA config:
port 7 <--> device Ethernet0
port 8 <--> device Ethernet2
port7: 10.0.0.100/24
port8: 20.0.0.100/24

sudo config route del prefix vrf Vrf100 20.0.0.0/24 nexthop vrf Vrf100 103.0.0.33
