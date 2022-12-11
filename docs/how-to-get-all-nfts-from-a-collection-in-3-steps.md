# 如何在 3 个步骤中从集合中获取所有的 NFT

> 原文：<https://moralis.io/how-to-get-all-nfts-from-a-collection-in-3-steps/>

多亏了 Moralis 的终极 NFT API，任何开发者都可以从一个集合中获得所有的 NFT。安装 Moralis SDK 并使用“***【getContractNFTs】*****”*****NFT API 端点；就这么简单！本质上，通过下面的代码片段，您可以涵盖从集合中获取不可替换令牌的核心内容:***

```js
 *const response = await Moralis.EvmApi.nft.getContractNFTs({
    address,
    chain,
  });*
```

*如果您已经熟悉了 [Moralis](https://moralis.io/) 以及它如何帮助您弥合 Web2 和 Web3 之间的开发差距，那么您可能有几个利用上述代码行的想法。但是，如果您是 Web3 开发的新手，请务必完成今天的教程。通过这样做，您将学会如何轻松地从集合中获取所有的 NFT。只需创建你的[免费 Moralis 账户](https://admin.moralis.io/register)并跟随我们。*

*![Unlock the Power of Blockchain - Get All NFTs from Contract by Signing Up with Moralis.](img/776315699d4da3e5c69ca048fbcedf78.png)[**Sign Up with Moralis**](https://admin.moralis.io/register)

### 概观

熊市是构建 dapps(去中心化应用)的最佳时机。考虑到 NFTs 仍然是最受欢迎的区块链用例之一，现在是学习如何使用终极 [NFT API](https://moralis.io/nft-api/) 的时候了。

![A hologram displaying a text that says how to get all NFTs from collection.](img/25a0c841b2291b4230d6eac6ea40b0ea.png)

正如前面指出的那样，“*getContractNFTs*”API 端点将是今天文章的焦点。接下来的教程将围绕正确合并上述代码片段展开。最后，我们将教您如何使用 JavaScript (JS)或 TypeScript (TS)轻松地从集合中获取所有 NFT。幸运的是，这是一个三步走的过程，不会花你超过几分钟。特别是因为您可以简单地复制和粘贴我们的 cod 行，一旦您从集合中获得 NFT，您就可以使用您的终端来浏览结果。

此外，我们决定帮助您更上一层楼。因此，你也可以跟随我们的领导，创建一个简单的 NFT 探险家 dapp。这样，您将看到如何巧妙地利用由" *getContractNFTs* "端点提供的结果。

然而，在我们邀请您卷起袖子按照我们的指示行动之前，我们需要确保您了解基础知识。因此，我们将首先解释什么是 NFT 和 NFT 集合。我们还将进一步了解 NFT 系列的终极开发工具——Moralis NFT API。

![NFT Collections](img/b32bc0adee1c41d8b2e269b2eab39637.png)

## NFT 和集合–它们是什么？

NFT(不可替换令牌)是一种特殊的加密资产。根据“不可替换”的含义，这些类型的令牌是不可互换的。这意味着每个 NFT 都有其唯一的令牌 ID(链上签名)。因此，NFT 被设计来表示唯一的数字或物理项目。因此，数字艺术和数字收藏品往往是不可替代代币最常见的实用示例是有道理的。然而，NFT 已经彻底改变了许多其他行业，这些行业需要任何类型的所有权证明或证书发放。尽管如此，这些加密资产也将改变游戏产业。毕竟，我们已经看到各种各样的 Web3 游戏项目，让玩家真正拥有自己的游戏资产。

此外，NFT 通常被分配给集合。这不是必需的，因为 NFT 可以完全独立。然而，通常情况下，不可替换令牌的创建者倾向于向单个集合分配更大量的令牌。当然，不同的项目集合的大小也有很大的不同。在数字艺术中，收藏倾向于包括较少的非艺术作品。另一方面，当涉及到数字收藏品时，单个收藏品通常可以包括几千个 NFT。例如，CryptoPunks 集合包括近 10，000 个 NFT。

![CryptoPunks Collection](img/70c1982baf4a6ea3a3b33cad9f296b03.png)

此外，值得指出的是，开发人员使用智能合约创建(制造)NFT。这些链上的软件包括他们关注的 NFT 的所有细节。此外，合同包括预定义的操作，这些操作将在满足特定的预定义条件时执行。因此，它们也管理与其非金融交易相关的交易。另外，请注意，在一个集合中的所有 NFT 背后都有相同的智能协定。因此，我们通过关注正确的智能契约从集合中获得 NFTs。

## NFT 系列的终极开发工具

既然您已经知道了什么是 NFT 和 NFT 集合，现在是时候让我们更仔细地研究一下让您从集合中获取所有 NFT 的工具了。至此，您已经知道，如果您想知道集合中有多少个 NFT，您可以使用 Moralis " *getContractNFTs* "端点。当然，这个优秀的工具还可以为您提供更多关于特定系列的细节。

您甚至可以通过利用 Moralis 武库中的其他 NFT API 端点来扩展您的工具集。此外，在构建 dapps 时，您可能希望使用其他 Moralis 的 Web3 APIs，从它的 [Web3 Auth API](https://moralis.io/authentication/) 开始。此外，当使用 NFT 集合时，“ [getWalletNFTCollections](https://docs.moralis.io/reference/getwalletnftcollections) ”和“ [getNFTContractMetadata](https://docs.moralis.io/reference/getnftcontractmetadata) ”端点可能特别有用。

然而，在本文中，我们想向您展示如何使用“*getContractNFTs*”*从集合中获取所有的 NFT。*因此，我们需要更仔细地研究这个端点，它本质上使您能够[从一个合同中获得所有的 NFTs】。另外，“ *getContractNFTs* ”为属于特定智能契约的所有 NFT 提供元数据。也就是说，您应该记住，端点被限制为每页显示 100 个结果。因此，对于超过 100 个 NFT 的集合，您需要使用 cursor 参数。](https://moralis.io/how-to-get-all-nfts-from-a-contract/)

### 根据合同文档获取 NFTs

以下是“[](https://docs.moralis.io/reference/getcontractnfts)*”文档页面截图:*

*![The getContractNFT endpoint documentation page.](img/19c19ba490789a8ce2534926671f4064.png)

后者提供了关于端点的所有细节。此页面还允许您测试此端点，并复制与您的编程语言相匹配的代码。此外，以下是该端点接受的参数:

*   *"* ***地址****"***–您使用此参数来提供 NFT 智能合同地址。此外，这个参数是必不可少的(所有其他参数都是可选的)。**
*   **"* ***链****"***-此参数让您决定关注哪个可编程链(Moralis 支持所有领先的 Web3 网络)。***
*   ***"* ***格式****"***–您使用此参数来确定想要使用哪种类型的令牌 ID 格式–十进制或十六进制。****
*   ******限制******–此参数允许您设置结果所需的页面大小。******
*   ***"****total range****"***–您可以使用此参数来确定将结果分割成多少个子范围。****
*   ***"* ***范围****"***-该参数用于设置需要查询的子范围。****
*   ***"* ***光标****"***–当您有超过 100 个 NFT 或希望每页显示更少的 NFT 时，您可以使用此参数进入下一页。****
*   ***"****normalize metadata****"–此参数让您决定是否应该返回规范化的元数据(true)或不返回(false)。如果选择“true”，端点将在名为“normalized_metadata”的新对象中返回标准化结构的元数据。***

**现在您已经了解了" *getContractNFTs* "端点的理论和功能，您已经准备好动手了。因此，请务必遵循我们的教程，其中涵盖了从集合中获取 NFT 所需完成的步骤。**

## **如何从集合中获取所有 NFT**

**知道如何从集合中获取所有的 NFT 非常有用。如前所述，NFT 在许多 dapps 中扮演着重要的角色，您可以使用这些类型的令牌来表示区块链上某个独特物品的所有权。相应地，你可以建立 NFT 投资组合跟踪器、NFT 门户网站、Dao、社交图和许多其他类型的 NFT dapp。**

**在继续之前，请确保您已经完成了这三个先决条件:**

***   安装 Node v.14 或更高版本。*   准备好自己喜欢的代码编辑器或者 IDE。我们倾向于使用 Visual Studio 代码(VSC)。*   安装你喜欢的包管理器(" *npm* " *，* " *纱* " *，或者* " *pnpm* ")。**

**![Wizard pointing at text that says learn how to get all nfts from a collection.](img/33cfa3bc48198f9833bb71d7b455de74.png)

### 步骤 1:建立 Moralis 观

要完成本教程并从集合中获取所有 NFT，您必须访问您的 Moralis 管理区。因此，请确保您创建了您的免费 Moralis 帐户。您可以使用简介中的链接或访问 Moralis 主页:

![](img/13308ae00dcbe83b6ebb43a30fc41489.png)

无论哪种情况，您都将进入注册页面。只需输入您的全名和电子邮件地址，创建您的密码，并接受条款和条件。有了这些详细信息，您就可以点击“注册”按钮了:

![](img/9ecdeb1428cae04ad6423aad88c9d26f.png)

最后，通过点击电子邮件收件箱中的确认链接来确认您的帐户。

无论您是否想要使用“ *getContractNFTs* ”从集合或任何其他 Moralis Web3 API 端点获取 NFTs，您都需要您的 Web3 API 密钥。幸运的是，现在您已经准备好了您的 Moralis 帐户并可以访问您的管理区，您只需简单地点击两次就可以获得它:

![](img/e2b55e49aa3c068ee0f5d84c2dcafe43.png)

在下一节中，您将看到在哪里粘贴您的 API 密匙。但是，在继续之前，请在您的项目中安装 Moralis SDK。根据您使用的软件包管理器，您需要运行以下命令之一:

```js
npm install moralis
```

```js
yarn add moralis
```

```js
pnpm add moralis
```

### 步骤 2:使用示例脚本从集合中获取所有 NFT

完成初始设置后，您就可以专注于一个示例脚本了，它使您能够毫不费力地从一个集合中获取所有的 NFT。下面是一个“index.js”脚本:

```js
const Moralis = require("moralis").default;
const { EvmChain } = require("@moralisweb3/evm-utils");

const runApp = async () => {
  await Moralis.start({
    apiKey: "YOUR_API_KEY",
    // ...and any other configuration
  });

  const address = "0xb47e3cd837dDF8e4c57F05d70Ab865de6e193BBB";

    const chain = EvmChain.ETHEREUM;

  const response = await Moralis.EvmApi.nft.getContractNFTs({
    address,
    chain,
  });

  console.log(response);
}

runApp();
```

*注意* *:如果你喜欢使用 TypeScript，请确保使用上面的“文档页面”链接。在那里，您可以在“index.js”和“index.ts”之间进行选择。*

而且，如果你看上面的几行代码，可以看到“ *EvmChain。以太坊*”。后者定义了脚本关注的链。因此，如果你想从其他领先的 [EVM 兼容链](https://docs.moralis.io/docs/cross-chain-requests#supported-evm-chains)上的集合中获得所有的 NFT，你需要相应地替换*以太坊*。

尽管如此，无论您决定使用 JS 还是 TS，您都需要用上面获得的 Web3 API 密钥替换" *YOUR_API_KEY* "占位符。

### 步骤 3:执行程序从集合中获取所有的 NFT

既然已经准备好了“索引”文件，就可以执行程序并查看给定地址的详细信息，包括集合中有多少个 NFT。因此，在终端中输入以下命令之一:

**对于 JavaScript:**

```js
node index.js
```

**对于打字稿:**

```js
node index.ts
```

运行适当的命令后，检查终端的结果。如果您没有更改上面代码中的地址，您应该会看到以下结果:

```js
{
  "total": 9991,
  "page": 0,
  "page_size": 100,
  "cursor": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ3aGVyZSI6eyJ0b2tlbl9hZGRyZXNzIjoiMHhiNDdlM2NkODM3ZGRmOGU0YzU3ZjA1ZDcwYWI4NjVkZTZlMTkzYmJiIn0sInRva2VuX2FkZHJlc3MiOiIweGI0N2UzY2Q4MzdkZGY4ZTRjNTdmMDVkNzBhYjg2NWRlNmUxOTNiYmIiLCJsaW1pdCI6MTAwLCJvZmZzZXQiOjAsIm9yZGVyIjpbXSwicGFnZSI6MSwia2V5IjoiZmQ5MmE0ODg3MmE4NjIwZTFlNmU0NTk3ODZkMTExYWYiLCJ0b3RhbCI6OTk5MSwiaWF0IjoxNjY3ODA4NzcxfQ.9qXwHyyUKJkzrub-ze-q2gm8dC0dy-jvgF0CJrm5piY",
  "result": [
    {
      "token_address": "0xb47e3cd837ddf8e4c57f05d70ab865de6e193bbb",
      "token_id": "9082",
      "amount": "1",
      "token_hash": "fffdaced3ddfb220d9124289a518bb97",
      "block_number_minted": "12021693",
      "updated_at": null,
      "contract_type": null,
      "name": "CRYPTOPUNKS",
      "symbol": "Ͼ",
      "token_uri": "https://www.larvalabs.com/cryptopunks/details/9082",
      "metadata": "{\"image\":\"https://www.larvalabs.com/cryptopunks/cryptopunk9082.png\",\"name\":\"CryptoPunk 9082\",\"attributes\":[\"Bandana\",\"Big Shades\",\"Shadow Beard\"],\"description\":\"Male\"}",
      "last_token_uri_sync": null,
      "last_metadata_sync": "2022-10-05T17:55:52.262Z",
      "minter_address": "0xc352b534e8b987e036a93539fd6897f53488e56a"
    },
    {
      "token_address": "0xb47e3cd837ddf8e4c57f05d70ab865de6e193bbb",
      "token_id": "4799",
      "amount": "1",
      "token_hash": "fff8ff007820e85a75c545389d5a88d4",
      "block_number_minted": "11637283",
      "updated_at": null,
      "contract_type": null,
      "name": "CRYPTOPUNKS",
      "symbol": "Ͼ",
      "token_uri": "https://www.larvalabs.com/cryptopunks/details/4799",
      "metadata": "{\"image\":\"https://www.larvalabs.com/cryptopunks/cryptopunk4799.png\",\"name\":\"CryptoPunk 4799\",\"attributes\":[\"Blue Eye Shadow\",\"Black Lipstick\",\"Straight Hair Blonde\",\"Earring\"],\"description\":\"Female\"}",
      "last_token_uri_sync": null,
      "last_metadata_sync": "2022-07-17T17:25:24.644Z",
      "minter_address": "0xc352b534e8b987e036a93539fd6897f53488e56a"
    },
    {
      "token_address": "0xb47e3cd837ddf8e4c57f05d70ab865de6e193bbb",
      "token_id": "47",
      "amount": "1",
      "token_hash": "fff3657368693f145d0ad29453f6cd4d",
      "block_number_minted": "3918216",
      "updated_at": null,
      "contract_type": null,
      "name": "CRYPTOPUNKS",
      "symbol": "Ͼ",
      "token_uri": "https://www.larvalabs.com/cryptopunks/details/47",
      "metadata": "{\"image\":\"https://www.larvalabs.com/cryptopunks/cryptopunk047.png\",\"name\":\"CryptoPunk 047\",\"attributes\":[\"Knitted Cap\"],\"description\":\"Male\"}",
      "last_token_uri_sync": null,
      "last_metadata_sync": "2022-07-24T12:12:11.930Z",
      "minter_address": "0xc352b534e8b987e036a93539fd6897f53488e56a"
    }
  ],
  "status": "SYNCED"
}
```

那么，聚焦以太坊链上的“*0x b 47 E3 CD 837 ddf 8 e4c 57 f 05d 70 ab 865 de 6 e 193 BBB*”地址时，一个集合中有多少个 NFT 呢？如果你想的是 9991，那你就对了。现在，尝试使用“index”脚本从其他 EMV 兼容链上的集合中获取 NFT。

![Finalized NFT explorer dapp letting a user get all NFTs from a collection in 1 click.](img/422c14809aebb7858ed2cee365a1ba69.png)

### 额外收获:使用浏览器 Dapp 从收藏中获取所有的 NFT

上面的教程教你如何从一个集合中获取所有的 NFT。这样，您现在就可以利用" *getContractNFTs* "端点构建一个合适的 dapp 了。如果这听起来很有趣，请务必使用下面的视频，并遵循我们内部专家的指导。您将构建一个简洁的 NFT 资源管理器 dapp，而不是关注集合中有多少 NFT。后者将使您能够输入一个合同地址，并选择您想要关注的链。有了这两个参数，您就可以点击“Get NFT”按钮，这将从一个集合中获取 NFT，并整齐地呈现前二十个 NFT:

![](img/04c8224d15f60c3a9bca4a37d135f108.png)

最后，这是一个视频教程，将向您展示如何创建一个 NodeJS 后端应用程序和 ReactJS 前端应用程序，并将它们结合在一起，创建一个很酷的 NFT 浏览器 d app 与 Moralis:

[https://www.youtube.com/embed/3oUb9QGTXEU?feature=oembed](https://www.youtube.com/embed/3oUb9QGTXEU?feature=oembed)

## 如何通过 3 个步骤从集合中获取所有非功能性食物–总结

在今天的文章中，您有机会学习如何使用终极 NFT API 从集合中获取所有的 NFT。如果您不熟悉 Moralis，您还会了解到这个企业级 Web3 API 提供程序使您能够以简单的方式创建杀手级 dapps。我们还解释了什么是 NFT 和 NTF 集合。然而，本文的核心是我们的三步教程，重点是使用" *getContracNFTs* "端点。此外，通过完成本教程，您学习了如何轻松地找出一个集合中有多少个 NFT，以及其他一些细节。最后但同样重要的是，您还有机会跟随一个简短的视频教程并构建一个示例 NFT 探索者 dapp。因此，您现在知道了如何使用我们的示例 dapp 从集合中获取所有的 NFT。

如果您喜欢今天的教程，并想继续探索 NFT 开发，请务必查看我们的其他 NFT API 操作指南，它们在 Moralis 的文档中等待着您。另一方面，您可能有兴趣探索其他区块链发展主题。在这种情况下，你应该访问 Moralis YouTube 频道和我们的 T2 区块链博客。那里的一些最新文章包括[加密钱包集成](https://moralis.io/crypto-wallet-integration-using-the-best-crypto-wallet-api/)、 [Web3 提供商](https://moralis.io/web3-provider-why-blockchain-developers-should-use-one/)、[面向企业的 web 3](https://moralis.io/web3-for-business-how-and-why-you-can-integrate-web3-into-your-enterprise/)，以及许多其他有趣的主题。

最后但同样重要的是，你可能会有兴趣去全职加密越早越好。如果是这样，你应该报名参加 Moralis 学院。在那里，你可以选择许多不同的课程，并获得区块链认证。然而，我们建议从[区块链和比特币基本面](https://academy.moralis.io/courses/blockchain-bitcoin-101)开始。****