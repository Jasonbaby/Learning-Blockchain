# BlockChain_learning
跟一些前辈交流之后，觉得区块链很可能是一种改变金融业格局的技术。但是之前接触到的都是一些比较零散的内容，导致我对区块链一直只有一点概念上的理解，对它的认识不够系统。之后希望能系统地、有规划地学习这一块的知识

做这个仓库主要有三个目的：
- 保存自己在学习区块链过程中看到的比较好的资料
- 记录我在学习区块链项目过程中的体会和心得
- 分享

希望通过对区块链技术、项目的学习，帮助自己理解这个新事物，理解区块链的逻辑

## 资料
普林斯顿大学的公开课: [Bitcoin and Cryptocurrency Technologies](https://www.coursera.org/learn/cryptocurrency/home/welcome)，这个公开课很适合入门。

[区块链 - 中文资源](https://github.com/LiuBoyu/blockchain)  里面收集了很多文章、资料

上述两个资料作为入门已经足够了。同时，上述两个资料所包含的内容，也是我之后所记录的内容的基础。

部分网址需要翻墙才能访问

接下来的内容，是我在学习区块链过程中接触到的项目、概念和技术，主要会记录它们独特的地方。

内容按照时间顺序罗列，所以看上去可能会有些混乱。不过不用担心，每当内容多到一定程度，我都会认真整理一次的，力求简洁明了。

---

## 跨链技术(侧链)
侧链(sidechains)是以锚定现有数字货币为基础的新型区块链，以融合的方式实现加密货币金融生态的目标。侧链可实现现有数字货币和其他帐簿资产在多个区块链间的转移。
这使用户能用他们已有的资产来使用新的加密货币系统。

此外，由于侧链是从父链中转移现有资产而不是另铸新资产，侧链不会引起未经授权的铸币，维护资产的安全和稀缺性依靠父链来实现。从而可避免出现与新货币相关的流动性短缺和市场波动。

侧链简介：[区块链中一个重要的链：侧链](https://steemit.com/cn/@monkeyplayfire/62v4en)


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
    楔入式侧链的技术基础称作双向楔入，流程如下(具体可见白皮书第2、3节)：
    ![双向楔入](https://steemitimages.com/0x0/http://upload-images.jianshu.io/upload_images/1698588-632a3bbe1874c5d0.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- ##### 闪电网络(Lightning Network)



#### [Rootstock](https://www.rsk.co/)
#### [BTC Relay](http://btcrelay.org/)






参考资料：
- [巴比特侧链专辑](http://8btc.com/topic-sidechain.html)


---


## 以太坊 Ethereum
以太坊是一个开源的有智能合约功能的公共区块链平台，它允许任何人在平台中建立和使用通过区块链技术运行的去中心化应用。

以太坊狭义上是指一系列定义去中心化应用平台的协议，它的核心是以太坊虚拟机（“EVM”），可以执行任意复杂算法的编码。

关于以太坊平台的详细介绍，可见参考文献：
- [项目源码 github](https://github.com/ethereum/go-ethereum)
- [以太坊官网文档中文版](http://book.8btc.com/books/6/ethereum/_book/)
- [维基百科](https://zh.wikipedia.org/wiki/%E4%BB%A5%E5%A4%AA%E5%9D%8A)
- [深入浅出以太坊](http://www.gxn.io/files/book/shenruqianchuyitaifang.pdf)
### 技术特点
#### RLP
递归长度前缀编码（RLP）是Ethereum中对象序列化的一个主要编码方式，起到穿针引线的作用，其目的是对任意嵌套的二进制数据的序列进行编码，这种编码格式将任意长度和纬度的字符串构成的数组串连接拼成字符串。


#### MPT (Merkle Patricia Tree)
MPT是以太坊中的一种加密认证的数据结构，可以用来存储所有的(key，value)对。

相比于传统的trie只有一种节点，以太坊增加了两个新的节点，称为叶节点和扩展节点；原来的节点称为分支节点。

MPT树能有效减少Trie树的深度，增加Trie树的平衡性。而且通过节点的hash值进行树的节点的链接，有助于提高树的安全性和可验证性。



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

