
# 知乎专栏，讲FIB/RIB:
https://zhuanlan.zhihu.com/p/415032187
## 路由表（Routing Table）、转发表（Forwarding Table）
在计算机网络中，路由器的主要工作就是为经过路由器的每个数据包寻找一条最佳的传输路径，并将该数据有效地传送到目的站点。为了能够实现从众多路径中选择最佳的传输路径，路由器中保存了周边网络的拓扑信息和各种路径参数，我们将这张表称作路由表。路由表（routing table）或称路由择域信息库（RIB, Routing Information Base），是一个存储在路由器或者联网计算机中的电子表格（文件）或类数据库。路由表存储着指向特定网络地址的路径（在有些情况下，还记录有路径的路由度量值）。路由表建立的主要目标是为了实现路由协议和静态路由选择。

在每一个路由器设备中，通常都维护了两张比较相似的表，分别为：

路由信息表（Routing Information Base），简称为RIB表、路由表
转发信息表（Forwarding Information Base）, 简称为FIB表、转发表
其中，路由表（RIB表）用来决策路由；转发表用来转发分组。

由于路由器的核心工作便是为经过路由器的每一个数据包找到最佳路径。何为最佳？ 当然是在众多路径中选择最快、质量最好、路径最短、…等指标选择最优的路径，并将到达不同网络的最优路径对应的路由组成一张新的表格，即FIB表(转发表)。

在我的Ubantu系统中可以分别通过route 、 route -F 来查询RIB表和FIB表。
## ![Linux FIB/RIB lookup](https://pic2.zhimg.com/80/v2-27677ba87283f92ed65a5f6e8003ea2d_1440w.jpg)

由于是主机设备，路由表比较简单，且不存在多个出接口，因此FIB表和RIB是相同的。

需要说明的是：这两种表存在多种叫法，但是只要知道了这两个表的作用，那么见到其他的叫法时便也不再陌生。通常情况下，我们在网络转发中提到的路由表，是这两个表的统称，或者根本没有区分使用的哪张表。不同的网络设备也有可能采用不同的表作为路由、寻址、转发的依据。

路由表项内容：
在路由表中，每一项都包括如下内容：

目的网络地址(Destination) + 子网掩码(Genmask)：

网络地址和网络掩码共同确定本机可以达到的目的网络范围，通常情况下，目的网络范围包含以下几种情况： (1) 主机地址：某个特定主机的网络地址； (2) 子网地址：某个特定子网的网络地址； (3)默认路由：所有未在路由表中指定的网络地址，用0.0.0.0统一匹配，用于配置默认网关(ubantu虚拟机中默认路由显示为default)

网关（Gateway）/下一跳（Next Hop）：

一般终端设备如（PC，手机等）接入网络时，无需配置任何路由信息，而是通过路由器的DHCP协议分配IP地址，终端设备接收IP地址的同时会将本设备的网关设置为直连的路由器。而后上网过程中所有的报文在查询路由时，由于没有其他路由，因此被直接发送到了网关设备，有网关设备进行后续转发功能。

而网络设备一般通过配置动态路由协议来更新路由表,除此之外也会设置默认网关。在收到数据包时如果路由表中有对应的路由表项，则通过此表项的出接口发送到下一跳网络设备，如果没有匹配到相应的路由表项，则需要发给默认网关，有网关进行后续转发处理工作。

接口（Iface）：

接口定义了针对特定的网络目的地址，路由器用于转发数据包的出接口。即用来确定数据包从哪个网口上发送到下一跳设备。

跳数（Metric）：

跳数用于指出路由的成本，通常情况下代表:到达目标地址所需要的总路由器个数，一个跳数代表经过一个路由器，IP数据报首部中的TTL字段就是该数据报所能存活的总跳数。跳数越少往往代表着该路由成本越低，跳数越多则说明成本越高。当具有多条达到相同目的网络的路由选项时，路由算法会选择具有更少跳数的路由。

标志（Flag）：

路由表中常见的flag标记有：

U：路由是动态的；
H：目标是一个主机；
G：路由指向网关；
R：恢复动态路由产生的表项；
D：由路由的后台程序动态安装；
M：由路由的后台程序修改；
!： 拒绝路由。
以前工作中经常查看思科设备路由表，它的标记位更加详细，明确标出了路由条目所属动态路由类型。

## ![cisco device RIB table](https://pic4.zhimg.com/80/v2-570cac36badef4e842d06509d0ae2ccf_1440w.jpg)

## 4. 小结
上文中主要介绍了计算机网络中经常遇到的3类表(路由表、ARP表、Mac表)。其中路由表又可以细分为路由信息表(RIB)和转发信息表(FIB)，RIB表用来维护网络的拓扑信息，而FIB则是从RIB表中选择最优的路由构成的转发表信息。在进行报文转发(发送)时：

先查询路由表，确定目的地址是否可达，如果可达则确定出接口和下一跳信息
再查询ARP表，获取到目的地址对应的Mac地址信息，构建完整的以太网报文。
最后查询Mac表，是为了确定报文的发送接口，确定了出接口，内核会将报文发送到对应的网卡驱动上，网卡在合适的时间会将报文发送到下一跳设备上。


# How to change 8201.json to enable per_event_counter for debug : get_counters() under debug shell
1.Xiaochen Fan 9/22/2022 5:15 PM • 
Steven Xi Chen

Xiaochen 测ACL资源用这个bin
/var/www/html/steven-1.54.0.ph2ea4.8-port_prot_cnt-09012022.bin
注意，8201.json里面加上
"per_event_counters" : true

Yang


Xiaochen Fan 9/22/2022 5:19 PM • 
{
    "board-type": "churchill_p3",
    "description": "Slot 0 (PHY 0), Asic 0 (churchill_p3 [0:39]) on chassis churchill",
    "board-rev": "0",
    "devices": [
         {
           "id": 0,
           "type": "gibraltar",
           "rev": 1,
	   "device_property": {
		   "enable_service_counters": true,


         "voq_prefetch_size": 4,
"flow_cache_enable": true,
"flow_cache_activity_aging_time_in_ns": 200000,
"flow_cache_coherency_aging_time_in_ns": 35000000,

		   "device_frequency": 1350000,
		   "per_event_counters" : true

           },
	   "traps_config": "/opt/cisco/silicon-one/res/config/traps_config.json",

           "push_port_qos_to_switch": true,
           "ifg_swap_lists": [
                  {"slice":0,"ifg":0,
                   "swap":[1, 0, 3, 2, 4, 5, 6, 7, 11, 9, 10, 8, 13, 15, 14, 12, 17, 16, 18, 19, 21, 22, 23, 20],
……
