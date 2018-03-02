# BlockChain_learning
跟一些前辈交流之后，觉得区块链很可能是一种改变金融业格局的技术。但是之前接触到的都是一些比较零散的内容，导致我对区块链一直只有一点概念上的理解，对它的认识不够系统。之后希望能系统地、有规划地学习这一块的知识

做这个仓库主要有三个目的：
- 保存自己在学习区块链过程中看到的比较好的资料
- 记录我在学习区块链项目过程中的体会和心得
- 分享

希望通过对区块链技术、项目的学习，帮助自己理解这个新事物，理解区块链的逻辑

## 资料
### 基础资料
- 普林斯顿大学的公开课: [Bitcoin and Cryptocurrency Technologies](https://www.coursera.org/learn/cryptocurrency/home/welcome)

    这个公开课很适合入门，讲了很多理解区块链所需要的基础知识，讲得也很清楚，节奏很好。 可以1.5倍速过一遍

- [区块链 - 中文资源](https://github.com/LiuBoyu/blockchain)  
    里面收集了很多文章、资料。翻一翻它的资源，对区块链的主要技术、发展脉络、主要项目能有一个大概的了解

上述两个资料作为入门已经足够了。同时，上述两个资料所包含的内容，也是我之后所记录的内容的基础。**部分网址需要翻墙才能访问**

### 相关社区
- [巴比特](http://www.8btc.com/)
- [Ethfans](http://ethfans.org/)



接下来的内容，是我在学习区块链过程中接触到的项目、概念和技术，主要会记录它们**独特**的地方。

内容按照时间顺序罗列，所以看上去可能会有些混乱。不过不用担心，每当内容多到一定程度，我都会认真整理一次的，力求简洁明了。

---

## 跨链技术(侧链)
侧链(sidechains)是以锚定现有数字货币为基础的新型区块链，以融合的方式实现加密货币金融生态的目标。侧链可实现现有数字货币和其他帐簿资产在多个区块链间的转移。
这使用户能用他们已有的资产来使用新的加密货币系统。

此外，由于侧链是从父链中转移现有资产而不是另铸新资产，侧链不会引起未经授权的铸币，维护资产的安全和稀缺性依靠父链来实现。从而可避免出现与新货币相关的流动性短缺和市场波动。


参考资料:
- [区块链中一个重要的链：侧链](https://steemit.com/cn/@monkeyplayfire/62v4en)
- [根链平台(RootStock)——基于比特币驱动的智能合约白皮书(中文翻译)](http://www.8btc.com/tan90d84)

### 相关项目及技术
#### 多重签名 Multi-sig
多重签名技术侧链的基础，理解多重签名有利于理解侧链。
[密钥分存](https://en.wikipedia.org/wiki/Secret_sharing)是多重签名的技术基础。
[Bitcoin and Cryptocurrency Technologies](https://www.coursera.org/learn/cryptocurrency/home/welcome)第四周的课程中有相关介绍。

#### [Blockstream](https://blockstream.com/technology/)
BlockStream公司由比特币核心开发团队成立。该公司提出侧链协议，即把比特币转出比特币区块链、另行开发二代区块链，一来保证比特币区块链的安全，二来应对二代币的冲击，针对不同应用场景实现商业化。
- ##### 楔入式侧链(Pegged Sidechains)
    [Pegged Sidechains 白皮书(英文)](https://blockstream.com/technology/sidechains.pdf)

    [Pegged Sidechains 白皮书(翻译版)](http://www.8btc.com/enabling-blockchain-innovations-with-pegged-sidechains-abstract-introduction)

    楔入式侧链的技术基础称作双向楔入，流程大概如下(具体可见白皮书第2、3节)：

    ![双向楔入](https://steemitimages.com/0x0/http://upload-images.jianshu.io/upload_images/1698588-632a3bbe1874c5d0.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- ##### 闪电网络(Lightning Network)
    闪电网络是由BlockStream公司提出的一个支持高容量、及时交易的小额支付系统。闪电网络在链下实现点对点微支付，原先比特币处理能力的瓶颈被彻底打破，时延、最终性、容量甚至隐私问题也迎刃而解。它是基于微支付通道演进而来，创造性的设计出了两种类型的交易合约：序列到期可撤销合约RSMC（Revocable Sequence Maturity Contract，哈希时间锁定合约HTLC（Hashed Timelock Contract）。
    
    详情可见：
    - [详解闪电网络](http://www.8btc.com/ln-rn-corda)
    - [The Bitcoin Lightning Network:Scalable Off-Chain Instant Payments](http://lightning.network/lightning-network-paper.pdf)

#### [Rootstock](https://www.rsk.co/)
RootStock是一个建立在比特币区块链上的智能合约分布式平台。它是第一个和比特币实现双向挂钩的开源的智能合约平台。RSK没有发行任何代币，它通过和比特币联合挖矿，吸引矿工加入，**矿工挖矿的收入是手续费**。 RSK实现了以太坊虚拟机的一个改进版本，它将作为比特币的一个侧链。它的目标是，将复杂的智能合约实施为一个侧链，为核心比特币网络增加价值和功能。可以把RSK理解为在比特币侧链上实现的升级版以太坊。

联合挖矿是一种允许比特币矿工同时挖其他加密货币的技术，并且边际成本接近零。根链的挖矿设备和使用方法和挖比特币是一样的，这就可以让比特币矿工在挖比特币的同时挖根链。



- ##### 动态联合挖矿/联邦(Dynamic Hybrid Merged mining/Federation)
    根链使用DECOR+区块奖励共享方案，以减少竞争，并且允许矿工延时切换到根链的最佳区块。如果矿工在切换矿机算力时一个根链区块被挖到了，他们将获得一个完整的根链区块奖励。如果他们延迟了切换，并且还在旧区块链头部挖矿，他们就相当于创建了一个叔叔(uncles)块。为了防止51%攻击，根链的矿工使用工作量证明挖矿会包含一个联邦检查点（federated checkpoints）。联邦检查点由注册过的联邦成员和客户组成，共同签名以决定最佳的区块链状态。

我理解的根链存在的逻辑是这样的：随着比特币区块奖励的减少，未来矿工的收入主要来自于交易的手续费。但是比特币交易速度太慢，最大为每秒七笔。若矿工为了维持收入，那么平均比特币交易的手续费将会激增。 减少平均每笔交易的手续费的方法，就是提高交易的数量。根链用侧链的方法，提高了交易速率。并且用联合挖矿的方法，保证了矿工参与的积极性。



#### [BTC Relay](http://btcrelay.org/)
BTC Relay由ConsenSys团队推出，其主要原理是BTC Relay把以太坊网络与比特币网络以一种安全去中心化的方式连接起来。BTC Relay通过使用以太坊的智能合约功能可以允许用户在以太坊区块链上验证比特币交易。

不过从这个项目的[github](https://github.com/ethereum/btcrelay)更新状况来看，应该是已经凉了！

参考资料:
- [BTC-Relay与RootStock侧链技术对比](https://bytom.io/?p=15)


---




## 以太坊 Ethereum
以太坊是一个开源的有智能合约功能的公共区块链平台，它允许任何人在平台中建立和使用通过区块链技术运行的去中心化应用。
以太坊狭义上是指一系列定义去中心化应用平台的协议，它的核心是以太坊虚拟机（“EVM”），可以执行任意复杂算法的编码。

关于以太坊平台的详细介绍，可见参考文献：
- [项目源码 github](https://github.com/ethereum/go-ethereum)
- [Ethfans.org中文文档](http://ethfans.org/wikis/Home)
- [维基百科](https://zh.wikipedia.org/wiki/%E4%BB%A5%E5%A4%AA%E5%9D%8A)
- [深入浅出以太坊](http://www.gxn.io/files/book/shenruqianchuyitaifang.pdf)
### 技术特点
#### RLP
递归长度前缀编码（RLP）是Ethereum中对象序列化的一个主要编码方式，起到穿针引线的作用，其目的是对任意嵌套的二进制数据的序列进行编码，这种编码格式将任意长度和纬度的字符串构成的数组串连接拼成字符串。


#### MPT (Merkle Patricia Tree)
MPT是以太坊中的一种加密认证的数据结构，可以用来存储所有的(key，value)对。
相比于传统的trie只有一种节点，以太坊增加了两个新的节点，称为叶节点和扩展节点；原来的节点称为分支节点。

MPT树能有效减少Trie树的深度，增加Trie树的平衡性。而且通过节点的hash值进行树的节点的链接，有助于提高树的安全性和可验证性。MPT树也导致了以太坊的Merkle Proof有别于比特币的。

#### GHOST (Greedy Heaviest Observed Subtree protocol)
“幽灵“协议（"Greedy Heaviest Observed Subtree" (GHOST) protocol）是由Yonatan Sompolinsky 和 Aviv Zohar在2013年12月引入的创新。幽灵协议提出的动机是当前快速确认的块链因为区块的高作废率而受到低安全性困扰； 
GHOST通过在计算哪条链“最长”的时候把废区块也包含进来；这就是说，不仅一个区块的父区块和更早的祖先块，祖先块的作废的后代区块（以太坊中称之为“叔区块”）也被加进来以计算哪一个区块拥有支持其的最大工作量证明。

以太坊付给以“叔区块”身份为新块确认作出贡献的废区块87.5%的奖励，把它们纳入计算的“侄子区块”将获得奖励的12.5%，不过，交易费用（手续费）不奖励给叔区块。
具体可见白皮书[对应章节](https://github.com/ethereum/wiki/wiki/White-Paper#modified-ghost-implementation)

这一块由于白皮书上描述不是很具体，所以我也不是很理解它这个机制。 待之后研究它源码的时候再回过头来补充内容

关于上面提到的技术的细节，可见参考文献：
- [RLP](https://github.com/ethereum/wiki/wiki/%5B%E4%B8%AD%E6%96%87%5D-RLP)
- [Merkle Patricia Tree 维基百科](https://github.com/ethereum/wiki/wiki/Patricia-Tree)
- [Merkle Patricia Tree (MPT) 树详解](http://www.cnblogs.com/fengzhiwu/p/5584809.html)
- [Merkle Tree学习](http://www.cnblogs.com/fengzhiwu/p/5524324.html)

有意思的是，以太坊进行过数次硬分叉，其中一次分叉还是为了让被黑客盗取的以太币回归原处。这显然跟区块链上的数据不可逆转不可篡改的特性违背了

---



## 瑞波 Ripple
[瑞波共识机制白皮书](https://ripple.com/files/ripple_consensus_whitepaper.pdf)

[瑞波 Github](https://github.com/ripple/rippled)

