
# BGP vs IGP:
IGP： interior gateway protocol—链路状态
BGP: border gateway protocol—距离矢量 

都是实现路由信息的交换、学习

都能实现路由的功能

BGP一般用于大型网络，可容纳的路由信息更多；而IGP协议，对于路由条目的存储量是有限的，比如OSPF协议，最多也只能容纳1W条路由；

IGP是内部网关协议，在AS内部实现路由信息的交换；BGP是边界网关协议，在AS之间实现路由信息的交换；

BGP的实现，需要IGP作为其底层的通信基础；

BGP是建立的可靠的TCP基础上的，端口号为179；

IGP的设计重点是对路由的学习与交换，发现路由等，而BGP的设计，主要是为了控制路由的传播，即进行路径选择，BGP有丰富的选路策略，与其说BGP是一个路由协议，倒不如说BGP是一个路径选择协议；

![BGP-IBGP-EBGP](https://img-blog.csdnimg.cn/058e396ffbf346eb8be64c24275c934c.png)

![BGP-message](C:\Users\yaliuliu\OneDrive - Cisco\Documents\work\input\learn\linuxnet\BGPmessage.png)


https://www.sdnlab.com/20315.html


# BGP message:

在TCP链接建立之后，BGP之间会发送OPEN信息，OPEN信息包含一些参数的协商。

版本号，默认是4，如果一边是3一边是4，则3会给4发notification，4会自动修改成3去建邻居。
AS号
Hold time，默认是180s，如果两端不一致，则自动协商成为小的那个。如果设置为0，则可以不发送keep alive
BGP ID，跟OSPF 的RID类似
其他的信息，例如认证
Keep alive
keep alive信息是根据hold time计算出来的。也就是hold time的三分之一。默认是60S
Update
网络层可达信息-NLRI，这个是以多元组的形式传输的-(Length, Prefix)，具体内容有待抓包确认。
路径的属性，也就是上面的那些路由条目所携带的属性
不可用的路由，也是以上面的那个多元组形式传输，标识一些已经不可用的路由，让邻居从BGP表中删除。
Note that although multiple prefixes might be included in the NLRI field, each update message
describes only a single BGP route (because the path attributes describe only a single path, but that path might lead to multiple destinations).
Notification
遇到错误的时候发notification


# BGP configuration: https://blog.csdn.net/m0_58462317/article/details/125962322
1，BGP建邻的基本配置

1，EBGP对等体关系直连建邻

2，IBGP对等体关系之间的环回建邻

3，EBGP对等体关系之间的非直连建邻

2，发布路由

1，network --- 在BGP中只能用来发布路由条目信息

2，重发布

3，BGP的路由聚合

自动聚合

手工聚合

4，路由反射器

路由反射器的反射规则：

5，联邦

## 1.BGP建邻的基本配置

EBGP的两个邻居必须是同网段的,或者像IBGP,用loopback port,指定指明多跳路由
IBGP的两个邻居可以不是同网段的，最佳实践： IBGP router IP地址用两个router各自的环回地址

### (1)EBGP对等体关系直连建邻
        [r1]bgp 1 ---- 启动BGP进程 ---- 后面的1不是进程号，而是配置路由器所在AS的AS号
        [r1-bgp]
        [r1-bgp]router-id 1.1.1.1 --- 配置RID
        [r1-bgp]peer 12.0.0.2 as-number 2 --- 手工指定对等体关系
        [r1]display bgp peer --- 查看BGP邻居表的命令
### (2)IBGP对等体关系之间的环回建邻
        由于IBGP邻居处于同一个AS中，一般情况下，一个AS中存在大量的备份路径，若使用物理接口建立邻居关系，将浪费这些备份或者负载均衡资源，故建议使用环回接口来进行IBGP对等体关系的建立。
        [r2-bgp]peer 3.3.3.3 as-number 2
        [r2-bgp]peer 3.3.3.3 connect-interface LoopBack 0 --- 指定在给3.3.3.3发包时使用的源IP地址为环回接口0的IP地址。
注意：在使用环回接口建立对等体关系时，一定要修改发送接口 。
### (3)EBGP对等体关系之间的非直连建邻
注意：在EBGP对等体关系之间，一般是不具备非直连建邻的路由基础的，所以，需要先保证地址可达才行。
        [r4-bgp]peer 5.5.5.5 as-number 3
        [r4-bgp]peer 5.5.5.5 connect-interface LoopBack 0
        [r4-bgp]peer 5.5.5.5 ebgp-max-hop 2 --- 因为EBGP对等体之间一般是直连建邻，所以，数据包中的TTL值设置为1，要想非直连建邻，则需要将这个值改大。[r5-bgp]peer 4.4.4.4 ebgp-max-hop --- 如果后面不跟参数，则代表将TTL值修改为最大值255
## 2.发布路由
1，network --- 在BGP中只能用来发布路由条目信息
注意：只要是路由表中存在的路由条目信息，BGP都可以通过Network来进行发送。
        [r1-bgp]network 1.1.1.0 24 --- 目标网段信息及掩码必须和路由表中的完全一致才行。
        [r1-bgp]display bgp routing-table --- 查看BGP表
Network         NextHop         MED         LocPrf         PrefVal         Path/Ogn
*> 1.1.1.0/24   0.0.0.0               0              0                 i
Network --- 目标网段信息及掩码信息
NextHop --- BGP的一个路径属性 ---- 谁发的路由信息，下一跳就是谁，如果是自己发的，则下一跳为0.0.0.0。
状态码
* --- 代表 可用 --- 设备每收到一跳路由信息，都会检查其下一跳的可达性。即根据下一跳在路由表中递归查询，只要可达，则改路由信息可用。
> --- 代表 优选 --- 当收到到达相同网段存在多条路由信息时，BGP将在其中根据属性优选出一条加载到路由表中。这条优选路由将赋予这个标记。
注意：只有一条路由条目是可用且优选的，他才能够被加到路由表中，也才能够被传递给其他的BGP对等体。
1.1.1.0/24 EBGP 255 --- 通过EBGP对等体学到的BGP路由信息，其标记为EBGP，默认的优先级为255。
I --- 状态码I --- 代表BGP路由信息是从自己IBGP对等体处学到的
i 1.1.1.0/24 12.0.0.1 --- 因为在AS内部存在AS-BY-AS规则，所以，默认情况下传递的属性信息是一致的，因为这个下一跳也属于路径属性之一，默认情况下也不会传递，则将可能导致路由可用性校验失败。
[r2-bgp]peer 3.3.3.3 next-hop-local --- 在给3.3.3.3传递路由信息时将下一跳属性改为本地
1.1.1.0/24 IBGP 255 --- 通过IBGP对等体学到的BGP路由信息，其标记为IBGP，默认的优先级为255。
路由表中的NextHop直接使用的是BGP属性中的下一跳，因为之前进行过可用性校验，所以，可以保证能够递归查找找到这个下一跳。
2，重发布
[r2-bgp]import-route ospf 1 --- 将OSPF的路由信息导入到BGP当中。
OGN --- 起源码 --- I，e，？ --- 用来标识路由条目的起源
        I --- 代表该路由信息起源于IGP协议（不局限于IGP协议，包括静态，直连），代表该路由条目起源于AS内部 ---通过network发布出来的路由信息其起源码为I
        E --- 代表该路由信息起源于EGP协议 --- EGP指的是BGP之前使用的外部网关协议
        ？ --- 通过除了以上两种方式学习到的路由 --- 重发布导入的路由起源码都是？
## 3.BGP的路由聚合
自动聚合
1，该方法只能针对重发布发布的路由信息生效。
2，自动聚合的路由只能按照主类进行聚合，将造成巨大的路由黑洞。所以，华为设备BGP的自动聚合功能是默认关闭的。
1，抓取流量
[r1]ip ip-prefix aa permit 172.16.0.0 22 greater-equal 24 less-equal 24
2，做路由策略
[r1]route-policy aa permit node 10
Info: New Sequence of this List.
[r1-route-policy]if-match ip-prefix aa
3，在重发布过程中调用路由策略
[r1-bgp]import-route direct route-policy aa
[r1-bgp]summary automatic --- 开启自动聚合的方法
Info: Automatic summarization is valid only for the routes imported
through the import-route command.
*> 172.16.0.0 127.0.0.1 --- 通过自动聚合会发布一条新的汇总路由，他是不携带子网掩码的，因为按照主类汇总，则子网掩码取主类默认值。而且通过聚合发布的路由信息其下一跳属性为127.0.0.1
注意：自动聚合之后，发布的汇总路由信息将在本地路由表中产生一条指向汇总的空接口，自动防环。
状态码 --- S --- suppressed --- 抑制 --- 抑制路由条目的传递
## 4.手工聚合
因为自动聚合存在两个缺陷，所以，如果需要对汇总进行精准把控时，手工聚合将是更理想的方案。
[r1-bgp]aggregate 172.16.0.0 22 --- 手工聚合
*> 172.16.0.0/22 127.0.0.1 --- 手工聚合后发布的路由条目将携带掩码信息，并且下一跳也是指向127.0.0.1，则其也会自动生成一条到达汇总网段指向空接口的路由进行防环。
手工聚合的问题：
1，发布聚合路由的情况下，不会抑制明细路由，导致汇总操作并没有减少路由条目数量，反而增加了。
2，在进行汇总的时候，发布的汇总路由不会继承明细路由的属性，尤其是AS_PATH，则将导致汇总路由部分属性缺失，甚至可能出现环路。
为了避免以上两个问题的产生，我们必须在配置过程中增加命令来完成。
[r4-bgp]aggregate 172.16.0.0 22 detail-suppressed --- 在发布汇总路由条目的同时将抑制所有的明细路由，但是，因为BGP协议的一些特殊性，我们往往不能将其所有的明细路由全部抑制。只能够抑制部分的路由信息 --- 所以我们需要使用到suppressed - policy。
1，抓取流量，使用前缀列表
[r4]ip ip-prefix aa permit 172.16.1.0 24
2，使用路由策略匹配流量
[r4]route-policy aa permit node 10
Info: New Sequence of this List.
[r4-route-policy]if-match ip-prefix aa
[r4-route-policy]q
3，使用抑制策略调用路由策略
[r4-bgp]aggregate 172.16.0.0 22 suppress-policy aa
对于第二个问题，我们专门设计了一个AS_SET关键字，如果在配 置命令的时候，将这个关键字激活，则BGP在汇总路由时，将携带上明细的AS_PATH属性，来进行防环。
[r4-bgp]aggregate 172.16.0.0 22 suppress-policy aa as-set
*> 172.16.0.0/22 127.0.0.1 0 {1 4}? --- 如果明细路由携带的AS_PATH属性不一样，则在激活了AS_SET属性后，汇总路由将会把明细路由的AS号都携带上并且用大括号括起来，之后，在进行防环的时候，里面所有AS号都将生效，都不能回传。但是，在使用AS_PATH属性进行选路的时候，当作一个AS来看待。因为聚合后的路由信息存在属性丢失问题，所以，这样的汇总路由需要格外的关注。
为此，我们为BGP专门引入了两个属性 --- ATOMIC_AGGREGATE，AGGREGATOR
ATOMIC_AGGREGATE --- 纯粹预警属性 --- 只有在抑制全部明细路由时才会携带
AGGREGATOR --- 将携带汇总者的RID以及其所在的AS号
Aggregator: AS 2, Aggregator ID 4.4.4.4, Atomic-aggregate
[r4]display bgp routing-table 172.16.0.0 --- 查看一条路由的详细情况
————————————————
版权声明：本文为CSDN博主「Xcgouge0972」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/m0_58462317/article/details/125962322
