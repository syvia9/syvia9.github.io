# why we need neighbor protocal(IPV4 ARP/IPV6 NH):
* neighbor协议用于管理两个neighbor的l2 address 和 l3 address 的mapping
  - l2 address 好比一个人的ID number, 一般情况下是固定的
  - L3 address 就像一个人的phone number，变化多一些
  - host1-intf1 represent A; host2-intf2 represent B
  - Q1:in which situation, A and B are neghbor?
    + there is only one L3 hop between A and B;
    + both below 2 conditions are required:
      * A and B are connected to the same LAN 2(A and B are living in the same city)
      * A and B are configured on the same L3 network 198.2.2.0/24 (they are registered in the same   telecom borough)
        IP of A: 198.2.2.1/24, IP of B: 198.2.2.5/24  
  - A talk to B by phone: 198.2.2.1 ping 198.2.2.5  
    + service provider check if they are in the same service borough-> yes
    + check from which port is used to be sent out and add whose ID number and if he has been    registered here(check ARP table).
      * if yes:the packet destination ID will be changed into B ID number; (l2 address)
      * if not:the ID num is kept ff:ff:ff:ff:ff:ff
  -
## ![SONIC architecture](C:\Users\yaliuliu\OneDrive - Cisco\Documents\work\input\learn\linuxnet)


https://43h.fun/network/arp.html
