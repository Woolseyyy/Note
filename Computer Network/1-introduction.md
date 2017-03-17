#CH1 - Introduction to Computer Network

## Network usage

### 商业应用

资源共享 resource sharing

 * 在网络中所有人都可以访问程序、设备，尤其是数据。共享物理设备、共享信息
 * 虚拟专用网络(VPN, virtual private network)
	 + 将不同地点的单个网络连接成一个可扩展网络
 * Server-Client 模型


通信媒介 communicarion medium
 
 - e-mail
 - IP telephony (如果用了Internet就是 VoIP, voice over IP)
 - 视频会议
 - Desk sharing
 - 远程医疗
电子商务 electronic commerce
##家庭应用
获取外界信息

- 获取信息的模式
	- Server-client
	- Peer-to-peer
		- 通常用于共享音乐和视频

人与人的通信

- e-mail 
- tweeter 
- tele learning 
- Facebook

电子商务

- 家庭购物 
- 网银
- 跳蚤市场

娱乐

普适计算 ubiquitous computing

- 大概就是物联网吧..给所有东西加上传感器并联网
- RFID(radio frequency Identification)技术

### 移动用户
 
 蜂窝网络 无线热点(hotspot)
 固定无线和移动无线的区别
 ![这里写图片描述](http://img.blog.csdn.net/20170317182513303?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvV29vbHNleXl5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

电话与Internet结合
移动商务(不如说移动支付 代替信用卡 美国人2000年提出的概念)
传感器网络
可穿戴计算机

## Network Hardware

### Transmission technology
Broadcast networks

- Unicasting 单播
- Broadcasting 广播
- Multicasting 组播
Point-to-point networks（Unicasting 单播）
注意，点对点链路和广播网络的区别不是行为上的区别，而是技术上的区别。点对点链路的信息在某一条路由上进行传播，而广播网络是所有机器都接到信息，然后自身判断要不要做出反应。广播网络也可以只对一个机器下达指令。这与broadcasting multicasting unicasting的不同有区别。这三种是行为层面上的区别。

### Scale
 ![这里写图片描述](http://img.blog.csdn.net/20170317182703180?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvV29vbHNleXl5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
Personal area networks(PAN)

- Bluetooth 
- RFID
Local area networks(LAN)

- (within a single building or campus of up to a few kilometers in size)
- 有线局域网&无线局域网
	- 局域网大小受限，所以最坏传输时间是有界的
	- 有线局域网速度快、延时低、错误少，所有性能都超过无线局域网·
- Topology 
	- 许多以点到点链路为基础
		- 交换式以太网(switched Ethernet)
			- Switch,  Port
			- VLAN(Virtual LAN)
	- 一条线性线缆上广播
		- 经典以太网(classic Ethernet)
- 静态设计和动态设计 - 如何分配信道
	- Static allocation
		- 将时间分为离散的时间间隔 轮询 每台机器只能在被分配到的时间槽（tiil slot）进行广播
	- Dynamic allocation（按需分配）
		- Centralized
		- Decentralized
- 家庭网络
	- 前景与应用
	- 所需具有的不同属性
		- 安装容易
		- 使用方便不易出错
		- 价格廉价
		- 从一两个设备扩展
		- 安全可靠
Metropolitan area network (MAN)

- Is basically a bigger version of a LAN and normally uses similar technology
- 如有线电视 WiMAX

Wide area network(WAN)
![这里写图片描述](http://img.blog.csdn.net/20170317183205093?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvV29vbHNleXl5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast) 

- Transmission lines
- Switching elements
- 与局域网的区别
	- 主机和子网由不同人运营
	- 路由器（router）通常连接不同类型的网络技术
	- 子网可以连接单个计算机 也可以连接整个局域网

Internet

- 不同且不兼容的网络连接起来成为互联网络(internet)
- 最有代表性的是全球范围的因特网(Internet)(注意要大写)
- 子网-网络-互联网的区别
	- 子网 广域网语境下， 广域网除了host之外的部分
	- 网络 利用单一技术相互连接在一起的计算机集合
	- 互联网 技术不同、运营者不同的网络连接在一起


## Network Software

 ![这里写图片描述](http://img.blog.csdn.net/20170317183530114?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvV29vbHNleXl5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

- Protocol hierarchies
	- Protocol
	- Peers
	- Network architecture
		- Interface need not be the same
	- Protocol stack
- Layer design issues
	- Network reliability
		- 检错、纠错
		- Routing  选择一条合适的线路
	- Network evolution
	- Network resource allocation
		- 统计复用 根据需求动态共享带宽
		- 流量控制
		- 服务质量
	- Network security
		- 保密性机制
		- 完整性机制
- Service issues
	- Connection-oriented service
		- (Messages are in order)
		- 先建立管道通信 再发送信息
	- Connectionless service
		- 直接发送带有地址的信息
		- (Messages can be out of any order
		- Unreliable datagram (electronic junk mail
		- Acknowledged datagram(registered mail
 ![这里写图片描述](http://img.blog.csdn.net/20170317183759404?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvV29vbHNleXl5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
 
- 服务原语 Service primitives
  ![这里写图片描述](http://img.blog.csdn.net/20170317183828701?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvV29vbHNleXl5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
  
 ![这里写图片描述](http://img.blog.csdn.net/20170317183910088?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvV29vbHNleXl5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
 
 
- 服务和协议的关系
![这里写图片描述](http://img.blog.csdn.net/20170317184036464?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvV29vbHNleXl5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


## Reference models

### OSI reference model
 ![这里写图片描述](http://img.blog.csdn.net/20170317184229998?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvV29vbHNleXl5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
#### Principle:

- Different abstraction is needed
- Each layer should perform a well-defined function
- 每一层的功能选择要像国际标准化目标看齐
- Minimize 层与层的划分要使得跨越接口的信息流 
- 层数要足够多，使得不同功能不会混在同一层中 但层数又不能太多 使得体系机构太过庞大
 
#### 各层
Physical layer:关注在一条通信信道上传输原始比特

- 确保收到的比特是准确的
- 什么电子信号来表示1/0 一个比特持续多少纳秒 传输是否可以在两个方向上同时进行 初始链接如何建立 双方结束之后如何撤销链接 网络连接器有多少针以及每一针的用途是什么
- 主要涉及 机械 电子 时序接口 物理传输介质

Data link layer 

- 主要解决两个问题 
	- 使传输没有漏检传输错误 
	- 流量调节 防止快速发送方用数据“淹没”慢速接收方

Network layer: concerned with controlling the operation of the subnet

- How to route packets from source to destination 
	- Routes can be based on static tables
	- They can be determined at the start of each connection
	- Highly dynamic
- How to control congestion(拥堵)
- 兼容不同协议 使得不同协议的网络可以互相通讯

Transport layer: split data up into smaller units if necessary, pass them to network layer

- How to make the multiplexing(多路复用) transport to the session layer
- Determine the type of service
- Which message belongs to which connection
- Regulate 

Session layer

- Dialog control, token management, synchronization

Presentation layer: concerned with the syntax and semantics of the information 

Application layer
 
### TCP/IP
 ![这里写图片描述](http://img.blog.csdn.net/20170317184802689?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvV29vbHNleXl5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
 
Host-to-network layer

- 不是真正意义上的层 而是主机与传输线路之间的一个接口
Internet layer

- 允许主机将数据包注入到任何网络 并且让这些包独立到达目的地
Transport layer

- 传输控制协议（TCP， Transport Control Protocol）
	- 将数据分割打包用于传输
	- 流量控制
- 用户数据报协议（UDP， User Datagram Protocol）

Application layer
![这里写图片描述](http://img.blog.csdn.net/20170317184854179?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvV29vbHNleXl5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
 
 
### 混合模型
 ![这里写图片描述](http://img.blog.csdn.net/20170317184913899?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvV29vbHNleXl5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
 
 
#### Comparison
Similarities 

- Protocols stack 都以协议栈概念为基础
- Layer functionality is similar
- 传输层之上的各层都是面向用户面向应用的

Difference

- OSI先有模型后有协议 通用性高 模型很漂亮但不实用
- TCP/IP先有协议后有模型 
- 层数不同 7 - 4
- 无连接和面向连接领域有所不同

OSI

- Bad timing
- Bad technology
	- 有两层是空的
	- 服务定义和标准十分复杂 难以实现并低效 
	- 层与层之间功能重复
- Bad implementation
	- 笨拙 效率慢
- Bad politics
	- 政府推行

TCP/IP

- 没有明确区分服务 接口 协议 的概念
- 模型不通用
- 接口和层没有明确区分
- 没有区分物理层和数据链路层
- 有部分流行的协议有设计缺陷 很落后
 
 
 
 

