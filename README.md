# Learning Blockchain
跟一些前辈交流之后，觉得区块链很可能是一种改变金融业格局的技术。但是之前接触到的都是一些比较零散的内容，导致我对区块链一直只有一点概念上的理解，对它的认识不够系统。之后希望能系统地、有规划地学习这一块的知识

做这个仓库主要有三个目的：
- 保存自己在学习区块链过程中看到的比较好的资料
- 记录我在学习区块链项目过程中的体会和心得
- 分享

希望通过对区块链技术、项目的学习，帮助自己理解这个新事物，理解区块链的逻辑。

需要说明的是，这个库主要用来帮助理解区块链的机制，没有涉及到区块链的编程。

## 资料
### 基础资料
- 普林斯顿大学的公开课: [Bitcoin and Cryptocurrency Technologies](https://www.coursera.org/learn/cryptocurrency/home/welcome)

    这个公开课很适合入门，讲了很多理解区块链所需要的基础知识，讲得也很清楚，节奏很好。 可以1.5倍速过一遍

- [区块链 - 中文资源](https://github.com/LiuBoyu/blockchain) 

    里面收集了很多文章、资料。翻一翻它的资源，对区块链的主要技术、发展脉络、主要项目能有一个大概的了解。我也会引用里面的一些资料文章。

- [白皮书集合](https://github.com/mipengchong/blockchain)

    收集了很多区块链白皮书，有很多中文版。

上述资料作为入门已经足够了。尤其是普林斯顿的公开课，我是看这个公开课入门的。这个公开课里面讲的内容，也是我之后提到的内容的基础。所以大家如果想顺利地看懂接下来的内容的话，建议先看看公开课的视频。**部分网址需要翻墙才能访问**

### 相关社区
- [巴比特](http://www.8btc.com/)
- [Ethfans](http://ethfans.org/)

### 补充资料：
- [区块链数字货币的9种共识机制比较 2018.1](https://zhuanlan.zhihu.com/p/32585236)
- [国内外区块链项目/联盟汇总 2017.03.16](https://www.jianshu.com/p/00e17ee7c646)
- [区块链理论学习入门指南 2017.8.24](https://daimajia.com/2017/08/24/how-to-start-blockchain-learning)
- [区块链核心技术演进之路－算法演进 2016.10.25](http://www.8btc.com/blockchain-tech-algorithm)
- [区块链核心技术演进之路 – 挖矿演进 2016.11.08](http://www.8btc.com/blockchain-tech-mining)
- [区块链核心技术演进之路-共识机制演进 2016.12.20](http://www.8btc.com/blockchain-tech-consensus-mechanism)

接下来的内容，是我在学习区块链过程中接触到的项目、概念和技术，主要会记录它们**独特**的地方。



---

## 目录
技术向：
- [跨链技术](https://github.com/Jasonbaby/Learning-Blockchain#%E8%B7%A8%E9%93%BE%E6%8A%80%E6%9C%AF%E4%BE%A7%E9%93%BE)
- [零币协议(Zerocoin protocol)](https://github.com/Jasonbaby/Learning-Blockchain#%E9%9B%B6%E5%B8%81%E5%8D%8F%E8%AE%AEzerocoin-protocol)
- [以太坊 Ethereum](https://github.com/Jasonbaby/Learning-Blockchain#%E4%BB%A5%E5%A4%AA%E5%9D%8A-ethereum)
- [EOS](https://github.com/Jasonbaby/Learning-Blockchain#eos)

应用向：
- [瑞波 Ripple](https://github.com/Jasonbaby/Learning-Blockchain#%E7%91%9E%E6%B3%A2-ripple)
- [比特股 BitShares](https://github.com/Jasonbaby/Learning-Blockchain#比特股-BitShares)
- [去中心化储存](https://github.com/Jasonbaby/Learning-Blockchain#%E5%8E%BB%E4%B8%AD%E5%BF%83%E5%8C%96%E5%AD%98%E5%82%A8)


---

## 跨链技术(侧链)
侧链(sidechains)是以锚定现有数字货币为基础的新型区块链，以融合的方式实现加密货币金融生态的目标。侧链可实现现有数字货币和其他帐簿资产在多个区块链间的转移。
这使用户能用他们已有的资产来使用新的加密货币系统。

此外，由于侧链是从父链中转移现有资产而不是另铸新资产，侧链不会引起未经授权的铸币，维护资产的安全和稀缺性依靠父链来实现。从而可避免出现与新货币相关的流动性短缺和市场波动。


参考资料:
- [区块链中一个重要的链：侧链](https://steemit.com/cn/@monkeyplayfire/62v4en)


### 相关项目及技术
#### *多重签名 Multi-sig*
多重签名技术侧链的基础，理解多重签名有利于理解侧链。
[密钥分存](https://en.wikipedia.org/wiki/Secret_sharing)是多重签名的技术基础。
[Bitcoin and Cryptocurrency Technologies](https://www.coursera.org/learn/cryptocurrency/home/welcome)第四周的课程中有相关介绍。

#### *[Blockstream](https://blockstream.com/technology/)*
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

#### *[Rootstock](https://www.rsk.co/)*
RootStock是一个建立在比特币区块链上的智能合约分布式平台。它是第一个和比特币实现双向挂钩的开源的智能合约平台。RSK没有发行任何代币，它通过和比特币联合挖矿，吸引矿工加入，**矿工挖矿的收入是手续费**。 RSK实现了以太坊虚拟机的一个改进版本，它将作为比特币的一个侧链。它的目标是，将复杂的智能合约实施为一个侧链，为核心比特币网络增加价值和功能。可以把RSK理解为在比特币侧链上实现的升级版以太坊。

联合挖矿是一种允许比特币矿工同时挖其他加密货币的技术，并且边际成本接近零。根链的挖矿设备和使用方法和挖比特币是一样的，这就可以让比特币矿工在挖比特币的同时挖根链。



- ##### 动态联合挖矿/联邦(Dynamic Hybrid Merged mining/Federation)
    根链使用DECOR+区块奖励共享方案，以减少竞争，并且允许矿工延时切换到根链的最佳区块。如果矿工在切换矿机算力时一个根链区块被挖到了，他们将获得一个完整的根链区块奖励。如果他们延迟了切换，并且还在旧区块链头部挖矿，他们就相当于创建了一个叔叔(uncles)块。(这个机制和以太坊的类似，之后再介绍以太坊的时候可以再详细了解。
)
    为了防止51%攻击，根链的矿工使用工作量证明挖矿会包含一个联邦检查点（federated checkpoints）。联邦检查点由注册过的联邦成员和客户组成，共同签名以决定最佳的区块链状态。

我理解的根链存在的逻辑是这样的：随着比特币区块奖励的减少，未来矿工的收入主要来自于交易的手续费。但是比特币交易速度太慢，最大为每秒七笔。若矿工为了维持收入，那么平均比特币交易的手续费将会激增。 减少平均每笔交易的手续费的方法，就是提高交易的数量。根链用侧链的方法，提高了交易速率。并且用联合挖矿的方法，保证了矿工参与的积极性。

参考资料:
- [根链平台(RootStock)——基于比特币驱动的智能合约白皮书(中文翻译)](http://www.8btc.com/tan90d84)

#### *[BTC Relay](http://btcrelay.org/)*
BTC Relay由ConsenSys团队推出，其主要原理是BTC Relay把以太坊网络与比特币网络以一种安全去中心化的方式连接起来。BTC Relay通过使用以太坊的智能合约功能可以允许用户在以太坊区块链上验证比特币交易。

不过从这个项目的[github](https://github.com/ethereum/btcrelay)更新状况来看，应该是已经凉了！我觉得他想法挺好的，凉了的原因可能是因为数字货币交易所基本都能实现各种数字货币之间的兑换，所以功能重叠了吧。

参考资料:
- [BTC-Relay与RootStock侧链技术对比](https://bytom.io/?p=15)


---


## 零币协议(Zerocoin protocol)
零币协议主要思想是[零基础证明](https://baike.baidu.com/item/%E9%9B%B6%E7%9F%A5%E8%AF%86%E8%AF%81%E6%98%8E)。

尽管比特币等数码货币以交易的隐蔽性著称，但在现实生活中却常常可以透过普通的比特币区块链的记录追踪交易，人们可以准确获知比特币的发送者和发送地点。零币协议可以实现以加密的形式交易原数据，而不是像比特币那样要将交易数据公布于大众，从而可实现非常高的匿名性。

[普林斯顿大学公开课](https://www.coursera.org/learn/cryptocurrency/home/week/6)有相关课程,讲解得也很详细。

### *[ZCash](https://z.cash/)*
ZEC是基于比特币0.11.2版本代码基础上进行修改的分支，保留了bitcoin原有的模式。和比特币不同，ZEC交易使用零知识证明的技术，自动隐藏区块链上所有交易的发送者、接受者和数额，从而实现交易绝对的匿名。[Github地址](https://github.com/zcash/zcash)

参考资料：
- [Zcash是什么？ - Leaf的回答 - 知乎](https://www.zhihu.com/question/51958283/answer/287647342)
- [有了深黑，市场真的需要纯黑吗？ ](http://8btc.com/thread-41384-1-1.html)

---



## [以太坊 Ethereum](https://ethereum.org/)
以太坊是一个开源的有智能合约功能的公共区块链平台，它允许任何人在平台中建立和使用通过区块链技术运行的去中心化应用。
以太坊狭义上是指一系列定义去中心化应用平台的协议，它的核心是以太坊虚拟机（“EVM”），可以执行任意复杂算法的编码。

关于以太坊平台的详细介绍，可见参考文献：
- [项目源码 github](https://github.com/ethereum/)
- [Ethfans.org中文文档](http://ethfans.org/wikis/Home)
- [维基百科](https://zh.wikipedia.org/wiki/%E4%BB%A5%E5%A4%AA%E5%9D%8A)
- [深入浅出以太坊](http://www.gxn.io/files/book/shenruqianchuyitaifang.pdf)

### 技术特点
#### *RLP*
递归长度前缀编码（RLP）是Ethereum中对象序列化的一个主要编码方式，起到穿针引线的作用，其目的是对任意嵌套的二进制数据的序列进行编码，这种编码格式将任意长度和纬度的字符串构成的数组串连接拼成字符串。


#### *MPT (Merkle Patricia Tree)*
MPT是以太坊中的一种加密认证的数据结构，可以用来存储所有的(key，value)对。
相比于传统的trie只有一种节点，以太坊增加了两个新的节点，称为叶节点和扩展节点；原来的节点称为分支节点。

MPT树能有效减少Trie树的深度，增加Trie树的平衡性。而且通过节点的hash值进行树的节点的链接，有助于提高树的安全性和可验证性。MPT树也导致了以太坊的Merkle Proof有别于比特币的。

#### *GHOST (Greedy Heaviest Observed Subtree protocol)*
“幽灵“协议（"Greedy Heaviest Observed Subtree" (GHOST) protocol）是由Yonatan Sompolinsky 和 Aviv Zohar在2013年12月引入的创新。幽灵协议提出的动机是当前快速确认的块链因为区块的高作废率而受到低安全性困扰； 
GHOST通过在计算哪条链“最长”的时候把废区块也包含进来；这就是说，不仅一个区块的父区块和更早的祖先块，祖先块的作废的后代区块（以太坊中称之为“叔区块”）也被加进来以计算哪一个区块拥有支持其的最大工作量证明。

以太坊付给以“叔区块”身份为新块确认作出贡献的废区块87.5%的奖励，把它们纳入计算的“侄子区块”将获得奖励的12.5%，不过，交易费用（手续费）不奖励给叔区块。
具体可见白皮书[对应章节](https://github.com/ethereum/wiki/wiki/White-Paper#modified-ghost-implementation)

这一块由于白皮书上描述不是很具体，所以我也不是很理解它这个机制。 待之后研究它源码的时候再回过头来补充内容。主要困惑的地方在于，既然叔块是有价值的，那么当矿工挖到一个区块的时候，是否可以复制这个区块到多台电脑上，使其他电脑的区块变为叔块，这样一来，获得的奖励不是很增加很多吗？

#### *Solidity*
Solidity是一种语法类似JavaScript的高级语言。它被设计成以编译的方式生成以太坊虚拟机代码。
[Github](https://github.com/ethereum/solidity)

关于上面提到的技术的细节，可见参考文献：
- [RLP](https://github.com/ethereum/wiki/wiki/%5B%E4%B8%AD%E6%96%87%5D-RLP)
- [Merkle Patricia Tree 维基百科](https://github.com/ethereum/wiki/wiki/Patricia-Tree)
- [Merkle Patricia Tree (MPT) 树详解](http://www.cnblogs.com/fengzhiwu/p/5584809.html)
- [Merkle Tree学习](http://www.cnblogs.com/fengzhiwu/p/5524324.html)

有意思的是，以太坊进行过数次硬分叉，其中一次分叉还是为了让被黑客盗取的以太币回归原处。这显然跟区块链上的数据不可逆转不可篡改的特性违背了



---


## [EOS](https://eos.io/)

EOS和ETH的愿景大致相似，一个操作系统的底层。相比于ETH，EOS为用户、开发者提供了更多的、更完善的底层功能和结构，有助于开发者在EOS方便快速地搭建他们的服务。

区块链应用最大的限制就是延迟和数据吞吐量，EOS通过并行链和DPOS的方式解决了延迟和数据吞吐量的难题，EOS通过并行链的方式，最高可以达到数百万TPS的数据吞吐量，并且并行本地链甚至可以达到毫秒级的确认速度。

- [Github](https://github.com/eosio)
- [白皮书 中文](https://link.jianshu.com/?t=http%3A%2F%2Fbtsabc.org%2Fportal.php%3Fmod%3Dattachment%26id%3D2196)
- [白皮书 英文](https://github.com/EOSIO/Documentation/blob/master/TechnicalWhitePaper.md)
- [解读《EOS.IO技术白皮书》](https://www.jianshu.com/p/bc489db794ce)
- [EOS：史诗级的区块链操作系统](https://www.jianshu.com/p/f65bf7691482)


### *并行链*
先占坑


---


## 瑞波 Ripple
瑞波（Ripple）是世界上第一个开放的支付网络，通过这个支付网络可以转账任意一种货币，简便易行快捷，费用几乎是零。 瑞波强调的不是“货币属性”而是“支付属性”。XRP的发行总数是固定的，在开始就被设定为1000亿个，不会再发行。

瑞波团队的领导层与其他虚拟货币也有不同，其他货币领导人大多是技术方面的大神，而Ripple的领导层则有很强的金融背景。Ripple更多是从业务层面做了创新。 

Ripple主要和[SWIFT](https://zh.wikipedia.org/wiki/%E7%8E%AF%E7%90%83%E9%93%B6%E8%A1%8C%E9%87%91%E8%9E%8D%E7%94%B5%E4%BF%A1%E5%8D%8F%E4%BC%9A)竞争。

[瑞波共识机制白皮书](https://ripple.com/files/ripple_consensus_whitepaper.pdf)

[瑞波 Github](https://github.com/ripple/rippled)

### 技术特点

#### *网关*
网关是资金进出瑞波（Ripple）系统的进出口。它像一个中介，人们可以通过这个中介将各类货币（不论是各国法币，还是比特币等虚拟货币）注入或抽离瑞波（Ripple）系统。这样的话，人们不需要再像以前那样（最初的瑞波系统只能让两个熟人之间转账），现在即使两个人互相是无信任的陌生人，只要他们两个人同时都信任同一个网关，这两人之间的转账就可以进行。如果“网关”是由大银行或大金融机构充任，那么这个信任链是很容易建立起来的。“网关”的引入解决了用户之间的转账不再局限于熟人之间，陌生人之间也可以进行。这也是为什么瑞波的主要合作伙伴是银行和机构（其他数字货币则以能上交易所为荣）

我是这么理解的，从A网关转钱到B网关，相当于在A网关挂了瑞波币买单，成交后在B网关挂瑞波币卖单。 这个过程中，网关是交易所、做市商的作用。这里网关和用户之间，是中心化的。然后应该也存在中某种机制，维持着网关和网关之间汇率的稳定。（感觉这个系统有很大的套利空间呀）

#### *瑞波币*
瑞波币（XRP）是瑞波（Ripple）系统内的流动性工具，是一个桥梁货币，是各类货币之间兑换的中间品。在瑞波（Ripple）系统内，不兑换成瑞波币（XRP）的话，就很难跨网关转账或提现;而瑞波币则可以在任意网关之间自由流通。瑞波币（XRP）的另外一个功能是阻止垃圾请求攻击，保障系统安全运行（每笔交易销毁万分之一瑞波）。

#### *瑞波共识机制*
瑞波共识算法使一组节点能够基于特殊节点列表形成共识。初始特殊节点列表就像一个俱乐部，要接纳一个新成员(Server)，必须由该俱乐部51%的会员投票通过。共识遵循这些核心成员的“51%权利”，外部人员则没有影响力。一个交易的确认需要获得该俱乐部成员至少80%的投票。由于该俱乐部由中心化开始，它将一直是中心化的。它的性能是以牺牲中心化的程度为代价的。

瑞波共识机制不像比特币的POW(Proof of Work)，是由部分服务器投票决定的，因此不需要矿工，资源消耗相对而言小很多。


参考资料：
[瑞波币与瑞波系统的运行机制](http://www.fx361.com/page/2016/1205/376236.shtml)

---


## [比特股 BitShares](https://bitshares.org/)
点对点的多态数字资产交易系统

### 技术特点
#### *石墨烯区块链库(graphene blockchain library)*
石墨烯是区块链工具组，由比特股团队cryptonomex开发，采用C++编写。 比特股(BitShare) 2.0版本基于石墨烯技术开发，性能得到了极大提升。

[Github](https://github.com/cryptonomex/graphene)

╮(╯▽╰)╭ 相关资料好少，不懂不懂。[官方文档](http://docs.bitshares.org/index.html)的介绍都好少。真难。。。



---



## 去中心化存储

### [IPFS](https://ipfs.io/)
- [白皮书.中文](https://gguoss.github.io/2017/05/28/ipfs/)
- [白皮书.英文](https://github.com/ipfs/papers/raw/master/ipfs-cap2pfs/ipfs-p2p-file-system.pdf)
### [Filecoin](https://filecoin.io/)
- [白皮书.中文](http://chainx.org/paper/index/index/id/13.html)
- [白皮书.英文](https://filecoin.io/filecoin.pdf)
### [BigChainDB](https://www.bigchaindb.com/)
- [白皮书.中文](http://blog.csdn.net/fengqing79/article/details/70154076)
- [白皮书.英文](https://www.bigchaindb.com/whitepaper/)

---

