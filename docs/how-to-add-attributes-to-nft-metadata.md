# 如何向 NFT 元数据添加属性

> 原文：<https://moralis.io/how-to-add-attributes-to-nft-metadata/>

虽然 NFT([**不可替代代币**](https://moralis.io/non-fungible-tokens-explained-what-are-nfts/) **)仍然主要用于数字艺术，但一个对 NFT 革命来说已经相当成熟的行业是 Web3 游戏。如果你玩或曾经玩过任何类型的视频游戏，你会很清楚游戏中的物品可以附带特定的能力。同样，NFT 可以添加属性，这可以为区块链游戏体验带来更多深度。此外，属性扩展了 NFT 的用例，使它们非常适合所有类型的 Web3 游戏。对于游戏开发人员来说，知道如何向 NFT 元数据添加属性是推进下一代区块链游戏的关键。**

在本文中，我们将探索如何在一个简单的 Unity 应用程序的帮助下轻松实现这一点。此外，通过克隆我们的代码，您可以使用我们的 Unity IPFS uploader v2 功能来获取元数据 URL。但是，我们将从介绍什么是 NFT 元数据属性开始这篇文章！

然后，我们将向您展示如何使用我们的 Unity IPFS 上传器 v2 向 NFT 元数据添加属性。在看了我们的应用程序的演示之后，我们将指导您完成安装过程，这将使您能够自己使用这个应用程序。我们还将看看上传应用程序代码中最关键的部分。在此过程中，您将学习如何完成初始的 Moralis 设置，这将是您进行 Web3 开发的门户。知道如何使用 [Moralis](https://moralis.io/) 并获得它的全部能力将使你能够创建各种 dapp([分散应用](https://moralis.io/decentralized-applications-explained-what-are-dapps/))。这意味着你将能够利用你的 Unity 技能创造一个优秀的 Web3 游戏。因此，要学习如何轻松地向 NFT 元数据添加属性，请务必[创建您的免费 Moralis 账户](https://admin.moralis.io/register)！

![](img/b0d7ae98cd72b9b0a4acc910c7f15b4e.png)

## 什么是 NFT 元数据属性？

你们中的许多人可能知道“NFT 属性”。这些是侧面图(PFP)NFT 具有的各种视觉方面。从不同的背景到不同的衣服、五官和配饰。然而，“NFT 元数据属性”是不同的东西。这些是通常不可见的属性。相反，它们被编码到 NFTs 元数据中。此外，由于有各种各样的 NFT 标准，需要注意的是，我们在这里重点关注的是 [ERC-721 令牌标准](https://moralis.io/erc-721-token-standard-how-to-transfer-erc721-tokens/)。

鉴于 OpenSea 是查看 NFT 及其详细信息的最流行的平台之一，查看他们关于该标准的文档可能会有所帮助。当然，你也可以在 GitHub 上看看官方的 ERC-721 元数据标准。

![](img/223fac1b932a9a8e86d5e2621308468a.png)

#### NFT 元数据属性数组示例

以下是 ERC-721 元数据的一个示例:

![](img/e462edbf68818ddc6a1d33fb074f58de.png)

如您所见，元数据属性以数组的形式出现。除了添加功能之外，这些属性使您能够为 NFTs 添加额外的唯一性。此外，以下是元数据属性数组的示例:

```js
{
"attributes": [
    {
      "trait_type": "Base", 
      "value": "Starfish"
    }, 
    {
      "trait_type": "Eyes", 
      "value": "Big"
    }, 
    {
      "trait_type": "Mouth", 
      "value": "Surprised"
    }, 
    {
      "trait_type": "Level", 
      "value": 5
    }, 
    {
      "trait_type": "Stamina", 
      "value": 1.4
    }, 
    {
      "trait_type": "Personality", 
      "value": "Sad"
    }, 
    {
      "display_type": "boost_number", 
      "trait_type": "Aqua Power", 
      "value": 40
    }, 
    {
      "display_type": "boost_percentage", 
      "trait_type": "Stamina Increase", 
      "value": 10
    }, 
    {
      "display_type": "number", 
      "trait_type": "Generation", 
      "value": 2
    }
  ]
}
```

查看上面的示例代码，您可以看到 ERC-721 属性是成对的特征类型和值。此外，属性还可以有一个可选的显示类型，我们可以指定或省略它。此外，这是 OpenSea 显示上述属性的方式:

![](img/b78e482658535222c5c4fba4309e82d6.png)

这个简单的元数据属性示例清楚地表明，当您向 NFT 元数据添加属性时，您可以向 NFT 添加很多值并扩展它们的功能。在 Web3 游戏的情况下，这可以产生巨大的差异。

## 如何使用我们的 Unity IPFS 上传程序向 NFT 元数据添加属性

让我们先来看看我们的 Unity IPFS 上传应用程序的演示。尽管我们的应用程序不执行任何链上事务，但它从 Web3 身份验证开始:

![](img/10e18585dd8926a3cef1fa6ddd62ff35.png)

所以，我们必须首先点击“连接”按钮登录。这样，就会出现一个二维码。接下来，我们需要使用我们最喜欢的移动加密钱包扫描代码:

![](img/7bc948767cb53cb70fad802db609bf26.png)

“用您的钱包签名”消息让我们知道我们已经成功扫描了代码:

![](img/45f2d70b91acb209c87de8e7ea338743.png)

成功登录后，我们进入上传应用的仪表板:

![](img/e9c00613e73e179757d7ecc06b826d80.png)

查看上面的截图，您可以看到该应用程序包括四个按钮。在右上角，如果我们决定退出，可以单击“断开”。然后，“选择”按钮让我们选择一个图像文件，我们想用作为 NFT 的视觉部分。该应用程序会将选定的图像上传到 IPFS，并在元数据中包含相应的图像 URL。此外，除了图像，NFT 的名字和描述也很重要。这是我们在应用程序面板右侧输入的内容。*以上是我们的* [*Unity IPFS 上传者 v1*](https://youtu.be/rVlh2BzjmU4) *已经包含的功能。*然而，我们的 IPFS 上传器的更新版本也允许我们向 NFT 元数据添加属性。这就是“查看属性”和“新属性”按钮发挥作用的地方。

## 无需编码即可向 NFT 元数据添加属性–演示

当我们点击“查看属性”按钮时，我们将看到添加的属性；但是，由于我们尚未添加任何内容，该列表目前为空:

![](img/bf4465d79f2f609849257d054267ae2b.png)

因此，让我们使用“新建属性”按钮向 NFT 元数据示例添加属性:

![](img/a4e2fe4f58c09e8675099762dfa91f5c.png)

正如你在上面的截图中看到的，“提交”按钮最初是禁用的。这是因为我们必须首先向 NFT 元数据添加基本属性。而且，如果你记住了，“特质类型”和“价值”是必不可少的，而“展示类型”是可选的。因此，填写底部的两个输入字段已经激活了“提交”按钮:

![](img/0fff73f27143e77f73ca91089f37bbf4.png)

但是，为了便于演示，我们还包括一个显示类型:

![](img/46ed4fc88dec3c6d3c8c0d0ce08996f1.png)

填充输入字段后，我们需要单击 submit 按钮。然后，我们已经可以通过“查看属性”按钮查看该特定属性:

![](img/c854e11bcdea60e8eb8d20407d421493.png)

此外，正如你在上面的截图中看到的，我们还可以在上传属性到 IPFS 之前删除它们。另一方面，我们可以再次使用“新属性”按钮来添加更多的属性:

![](img/8a6cbfc82d2c28a79884f8ecba62aa2f.png)

通过这样做，我们的属性列表扩展了:

![](img/654c0fa78d9ba5c9364f8332562a9702.png)

当然，如果我们愿意，我们可以添加更多的属性。然而，现在让我们上传我们的元数据到 IPFS。因此，我们需要返回主面板。

### 将元数据上传到 IPFS–演示

设置好属性后，我们需要选择一个图像文件，并给它一个名称和描述，然后才能将元数据上传到 IPFS。首先，我们从计算机中选择一个 PNG 文件:

![](img/2234cf6e86a8234873c7a7dc74c5c291.png)

然后，我们添加我们的 NFT 的名字和描述，这将激活“上传”按钮:

![](img/dbd9ba8c9166140ce4d292bdeae3a4e7.png)

点击“上传”按钮后，你会得到“图像文件成功保存到 IPFS！”显示消息，随后显示“元数据已成功保存到 IPFS！”：

![](img/966f25c5232e34f4e372de5d5c0be44b.png)

如果我们打开 Unity 控制台，我们可以看到包含示例元数据的 JSON 文件的 URL:

![](img/49d6a0acef1f0dbfb45da966c68d5a2b.png)

我们可以将上述 URL 复制到任何浏览器中，以查看我们的元数据:

![](img/57930cfb380cdbddf77731b749c3d06d.png)

我们还可以使用格式改变工具(例如“JSON 格式化程序”)以更简洁的格式查看我们的示例数据:

![](img/2dc3e290bb0100f33d9c557f8bc3fae2.png)

## 如何使用我们的统一 IPFS 上传

既然您已经看到了我们的 IPFS 上传器应用程序的运行，您可能会渴望使用它来添加 NFT 元数据的属性。幸运的是，只需要几分钟就可以完成初始设置。本质上，你只需要从我们的 [GitHub 页面](https://github.com/MoralisWeb3/unity-web3-ipfs-uploader)下载这个项目，在 Unity 中打开它，然后输入你的 Moralis dapp 的证书。虽然这是一个相对简单的过程，但遵循以下分步指南可能会非常有用:

1.  使用上面的“GitHub 页面”链接下载 ZIP 文件或克隆代码:

![](img/6c9ce5f70dfadfab0dc08d7986abf44a.png)

2.  打开您的 Unity hub，然后打开项目:

![](img/7124a924a7bca72f2a2096ee564d4170.png)

3.  使用简介中的“创建您的免费 Moralis 帐户”链接或访问 Moralis 的官方网站:

![](img/19a5d69eb86a68a3152c343e69b5cd23.png)

*注* *:正如你在上面看到的，这里也是注册具有可观价格池的挑战性黑客马拉松的地方。*

4.  创建您的免费 Moralis 帐户后，您将访问您的管理面板。这是您创建新 dapp 的地方:

![](img/603c429bbf6dfc7cff955eb2eea51427.png)

5.  在 dapp 设置的第一步，选择“Mainnet”:

![](img/26b5cb6387544404003bc90610178608.png)

6.  接下来，您可以选择 Moralis 支持的领先网络之一。*为了这个例子，我们用 Cronos:*

![](img/9d240a0526c91d7b3cfabb7124496d3c.png)

7.  接下来，您需要选择您所在的地区。使用下拉菜单，选择离您的实际位置最近的城市:

![](img/8dff84dea68fdd3dac1817bb1051c276.png)

8.  作为 Moralis dapp 设置的最后一步，您需要命名您的 dapp 并点击“创建您的 dapp”按钮:

![](img/530cd4df44ee4c2a87b5808264ec9e71.png)

9.  一旦您的 dapp 启动并运行，您可以点击“设置”按钮:

![](img/2a2c5020486f4b7dc5468166c430b813.png)

10.  若要访问您的 dapp 凭据，您需要向下滚动一点。然后，使用“复制”图标复制您的 dapp URL 和 ID:

![](img/960544f4be6c2eae9b8bba1c99f7caa4.png)

11.  返回 Unity 并打开 Moralis Web3 设置模块:

![](img/9e6997b6e02e2024e093ed989e7bb793.png)

12.  将您的 dapp 凭据粘贴到指定的输入字段中:

![](img/340847ef155a0ecb694bc526e9821e02.png)

现在，您可以点击“播放”向 NFT 元数据添加属性:

![](img/f5e68f79fb799dadb455a9f35c8b4871.png)

### 使我们的应用程序能够向 NFT 元数据添加属性的代码

至此，您已经知道如何使用我们的 Unity IPFS 上传程序 v2 向 NFT 元数据添加属性。因此，您可以开始使用它来准备元数据。但是，我们鼓励您也花几分钟时间来确保您正确理解了使这成为可能的代码。因此，使用下面的视频，从 9:46 开始。

在视频中，您将首先看一看“AppManager ”,它包含我们的应用程序的状态。这些是“Main”、“NewAttribute”和“ViewAttributes”，您可以在上面的演示中看到:

![](img/e5e5545ebe53a16d13195bfb3ecc8375.png)

在“ *NewAttribute* ”脚本中，您将首先看到从输入字段中捕获文本的代码行。11:21，您将仔细查看“ *AttributeObject* ”类，该类是在“ *NewAttribute* 状态下单击“提交”按钮后触发的。此外，还有几行代码确保“提交”按钮只有在提供了所有必要的数据时才是活动的。另外，“ *SubmitButtonPressed()* ”函数触发“ *OnSubmittedAttribute* ”事件。应用程序管理器监听该事件，并向私有列表添加新的属性对象。

但是，基本功能是“*UploadToIpfs*”(12:35)，您可以通过单击“上传”按钮调用它。这就是“ *BuildMetadata* ”构造对象属性数组的地方。尽管如此，从 14:01 开始，您还将看到“ *ViewAttributes* ”脚本。后者用属性的细节创建预置，并以用户友好的方式显示它们。

*最后，这是一个视频教程，将带你浏览我们的 Unity IPFS 上传应用程序背后的代码:*

[https://www.youtube.com/embed/bvoJJTAIk3E?feature=oembed](https://www.youtube.com/embed/bvoJJTAIk3E?feature=oembed)

## 如何向 NFT 元数据添加属性-摘要

在以上各节中，您了解了如何向 NFT 元数据添加属性并将该元数据上传到 IPFS。使用我们的 IPFS 上传应用程序，只需要几分钟就可以完成 NFT 创作的重要部分。在此过程中，您还学习了如何完成初始的 Moralis 设置，包括创建新的 Moralis dapp 并获取其证书。您必须将后者粘贴到 Unity 中才能访问 Moralis 的 Unity Web3 SDK。后者包括 IPFS 一体化。

创建元数据是创建 NFT 的重要部分，但这只是旅程的一部分。您仍然需要执行一个实际的链上事务来将您的元数据转换成 NFTs。同样，有几种选择来铸造 NFT。然而，如果您想走阻力最小的道路，使用我们的 Unity NFT 敏特 dapp 是正确的选择。你可以在[Moralis 博客](https://moralis.io/blog/)上了解所有你需要知道的关于如何[打造一个团结的 NFT](https://moralis.io/how-to-mint-a-unity-nft/) 。这也是一个很好的地方来了解更多关于 dapp 开发的全部内容。当然，你也应该访问[Moralis YouTube 频道](https://www.youtube.com/c/MoralisWeb3)，在那里你会找到大量优秀的教程。最终，这是两个可以免费帮助你成为 Web3 开发者的途径。

我们希望你能好好利用 IPFS 上传器和 NFT minter 工具，创造出一些杀手级的 Web3 游戏。然而，如果你还没有足够的信心来处理你自己的项目，请确保通过完成我们的示例项目来练习。尽管如此，你可能渴望尽快成为全职加密员。如果是这样的话，获得区块链认证是一条必经之路，这也是 Moralis 学院为你提供支持的地方。