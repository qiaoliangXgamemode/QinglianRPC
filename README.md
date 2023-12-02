# XoRPC Qiangliang

## 青联RPC
XoRPC是青联应用之一，基于基础的网络编程实现，协助网络传输。可用于Minecraft联机、点对点通信。

青联RPC 分为 RPC 和 RPC PLUS 版本

青联RPC PLUS 是在青联做上组网，目前未实现，实现后也是自己使用。

据我所知一些游戏好友，青联RPC 更适用于广大Minecraft玩家所用。

（本身此青联RPC和RPC PLUS的用途是自身团队所用）
### 目录

* [开发状态](#开发状态)
* [设计图](#设计图)
    * [思路](#思路)
* [计划表](#计划表)
    * [保持计划](#保持计划)
    * [其他](#其他)
    * [基本](#基本)
* [赞助](#赞助)

## 开发状态
个人：由于本人是封闭式管理高中，此项目是初三写剩下的，可能不定期维护；加上本人是美术生，更多时间放在学习与练习之中。

项目：对于本项目，我有候选人，预计明年此项目是三人共同编写。后期我会退出一段时间，之后再回来。

维护性： 我早已做成模块化形式，满足效率与维护性高。

## 设计图
![Design](https://github.com/qiaoliangXgamemode/QinglianRPC/blob/main/design.png?raw=true)
![DDD](https://github.com/qiaoliangXgamemode/QinglianRPC/blob/main/DDD.png?raw=true)

## Node (服务节点注册)代码示例
```
   var Config cfg.ServerConfig
	// 节点ID
	Config.ServiceID = 1
	// 节点名称
	Config.ServiceName = "服务器节点1"
	// 节点权重
	Config.Serviceweight = 1
	// 节点通信加密
	Config.ServiceEncrypt = true
	// 节点过滤器
	Config.ServiceFilter = true
	// 节点过滤器类型
	// Minecraft 节点只专注于minecraft的数据
	Config.ServiceFiltertype = "minecraft"
	// 节点公开的验证密钥
	Config.PublicToken = "1bb8snhasd(Habv)"
	// 节点私密的验证密钥
	Config.PrivateToken = "G9sdb&Ubvsad0GH*Jwds2rt4t59ndc0cn+112s.Nsm234"
	// 节点Hash唯一
	Config.ServiceGroupHash = "1dsf"
	// 广域网(可选)
	Config.Node_widearea_spDimain = {
		0:"193.22.45.111"
	}
	// 公域网(可选)
	Config.Node_public_spDimain = {}
	// 绑定地址
	// Config.NodeIPV6 = "fe80::973e:1e65:a21e:c3f3"
	Config.NodeIPV4 = "0.0.0.0"
	// 通信协议
	Config.Protocol = "UDP"
	// 绑定端口 (UDP)
	Config.SerNodePort = 2333
	// Config.conn
	// 是否启用节点流量转发
	Config.TranspondForwar = 1
	// 流量转发端口绑定 （TCP） | 可以分开UDP和TCP
	Config.TranspondForwarPort = 10086
	XoServerNode := XoRPC.NewServerXORPC(Config)
	XoRPC.LogsConfigServer(XoServerNode)
	XoServerNode.Server(4)
```
### 思路
NAT

## 计划表
- [ ] 支持IPV6
- [ ] 支持QUIC协议
- [ ] 支持免费服务器服务
- [ ] 实现自己一套多路复用方案
- [ ] 支持VarInt过滤器，用于 Minecraft
- [ ] 支持节点之间中转数据
- [ ] 额外开发用于想贡献服务器宽带作为给用户带来更好体验的版本（审核机制严格，国外服务器一律不需要）
- [ ] 支持UPNP
- [ ] 支持ICMP隧道
- [ ] 更好的网络延迟计算公式
- [ ] （空想）通过DNS加密获取双方NAT

### 保持计划
1. 逐步实现区块链无中心化，让更多人受益。
2. 保持对Minecraft游戏体验支持。
3. 合作更多人，立志于提供更好服务。

### 其他
1. 用于 青联 - 院块简 （给学校弄的玩意）多人编辑表格和文档之中

### 基本
- [x] AES加密
- [x] KCP协议应用
## 赞助
爱发电地址：https://afdian.net/a/Buserpi

我们立志于给任何用户带来更好体验，团队内部时刻保持透明、晴朗。

对于大部分计划，始终公开透明。
