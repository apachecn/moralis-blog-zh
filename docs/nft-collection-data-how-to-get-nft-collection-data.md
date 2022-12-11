# NFT 收集数据-如何获得 NFT 收集数据

> 原文：<https://moralis.io/nft-collection-data-how-to-get-nft-collection-data/>

大多数不可替换的代币属于 NFT 收藏。因此，如果你打算建立与 NFT 相关的 dapps，了解如何获得 NFT 收集的数据会非常有益。幸运的是，您不必构建一个能够让您从头开始做这件事的基础设施。相反，这里有两个代码片段，可以帮助您不费吹灰之力地获得您需要的所有 NFT 集合数据:

```js
const response = await Moralis.EvmApi.nft.getNFTContractMetadata({address,});
```

```js
const response = await Moralis.EvmApi.nft.getContractNFTs({address,});
```

“ *getNFTContractMetadata* ”和“ *getContractNFTs* ”端点是 Moralis 的终极 [NFT API](https://moralis.io/nft-api/) 的一部分。如果您以前使用过 [Moralis](https://moralis.io/) 并且精通 JavaScript，您很可能知道如何利用上面的代码行来获取 NFT 收集的数据。另一方面，这可能是你第一次和 Moralis 家一起竞技。在这种情况下，您应该完成这个循序渐进的教程。你只需要创建你的免费 Moralis 帐户，并遵循我们的领导！

![Unlock the Power of Blockchain with Moralis](img/776315699d4da3e5c69ca048fbcedf78.png)[**Sign Up with Moralis and Unlock the Power of Blockchain**](https://admin.moralis.io/register)

### 概观

NFTs 仍然是最受欢迎的区块链用例之一。它们提供了无数的机会来创建分散的应用程序(dapps ),这些应用程序在某种程度上包含了 NFT。这可能是 NFT 探险者，NFT 追踪者，NFT 门控网站，Web3 游戏等。此外，每当您想要构建与 NFT 相关的 dapps 时，获取 NFT 集合数据的能力会使事情变得简单很多，使用上面的两个代码片段是最好的方法。

![User looking at a digital painting that says NFT Collection Data.](img/963ce6dbc19c6595e5d4fe3a7d73b4af.png)

接下来，我们将首先解释什么是 NFT 集合数据，以及 NFT 集合存储是什么类型的数据。然后，我们将仔细研究 NFT 收藏的终极数据工具 Moralis Web3 API。在这里，您将更好地熟悉 Moralis NFT API 和" *getNFTContractMetadata* "和" *getContractNFTs* "端点。虽然这是获取 NFT 收集数据的两个核心工具，但你可以利用 Moralis 的 [Web3 基础设施](https://moralis.io/web3-infrastructure-exploring-the-best-solution-for-web3-development/)解决方案做得更好。例如，您可以使用 [Web3 streams](https://web3streams.com/) ，这使您能够创建[以太坊 webhooks](https://moralis.io/ethereum-webhooks-what-they-are-and-how-to-use-webhooks-for-ethereum/) 来毫不费力地将链上事件直接传输到您的后端。此外，您还希望使用 Moralis 的 [Auth API](https://moralis.io/authentication/) 为您的 dapp 配备 Web3 身份验证。

一旦您知道了上述两个端点接受什么参数以及如何测试它们，您就可以开始今天的教程了。当然，您可以在同一个脚本中组合这两个端点。然而，为了清楚起见，我们将向您展示如何使用" *getContractNFTs* "端点。毕竟后者为你提供了更多的细节。

![Two developers using various tools in their workspace.](img/7f614c4ffddb0b13b0cc6d36517c3af6.png)

## 什么是 NFT 收集数据？

NFT 收集数据指的是关于一个集合的不同信息。然而，我们通常将特定集合中关于 NFT 的细节称为 NFT 集合数据。因此，NFT 收集数据通常也指 NFT 元数据。此外，值得指出的是，可以将 NFT 分配给集合(通常都是这样)，但这不是必需的。毕竟，NFT 可以完全独立。然而，NFT 的创造者通常会在一个集合中分配大量的代币。一个很好的例子是 CryptoPunks 集合，它包括近 10，000 个 NFT。最终，为了知道什么是 NFT 集合数据，您需要正确理解什么是 NFTs 和 NFT 元数据。

![CryptoPunk NFT Collection Data](img/c1a03361775b85931a876fd0db55e42f.png)

### 什么是不可替换的令牌？

不可替换令牌(NFT)是唯一的不可互换的加密资产。每个 NFT 都有其唯一的令牌 ID(链上签名)，这使得这些令牌非常适合表示唯一的数字或物理项目。这就是为什么数字艺术和数字收藏品往往是 NFT 效用最常见的例子。也就是说，你应该记住，NFT 已经革新了许多行业(认证、所有权证明、票务、游戏等)。).

此外，您可能知道开发人员使用 NFT 智能合约创建(mint)NFT。后者是软件的链上部分，整合了他们关注的 NFT 的所有必需和可选的细节。此外，一个集合中的所有 NFT 背后都有相同的智能合约。因此，要从集合中获取 NFT，您需要关注适合该集合的智能契约。

![NFT metadata code outlined in a graph.](img/b080bfcbbbfce6fd9cd4ba3aae3268ab.png)

### 什么是 NFT 元数据？

NFT 元数据提供了与 NFT 相关的数据信息。此外，查看上面的图像应该会让您对 NFT 元数据包含的细节有一个很好的了解。还需要注意的是，NFT 元数据本身并不存储在区块链上，代表 NFT 的文件也不存储在上(通常是 JPEGs，但也可以是任何其他文件格式)。相反，开发人员使用云存储解决方案(最好是分散的)来存储这些文件和元数据文件。后者包括代表 NFT 的文件的位置链接(URL)。这就是为什么获得 NFT 元数据的技能也能让你获得代表 NFT 的文件。

此外，元数据文件通常是 JSON 格式的。指向这些文件(一旦在线存储)的链接被称为 URIs。请注意，NFT 元数据中包含的确切细节各不相同。然而，由于 NFT 标准已经确立(ERC-721，ERC-1155，SPL 等)，你通常知道你在处理什么。).例如，在 ERC-721 或 ERC-1155 标准的情况下，元数据通常包括描述、名称、代表 NFT 的文件目的地以及可选的属性或特征。要了解关于属性的更多信息，请查看我们的“ [*如何将属性添加到 NFT 元数据*](https://moralis.io/how-to-add-attributes-to-nft-metadata/) ”文章！

![Hologram showing a digital NFT.](img/78e522428360e299257aab812e2f4ec2.png)

## NFT 收藏中存储了哪些数据？

NFT 系列是由智能合约铸造和管理的。因此，NFT 系列中的细节就是该系列的智能合约所包含的细节。这些通常包括集合中 NFT 的总数、集合名称、集合符号、基本令牌 URI 以及该集合中各个 NFT 的所有细节。此外，一些最重要的 NFT 细节以 NFT 元数据(URIs)的形式出现。此外，后者包括代表 NFT 的文件和其他必需的和可选的细节，如上所述。然而，查看 NFT 集合中存储的数据类型的最佳方式是使用“ *getNFTContractMetadata* ”和“ *getContractNFTs* ”端点。

![Moralis' homepage with an arrow pointing at the Start for Free button.](img/bdd8feec1a6244d7df079b2cdf39b796.png)

## NFT 系列的终极数据工具

Moralis 是 NFT 集合的终极数据工具，特别是由于“ *getNFTContractMetadata* ”和“*getContractNFTs*”NFT API 端点。因此，我们鼓励您通过使用 Moralis 文档来仔细查看这两个端点。因此，让我们从下一节中的“ *getNFTContractMetadata* ”端点及其文档页面开始吧！

### 探索“getNFTContractMetadata”NFT API 端点

下面是[获取集合元数据端点](https://docs.moralis.io/reference/getnftcontractmetadata)的文档页面的截图:

![Documentation page showing the code to get NFT collection data, which is the get collection metadata endpoint.](img/9c88aa853e647eb9fcb8af6d33e63884.png)

正如您在上面的图像中看到的，该端点获取给定智能协定的集合(协定)级元数据。为此，它需要一个感兴趣的 NFT 合同的地址。而且，这使得“ ***地址*** ”参数必不可少。此外，“ *getNFTContractMetadata* ”端点还允许您使用“ ***chain*** ”参数选择要查询的链。

您可以使用上面页面的右上角部分来选择您想要使用的编程语言，并尝试上面图像中所示的代码。

### 探索“getContractNFTs”NFT API 端点

与获取集合级元数据的“ *getNFTContractMetadata* ”端点不同，“ *getContractNFTs* ”获取的细节要多得多。它还获取目标集合中所有 NFT 的元数据，并提供额外的可选参数。写完这篇文章后，一定要看看我们的另一篇文章，解释如何[从合同](https://moralis.io/how-to-get-all-nfts-from-a-contract/)中获得所有 NFT。也就是说，现在让我们确保浏览一下[通过合同文档获取 NFTs](https://docs.moralis.io/reference/getcontractnfts)页面:

![Showing all the information on the get NFTs by contract documentation page, including code snippets.](img/85ce3a13b89f652d63feac87fb9b7a28.png)

如前一节所述，您可以使用通过契约获取 NFTs 的文档页面，以“ *getContractNFTs* ”进行测试，并复制各种编程语言所需的代码行。

尽管如此，以下是该端点接受的所有参数:

*   "**地址**"**-该参数用于提供 NFT 智能合约地址，是唯一必需的参数。**
*   **"**链**"**–您可以使用该参数来确定将哪个可编程链作为目标(Moralis 支持所有领先的 Web3 网络)。****
*   ****"**格式**"**–此参数允许您确定要使用哪种类型的令牌 ID 格式(十进制或十六进制)。******
*   ******"**limit**"**–您可以使用该参数设置所需的结果页面大小。********
*   ******"**total range**"**–此参数允许您决定将结果分成多少个子范围。********
*   ******"**范围**"**-您可以使用此参数设置想要查询的子范围。********
*   ******"**cursor**"**–当您有超过 100 个 NFT 或希望每页显示更少的 NFT 时，此参数使您能够进入下一页。********
*   ******"**normalize metadata**"–如果您想要获取规范化的元数据，可以使用该参数。如果选择“true”，端点将在一个名为“ *normalized_metadata* ”的新对象中返回标准化结构的元数据。******

## ****如何用 Moralis 获取 NFT 馆藏数据****

****现在您已经知道了两个端点的要点，这两个端点使您能够获取 NFT 集合数据，现在是学习今天教程的时候了。由于" *getContractNFTs* "为您提供了更多的细节，我们将把我们的教程集中在这个端点上。不过使用“ *getNFTContractMetadata* 的步骤基本相同。因此，跟随我们下面的引导，你将确切地知道如何利用它。****

****首先，确保完成三个先决条件:****

*****   准备好自己喜欢的代码编辑器或者 IDE。我们倾向于使用 Visual Studio 代码(VSC)。*   安装 Node v.14 或更高版本。*   将您最喜欢的包管理器(" *npm* " *，* " *纱* " *，或* " *pnpm* ")设置到位。****

****![Wizard pointing at a billboard that states How to Get NFT Collection Data.](img/76343a896188524cb8025b1339ecfdd7.png)

### 步骤 1–建立 Moralis 观

您需要一个 Moralis 帐户来访问终极 Web3 API 的功能。因此，如果你还没有这样做，创建你的免费 Moralis 账户。然后，您将能够访问您的 Moralis 管理区并获得您的 Web3 API 密钥:

![Step 1, click on the Web3 APIs button. Step 2, copy the API key.](img/12c40fbaee9db56e0a906682e84d31a6.png)

现在，保持您的 API 密钥，并专注于在您的项目中安装 Moralis SDK。一个简单的命令就能解决问题；请确保使用与您的软件包管理器相匹配的命令:

```js
npm install moralis
```

```js
yarn add moralis
```

```js
pnpm add moralis
```

### 步骤 2:使用一个示例“Index.js”脚本

既然您已经访问了 Moralis，那么是时候创建一个示例脚本了，它充分结合了本文开头给出的代码行。当然，您可以简单地从我们的示例“index.js”脚本中复制粘贴以下代码行:

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

*注意* *:如果您要专注于使用“getNFTContractMetadata”端点，您可以使用完全相同的脚本，只需将“getContractNFTs”替换为“getnftcontractmetada”。*

看上面几行代码，可以看到“ *EvmChain。以太坊*”。我们使用后者来定义我们想要查询的链。当然，我们可以用其他[支持的链](https://docs.moralis.io/reference/supported-chains)替换*以太坊*，或者添加额外的链来查询多个链。尽管如此，您一定不要忘记用您在第一步中获得的 Web3 API 密钥替换“ *YOUR_API_KEY* ”占位符。

*注意:访问* [*文档页面，从集合*](https://docs.moralis.io/docs/how-to-get-all-the-nfts-from-a-collection) *中获取所有的 NFT，以复制上述“索引”脚本的打印版本。*

### 第三步:执行程序

此时，您应该已经准备好了上面几行代码，包括实际的 Web3 API 键。因此，您已经准备好执行程序并探索结果——所有的 NFT 收集数据。因此，在您的终端中输入以下命令:

```js
node index.js
```

*注意* *:如果你正在使用“index.ts”脚本，你将需要使用“node index.ts”命令来代替上面的命令。*

最后，您可以在您的终端中探索结果。如果您使用“0 XB 47 E3 CD 837 ddf 8e 4c 57 f 05d 70 ab 865 de 6e 193 BBB”地址(如上所述)，您应该会看到以下响应:

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

研究结果后，您可以直接看到“ *getContractNFTs* ”端点为您提供的所有 NFT 集合数据。例如，它甚至返回集合中 NFT 的总数，在上面的例子中是“ *9991* ”。

## NFT 收集数据-如何获取 NFT 收集数据-摘要

在今天的文章中，您了解了如何以最简单的方式获得 NFT 收集数据。一路上，你也学到了什么是 NFT 收集数据。也就是说，要完成本教程，您只需要一个免费的 Moralis 帐户来获得 Web3 API 密钥，这是使用所有 Moralis web 3 API 端点的网关。在获取 NFT 集合数据时，“ *getNFTContractMetadata* ”和“ *getContractNFTs* ”端点是终极工具。此外，您有机会熟悉这些工具，甚至在本文中使用它们。

知道如何获得 NFT 收集数据可能是有益的。毕竟，NFT 在许多 dapps 中扮演着重要的角色。有了这里获得的知识，你可以建立 NFT 投资组合追踪器、NFT 门控网站、Dao、社交图和许多其他类型的 NFT dapp。因此，我们强烈建议您使用 Moralis 文档来创建您的第一个 dapp。最好的事情是，您可以使用您最喜欢的遗留开发工具来这样做。

另一方面，您可能有兴趣探索其他区块链发展主题。在这种情况下，一定要访问[Moralis 伦理 YouTube 频道](https://www.youtube.com/c/MoralisWeb3)和[Moralis 伦理博客](https://moralis.io/blog/)。例如，一些最新的主题教你如何[获得钱包余额](https://moralis.io/get-wallet-balance-how-to-get-wallets-native-crypto-balance/)，如何[获得 NFT 元数据](https://moralis.io/get-nft-metadata-how-to-get-the-metadata-of-an-nft/)，[集成 WalletConnect 模态和二维码](https://moralis.io/how-to-integrate-the-walletconnect-modal-and-qr-code/)，等等。

当然，你也可以采取更专业的方式来接受加密教育，并获得区块链认证。在这种情况下，你应该报名参加 Moralis 学院，向成为网络 3 专家迈出第一步。“[区块链&比特币 101](https://academy.moralis.io/courses/blockchain-bitcoin-101) 课程是一个很好的起点。****