# Welcome to EosVoteChain
由于投票是一个需要强去中心化，保密性的可信性质选举机制。所以投票系统是最有价值利用区块链来实现的功能之一。
因此团队决定开发一款专门服务于对去中心化投票有需求群体的基于EOS的投票DAPP。



## EosVoteChain的优势
### 安全性，去中心化性
区块链本身的加密，出块体系决定了投票DAPP的不可篡改性
### 免费
EOS区块链中执行操作是完全免费的，所以投票也可以实现为只需要占用用户少量CPU的操作。（CPU会随着时间全部释放回账户中）
### 快速
由于大多数投票是具有时效性，有截止时间。为了确保在截止时间之前所有投票均为有效有票，区块链的出块速度就是一个很重要的影响因素。
### 透明
对于记名投票的方式，EOS区块链可以很好的追查到所有投票人的账户等信息。


## 项目规划
EosVoteChain将会致力于投票系统的开发，主要项目将围绕投票展开。
### 1、投票游戏
投票游戏的形式将非常简单易懂，其游戏规则如下：
#### 1.1游戏规则
投票游戏将持续某个固定时间。在游戏时间内，用户可以为各个选项进行投票。时间到达指定时间之后游戏结束，用户不可以再继续投票。此时票数最多的选项获胜。除此选项外的票将分配给选择了胜出选项的账户。
#### 1.2如何投票
用户将票以token的形式转移给合约账户，并在备注信息里标注想要投票的选项。
例如：
想要投票给选项A 100票，则只需：
转账100票给合约账户，备注"A"。
#### 1.3如何获得投票
游戏期间，每个用户都可以在指定票池里使用EOS进行票的兑换。
设代币符号为：VOTE，总量为十亿票（精确到小数点后四位）。

![兑换价格公式](https://github.com/eosvotechain/eosvotechain.github.io/blob/master/pic/price_function.png?raw=true)

兑换价格变化趋势如下图：

![兑换价格变化趋势](https://github.com/eosvotechain/eosvotechain.github.io/blob/master/pic/function_pic.png?raw=true)
也就是说每票的价格会随着票池里面剩余票数变化而变化。且可以随时以当前实时价格进行买入和卖出。且每次交易均收取1%服务费以防止恶意刷票。

### 2、自定义投票
本项目将支持用户自定义的投票形式。任何用户可以发起投票，参与投票。
#### 2.1 记名投票
记名投票，顾名思义，就是将投票者信息全部公开的投票系统。且每个eos账户名可以且只可以投出一票。
#### 2.2 匿名投票
匿名投票，这里指的是尽可能地隐藏投票者信息的投票系统。且每个eos账户名可以且只可以投出一票。匿名投票将在整个投票系统运行活跃度比较高的情况下投入使用。
#### 2.3 token记名投票
token投票，指的是用户将指定token转移到合约，作为投票的数量依据。记名含义同2.1
#### 2.4 token匿名投票
token投票含义同2.3。匿名含义以及规则同2.2。
