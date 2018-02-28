# BlockChain_learning
跟一些前辈交流之后，我觉得区块链很可能是一种改变金融业格局的技术。但是之前接触到的都是一些比较零散的内容，导致我对区块链一直只有一点概念上的理解，对它的认识不够系统。之后希望能系统地、有规划地学习这一块的知识

做这个仓库主要有三个目的：
- 保存自己在学习区块链过程中看到的比较好的资料
- 记录我在学习区块链项目过程中的体会和心得
- 分享

希望通过对于区块链技术、项目的学习，能够帮助自己理解这个新事物

## 资料
普林斯顿大学的公开课: [Bitcoin and Cryptocurrency Technologies](https://www.coursera.org/learn/cryptocurrency/home/welcome)，这个公开课很适合入门。

[区块链 - 中文资源](https://github.com/LiuBoyu/blockchain)  里面收集了很多文章、资料

上述两个资料作为入门已经足够了。

接下来，让我们学习区块链的项目，理解每个平台和技术的独特魅力吧




## 以太坊 ethereum
以太坊是一个开源的有智能合约功能的公共区块链平台，它允许任何人在平台中建立和使用通过区块链技术运行的去中心化应用。

以太坊狭义上是指一系列定义去中心化应用平台的协议，它的核心是以太坊虚拟机（“EVM”），可以执行任意复杂算法的编码。

关于以太坊平台的详细介绍，可见参考文献：
- [深入浅出以太坊](http://www.gxn.io/files/book/shenruqianchuyitaifang.pdf)
- [维基百科](https://zh.wikipedia.org/wiki/%E4%BB%A5%E5%A4%AA%E5%9D%8A)

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