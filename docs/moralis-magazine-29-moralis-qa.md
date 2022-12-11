# Moralis 杂志# 29–Moralis 问答

> 原文：<https://moralis.io/moralis-magazine-29-moralis-qa/>

我们(Moralis DAO)支持并使用现有的最健壮和最强大的 Web3 框架。

**Moralis 是一个强大的 Web3 框架**，但是作为 Moralis DAO，我们不仅仅是这样。我们希望通过为您提供快速构建应用程序所需的工具和组件来帮助您提升开发水平。

## **Web3 属于我们所有人……**

Web3 不是 Moralis 家发明的东西。尽管我们努力成为事实上的 Web3 框架，但 Web3 世界本身不属于我们(或任何人)——它属于我们所有人！如果你想成为这个惊人的全球变革的一部分，参与进来是很容易的；开始建造吧。Moralis 经过精心巧妙的设计，让您的 Web3 开发之旅更加舒适，效率更高。

今天就来看看我们的一些开源入门工具，亲眼看看 Moralis 适合你！

你在用 Moralis 建造什么？你卡住了吗？向我们提出问题和意见。谁知道呢，我们甚至可能会在未来的杂志上直接回复你！

[**发送您的问题给我们**](https://ivanontech.typeform.com/to/R9K5lnGe)

## **Moralis 家法师问&一个豪华！**

本周，我们深入挖掘了一些我们最近调查的最佳案例！如果我们没有回复您的问题，请随时再次发布！此外，我们的论坛还提供了更深入问题的答案和动手帮助。跳到最后一个链接，看一个论坛问题的很好的例子(仍然没有发布，这取决于你们中的一个人在这里采取下一步行动！)

Moralis 专家回答了以下问题，这些方法基于经验和测试。正如大多数发展中的事物一样，有不止一条路线可以达到相似的目的。我们希望这里提供的答案能帮助你在通往 Web3 成功的旅途中找到自己的道路！

问:没有真正的问题——只是想向团队传递更多的爱。感谢您支持我们

开发人员构建快速 dApps！

谢谢你的美言，Moralis 家法师！我们同样为能与你们所有人一起工作而自豪，请放心，我们只是刚刚开始。感谢所有阅读这篇文章的人成为 Moralis 的一部分！

**问:我怎样才能让我的 marketplace 拥有许多过滤器，类似于 Ninneko 和 Axie Infinity，以便使用 Moralis 在我们的 dApp 中搜索 NFT 的房产？**

答:一种选择是使用 React 之类的东西构建过滤器组件，然后您可以使用 Moralis 来检索 NFT 元数据(特别是 NFT 的属性),您的应用程序逻辑将在前端处理过滤。

或者，web3api 中直接有搜索功能，[https://docs . moralis . io/moralis-server/web 3-SDK/token # search nfts](https://docs.moralis.io/moralis-server/web3-sdk/token#searchnfts)！
使用这个开源模板，可以很容易地配置特定的集合和应用过滤器。

问:我从 Onramper 收到生产密钥后，下一步该做什么？

答:为此，您可以考虑从以太坊样板[https://github . com/ether eum-Boilerplate/ether eum-Boilerplate]开始，看看如何应用 Onramper 插件。或者，一旦添加到 Onramper 插件设置中，您可以自己应用它。

问:我正在用你的插件建立一个 DEX 网站，但是因为你的插件而停止了

**不支持保险丝网络。如果你能帮我添加保险丝网络，我将不胜感激。**

答:不幸的是，我们目前不支持 Fuse 网络。但是，将来我们计划引入对更多网络的支持。自托管选项稍后也将可用，可能有助于解决这一问题。

**问:如何将您的 dApp 与其他智能合约结合使用——我正在构建一个智能合约**

就像一个地址簿，如果能快速连接到你的 dApp 就太好了！

答:通过 Moralis，您可以使用自动同步来监听智能合同事件，然后围绕链上发生的新事件构建逻辑和触发器。

SDK 中还有专门针对契约交互的函数:Moralis.executeFunction 就是其中之一，更多详细信息请查看文档:https://docs . moralis . io/moralis-server/web 3/web 3 # execute function

问:我的梦想是用 Moralis 构建一个区块链 2D 游戏。

答:看看我们的一些游戏教程。游戏逻辑和图形用户界面是一个组件，你需要分别掌握(YouTube 有很多好的教程，试着搜索一下

“如何建造…”以一个类似于你有兴趣创建的游戏结尾)。第二个组成部分是 Web3 集成，

我们还没有制作出一款 2D 游戏专用的深潜，但是这两个教程会给你指明正确的方向:

https://www.youtube.com/watch?v=FhiQFkxUwQohttps://youtu.be/CsdhJrD9m1M

**问:如何将我的网站导入到我的 Moralis 服务器，并将其编辑为网站 3**

**项目？？**

答:您可以通过使用一些简单的 JavaScript 与 Moralis SDK 进行交互。

通读 Moralis 文档，看看你想使用哪些特性。

第一步是导入 Moralis SDK 并使用 SDK 中的函数

https://www.youtube.com/watch?v=MY4WYoZPr-U&ab_channel=MoralisWeb3

最后，我们以我们开头提到的例子收尾。有些问题虽然结构非常好，但对我们来说太长了，无法在这里回答。好消息是这对于我们的论坛来说是完美的！

**问:我看了 YouTube 上为 Web3 社交网络编码的视频(Reddit 克隆版)和**

我看到了这个网站(metafora.app ),我认为它有点类似。我有具体用途

**案例我想实施，但却被困在哪里找不到**的信息

**以下。未上市是什么意思？如何在智能合同中取消列表？)**

**工作？另外，Profile 是如何工作的？比如，它怎么知道向你(用户)显示**

**只有你的帖子？跟随是如何工作的？智能合约如何存储谁**

你在跟踪？有没有可能让其他事情不公开，比如你是谁

**以下？最后，如何删除文章？它是否只是“断开”消息**

**从 UI？有什么资源或地方可以帮我找到**

不胜感激。

答:法师们，使用以下链接查看这个问题是否已经发布到:

[https://forum . moralis . io/t/ether eum-social-media-boilerplate/4655/22](https://forum.moralis.io/t/ethereum-social-media-boilerplate/4655/22)(如果没有，就发帖开始讨论，到时见！)

你们每个人都是非凡事物的一部分，这本杂志就是要让 Moralis 的力量为你所用！

我们都是 Moralis 家，在这里互相支持。如果你不是已经活跃在[道貌岸然道不和](https://discord.com/invite/P9N9HF97hH)的话，今天就是让你登场的日子。

在 Moralis 道的冲突中，你会发现一堆 Moralis 专家和法师同伴。发布您的项目并从社区获得反馈，参与编码挑战，并了解最新的 Moralis 特性和更新。

* * *

### **下一关……**

准备好更进一步了吗？我们的 Moralis 专家 Ash 正在努力工作，为 Moralis Web3 游戏开发人员收集新的教程。下周他将带着全新的教程回来，只对《Moralis》杂志的订阅者开放。

![](img/1d3a45ad153a1620eaad3d7ea212e901.png)

如果你迫不及待地想开始，这里有一些由 Moralis 法师大卫最近制作的指南。准备好，我们要建立自己的网站 3 MMO！

https://youtu.be/5Bz-r1KBres

奖励 WEB3 游戏开发更新:Moralis 赞助 ETHGlobal BuildQuest 点击这里了解详情:[https://buildquest.ethglobal.com/](https://buildquest.ethglobal.com/)

你如何利用所提供的工具和专业知识取决于你自己，我们希望这本杂志能激发一些想法。

* * *

感谢阅读！我们希望本周的 Moralis 杂志对你有用。

继续建造！

下次见💚

Moralis 研究小组