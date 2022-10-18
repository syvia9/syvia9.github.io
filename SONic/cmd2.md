show interfaces description 
查看设备中所有端口的描述。
show interfaces+端口名
查看指定端口下的信息，如流量、双工模式、UP/DOWN状态、IP地址、描述等。
show running-config
查看设备的配置。
show running-config interface+端口名
查看指定端口的配置。
show version
查看设备硬件、软件信息。主要用来看设备重启时间。
show logging
查看设备日志。
show processes cpu
查看设备CPU各进程状态。主要用来查看CPU是否占用率过高，哪个进程占用过高。
show arp 端口名。
查看指定端口的arp状态，主要用来查看是否能解析到与该端口相连设备的二层地址和三层地址。
show arp vrf +vrf名字
查看指定vrf的arp状态，主要用来查看是否能解析到该vrf下所有端口的对端设备二层地址和三层地址。
show arp vrf +vrf名字+端口名
查看指定vrf的arp状态，主要用来查看是否能解析到该vrf下指定端口的对端设备二层地址和三层地址。
show vrf all
查看设备下包含的所有vrf名字及其RD和RT名字。主要用来查看该设备上是否有指定VPN的存在。
show ip interface brief
查看设备中所有端口的IP地址、UP/DOWN状态。
Ping+ip地址
查看从设备到指定ip地址的连通性。
Ping vrf +vrf名字+ip地址
查看从设备到指定vpn下ip地址的连通性。
Show vlan brief
查看设备vlan划分状态，主要用来查看交换机各端口属于哪个vlan
Show mac-address-table
查看设备mac地址表，主要用来查看交换机端口与对端设备是否连通。
Show route
查看路由表
Show route | inc +ip地址
查看路由表中包含指定ip的路由条目，主要用来查看该设备是否有到达指定ip的路由。
Show route vrf+vrf名字 | inc +ip地址
查看指定vrf路由表中指定ip的路由条目，主要用来查看该设备是否有达到指定vrf中指定ip的路由。
traceroute +ip地址
查看设备到指定ip途径的设备的ip地址。
traceroute +vrf名字+ip地址
查看设备到指定vrf 的指定ip途径的设备的ip地址。
show controllers +指定物理端口+ phy
查看指定物理端口的物理特性，主要用来查看端口的光功率。
