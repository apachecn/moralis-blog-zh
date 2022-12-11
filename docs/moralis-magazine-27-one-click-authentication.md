# Moralis 杂志# 27–一键认证

> 原文：<https://moralis.io/moralis-magazine-27-one-click-authentication/>

如果你不去要求，你怎么能得到你想要的呢？

通常在销售和生活中，你永远不会得到比你努力争取的更多的东西。这就是为什么在 Moralis，我们强调“大胆大胆的大目标”的重要性对一些人来说，这些基准似乎无法达到，甚至是可笑的。我们这样做是因为我们明白不努力变得不可思议的伟大的后果；接受平庸。

作为一个 Moralis 家法师，你是一类精英开发者中的一员；您有特权，或者更确切地说，有权利宣布什么协议、什么集成和什么方法对您来说是重要的。Moralis 随时准备适应您的需求和整个 Web3 社区的需求；让我们来看看如何…

你在用 Moralis 建造什么？你卡住了吗？向我们提出问题和意见。谁知道呢，我们甚至可能会在未来的杂志上直接回复你！

[**发送您的问题给我们**](https://ivanontech.typeform.com/to/R9K5lnGe)

**你问，我们答！**

每周我们都会收到像您一样的 Moralis 开发人员的问题。通常，通过访问官方的 Moralis 论坛可以找到答案。就拿我们最近收到的一个问题来说:

**“我在 NodeJS 中构建一个对 NFT 集合竞价的 REST API，我想在 Moralis React 中构建前端，它调用 REST API 进行服务，但是使用登录用户认证的 wallet。您如何将这些钱包凭证从 Moralis 传递给 API，以便 API 可以从最终用户的钱包中出价？”**

![](img/0a5a451bf29a74c0adb2d6557a301a14.png)

对于这个问题，我们的回答是:

如果您需要从应用程序调用外部 API，那么尝试从云函数内部发出 HTTP 请求。文档中有更详细的说明，但是您需要定义一个简单的云函数，它向您的 API 返回一个 HTTP 请求；调用云函数时，可以传递钱包地址(request.params.address)等参数。

但是等等，还有更多…

有关云服务器请求的详细信息，请访问:

[https://docs . moralis . io/moralis-server/cloud-code/http request。](https://docs.moralis.io/moralis-server/cloud-code/httprequest.)

有关相关主题的讨论可在此处找到:

[https://forum . moralis . io/t/how-to-call-external-API-in-moralis-cloud-function-and-job/7673。](https://forum.moralis.io/t/how-to-call-external-api-in-moralis-cloud-function-and-job/7673.)

如果所有这些都失败了，在 Moralis 道不和谐聊天室寻求进一步的帮助。

**提出要求，你将获得……**

Moralis 核心团队维护着一份活的时间表文件，该文件在[https://roadmap.moralis.io/](https://roadmap.moralis.io/)找到。与你过去可能遇到的其他时间线不同，Moralis 时间线是一个不断增长的适应新建议、计划提案和正在进行的实施的花名册。

我们想知道你是怎么想的，什么对你来说是重要的。查看路线图并立即提交您的功能请求！

像魔术一样认证！

希望将“可信机构”钱包创建和认证集成到您的基于 Moralis 的 Web3 dApp 中？现在你可以了！查看我们的新教程，了解全部详情:

https://www.youtube.com/watch?v=gLJ4YejmG2E

大多数用户会发现 Magic(来自 Magic Labs)是一个非常直观的新用户认证解决方案；然而，这并不是 Moralis 开发者的唯一选择。很快，Web3Auth 也将得到 Moralis 的 Web3 框架的支持。web 3 auth([https://web3auth.io/](https://web3auth.io/))通过实现“秘密共享方案”提高了选择的多样性，该方案取代了 Magic 实现的密钥保管方法。

你们每个人都是非凡事物的一部分，这本杂志就是要让 Moralis 的力量为你所用！

![](img/2c615e2255f34e796b97b16916d05350.png)

我们都是 Moralis 家，在这里互相支持。如果你不是已经活跃在[道貌岸然道不和](https://discord.com/invite/P9N9HF97hH)的话，今天就是让你登场的日子。

在 Moralis 道的冲突中，你会发现一堆 Moralis 专家和法师同伴。发布您的项目并从社区获得反馈，参与编码挑战，并了解最新的 Moralis 特性和更新。

* * *

**游戏中的动态 NFT:第二部**

我们无畏的 Moralis 专家 Ash 本周又来了，提供了更多的技巧和工具来增强我们的 Web3 游戏！

本周的视频继续第一部分的内容:

https://www.youtube.com/watch?v=NC7T1Li9wjE

元宇宙/NFT 游戏开发的最大限制是捕捉链外发生的事情并将其带到链上的能力。

这被称为“神谕问题”,影响了所有希望“加入”当前元宇宙游戏机会的游戏。

在之前的视频中，我们讨论了更新 NFT 游戏资产的概念和用户体验的最佳实践，但在本视频中，我们将为您提供一些逐行解决方案。

让我们进入我们用 Moralis 构建的 NFT 游戏沙盒的代码，它将演示这个问题。

你如何利用所提供的工具和专业知识取决于你自己，我们希望这本杂志能激发一些想法。

* * *

感谢阅读！我们希望本周的 Moralis 杂志对你有用。

继续建造！

下次见💚

Moralis 研究小组