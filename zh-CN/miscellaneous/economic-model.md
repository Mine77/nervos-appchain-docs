# 经济模型 {docsify-ignore-all}

## Token设计概述
一个Token通常应该包括如下三个维度的设计

 - 内在用途
 - 存在目的
 - 发行机制

内在用途代表只能用该Token完成的工作，它是该Token的价值来源。例如法币，其内在用途就是法币发行方可控范围内唯一合法的税收单位，也因此法币具备保存和流通价值。例如比特币的内在用途就是矿工费用的记账单位，EOS的内在用途就是系统资源的使用比率。

存在的目的表示运营方设置该Token的目的，例如提高系统可用性和安全性（比特币、以太坊），或者提高持币人的参与度（网易星球积分等）。

发行机制包含发行总量是否受限、是否提供出块奖励、是否空投等。

一个优秀的Token设计应该满足：

 - 对所有参与方提供恰当、持续的激励
 - 促使矿工对外提供稳定可靠的服务
 - 使用者难以发起DDOS攻击

## 参与方
Nervos-CITA链上存在链运营方、记账人、开发者、终端用户等四个参与方角色。其中运营方、记账人、开发者角色可能由同一方承担，但更普遍的情况是他们是有独立利益诉求的参与方。

### 运营方
促使区块链网络提供稳定的记账服务，维护区块链浏览器等生态服务是运营方的基础诉求。随着区块链网络上积累的DAPP和用户数量越来越多，运营方通过**预分配代币**、**交易手续费**、**交易所**等盈利模式获得收益。

### 记账人
通常意义上的“矿工”。他们的诉求是获得超过记账成本外的收益。即记账收益或预期收益大于电费和基础设施投入的成本即可。因此，理论上只要交易手续费足以超过矿工成本，区块链是不需要“**出块奖励**”的。

### 开发者
开发者开发DAPP对外服务，他一方面希望区块链提供开放、稳定的基础设施，另一方面希望区块链生态中有大量的用户。为了使用区块链网络，开发者需要支付DAPP的“**部署费用**”，同时，为了降低用户门槛，开发者希望他的用户可以**免费地**使用区块链。

### 终端用户
终端用户使用开发者提供的DAPP。古典互联网用户一般不需要为互联网服务付费，在区块链网络中，用户也不应该为基础服务付费。

## 推荐的经济模型

### 改进的以太坊经济模型

假设运营方、矿工和DAPP开发者分属不同的参与方。那么如下的模型比较符合我们的要求。

- 运营方提供运营、宣传、推广工作并发行Token
- DAPP开发者使用区块链平台、购买Token
- 用户使用DAPP时自动获得开发者提供的少量Token，以维持其正常业务需求
 - 例如用户注册时可以获得开发者的少量Token
- 用户发起交易支付Token作为手续费
- 矿工收集手续费，运营方回购或者DAPP开发者购买，以实现价值流转

### 参与方混合模型

“改进的以太坊经济模型”仅仅用来实现“稳定可靠的区块链平台”这样一个目标设计的。如果区块链的矿工完全由运营方或运营方的联盟来运行，则不需要对矿工提供链上激励机制。此时需要考虑的是这个Token的其他功能，比如注意力等。

- 矿工“无偿”工作，维护系统稳定
- 运营方发行应用代币，用来支付其核心应用的费用（例如版权费等）
- 消费者购买应用代币，获得系统服务
