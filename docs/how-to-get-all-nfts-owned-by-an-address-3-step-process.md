# 如何获得一个地址拥有的所有 NFT–3 步流程

> 原文：<https://moralis.io/how-to-get-all-nfts-owned-by-an-address-3-step-process/>

构建 NFT 相关的 dapps(去中心化应用)需要最好的工具。由于终极的 NFT API，您可以轻松地为您的 dapps 集成特定的功能，例如让一个地址拥有所有的 NFT。要获取 address 拥有的所有 NFT，您可以使用以下包含" [getWalletNFTs](https://docs.moralis.io/reference/getwalletnfts) "端点的脚本:

```js
const Moralis = require("moralis").default;
const { EvmChain } = require("@moralisweb3/evm-utils");

const runApp = () => {
  await Moralis.start({
    apiKey: "YOUR_API_KEY",
    // ...and any other configuration
  });

  const address = "0xd8da6bf26964af9d7eed9e03e53415d37aa96045";

  const chain = EvmChain.ETHEREUM;

  const response = await Moralis.EvmApi.nft.getWalletNFTs({
     address,
     chain,
  });

  console.log(response);
}

runApp();
```

如果你以前和 [Moralis](https://moralis.io/) 一起工作过，你可能知道如何使用上面的代码行。因此，只需使用下面的链接进入文档页面即可立即开始。但是，如果这是您第一次参加 Moralis 的竞技表演，并且您想要一步一步地了解如何获得 address 拥有的所有 NFT，请务必完成今天的三步教程！

[**Documentation Page to Get All NFTs Owned by an Address**](https://docs.moralis.io/docs/how-to-get-all-nfts-owned-by-an-address)

### 概观

接下来，我们将首先对该主题进行适当的概述，以确保大家都知道什么是 NFTs 和 Web3 地址。然后，我们将仔细查看" *getWalletNFTs* "端点，我们还将研究它的参数。最后，我们将带您完成获得 address 拥有的所有 NFT 所需的三个步骤。

此外，我们将在本文中关注以太坊链。然而，我们也将解释如何调整单个代码片段来处理其他领先的可编程链。毕竟，Moralis 是关于跨链互操作性的。因此，Moralis 让您在主要的区块链网络上开发，包括 BNB 智能链、雪崩、多边形等等！也就是说，如果你想学习如何简单地获得 address 拥有的所有 NFT，创建你的[免费 Moralis 帐户](https://admin.moralis.io/register)并跟随我们的领导！

## 什么是 NFTs 和 Web3 地址？

不可替换的令牌是特殊类型的加密资产。与可替换令牌不同，NFT 是不可互换的。毕竟，每个 NFT 都有其独特的令牌 ID(链上签名),这使得它不同于任何其他 NFT。这一特性使得不可替换的代币非常适合数字艺术和数字收藏品。此外，由于 NFT 可以表示各种类型的文件，它们开始彻底改变现实世界的用例。此外，NFT 可以作为所有权、证书等的证明。当然，NFT 也在改变游戏行业。玩家可以通过令牌化(转换为 NFTs)游戏中的资产来真正拥有自己的游戏进度。因此，他们可以交易他们的非功能性游戏，并将游戏中的资产转移到世界经济中。

![A bag with NFT artwork pieces popping out of it.](img/8f91ac130946e59d7cd9546999888f89.png)

此外，值得指出的是，需要创造非功能性金融工具。这是执行在区块链上存储 NFT 元数据的链上事务的过程。此外，制造 NFT 是通过部署智能契约(软件的链上部分)来完成的，智能契约包含关于它们所关注的 NFT 的预定义条件和动作。此外，为了确保事情遵循既定的指导方针，不同的 NFT 标准有不同的智能合同。最常见的是 ERC-721 和 ERC-1155。请记住，每一个 NFT 都被分配到用于铸造它的智能合同。相应地，你也可以从合同中[获得所有的非功能性交易。](https://moralis.io/how-to-get-all-nfts-from-a-contract/)

![Web3 Wallet - MetaMask](img/ebeeb7c431157fed8fe30033dbdce098.png)

然而，一旦用户购买或获得 NFT 的所有权，后者将被转移到他们的 Web3 钱包中。此外，Web3 钱包可以有多种形式，但本质上，它是私钥和公钥的组合。公钥被称为区块链地址。因此，我们可以得到地址拥有的所有 NFT。

## NFT API 获取地址拥有的所有 NFT

本节详细介绍 Moralis 的" *getWalletNFTs* "端点。后者使 devs 能够毫不费力地获得 address 拥有的所有 NFT。此外，这个 NFT API 端点根据代码索引的合同返回包含“*【已同步/正在同步】*”状态的响应。此端点的结果包括所有索引的 NFT。任何包含“*token _ address*”参数的请求都将在脚本第一次请求时启动 NFT 集合的索引过程。此外，“ *getWalletNFTs* ”端点包括几个可选的查询参数，帮助您进一步细化搜索。

最后，以下是您在使用上述 NFT API 端点时可以使用的所有参数:

*   "**地址**"–这是 NFT 所有者的区块链地址，也是唯一必需的参数。
*   "**链**"**-此参数让您决定想要查询的链。您可以在所有[支持的链](https://docs.moralis.io/reference/supported-chains-for-nft-api)中进行选择。**
*   **"**格式**"**–您可以选择令牌 ID 的十进制或十六进制格式。****
*   ****"**限制**"**-该参数使您能够设置结果的所需页面大小。******
*   ******"**token _ addresses**"–您可以使用一个字符串数组来表示您想要获得余额的不同地址。******
*   ****"**cursor**"**-cursor 参数来自上一个响应，用于获取下一页。******

### ******如何亲自探索" *getWalletNFTs* "端点******

******如果您想探索" *getWalletNFTs* "端点，甚至查看它对特定参数的响应，请务必访问 [Moralis 文档](https://docs.moralis.io/reference/getwalletnfts):******

******![The get nfts by wallet page.](img/d9b17899581c25a479174123778802ba.png)

如上图所示，您必须先输入一个钱包地址。当然，你也可以添加任何可选参数。接下来，您必须在页面的右上角选择编程语言。最后，你可以点击“试试看！”按钮并查看下面的响应。然而，要看到这个 Moralis 的 NFT API 端点的真正威力，您需要粘贴您的 Moralis Web3 API 密钥。您可以在下面的“*步骤 1:设置 Moralis 规范*”一节中了解如何通过两次点击来获取密钥。

![Red tutorial button.](img/541a2d0812a70a19234418748b7e84ae.png)

## 3 步教程-如何获取地址拥有的所有 NFT

在我们向您介绍这个三步教程的细节之前，值得指出的是，能够获得 address 拥有的所有 NFT 是非常有用的。毕竟，您知道 NFT 在许多 dapps 中扮演着重要的角色。开发人员使用这些类型的令牌来代表区块链上一个独特项目的所有权，无论是虚拟的还是物理的。一些最常见的 NFT 公用事业用例包括 NFT 投资组合跟踪器、NFT 门户网站、Dao 和社交图。因此，所有这些都需要后端代码来获取 address 拥有的所有 NFT。因此，通过掌握即将到来的三个步骤，你将能够建立各种各样的 NFT dapp。

此外，在开始实现代码之前，您需要考虑一些先决条件:

*   您应该准备好 Node v.14 或更高版本。
*   安装并设置您最喜欢的代码编辑器或 IDE。我们更喜欢使用 Visual Studio 代码(VSC)。
*   另外，确保你已经安装了你最喜欢的包管理器(" *npm* "、" *yarn* "或" *pnpm* ")。

![A wizard pointing at a text that says how to get all nfts owned by an address.](img/23d9fb09a97b45aebc62e96783132720.png)

### 步骤 1:建立 Moralis 观

如果您还没有这样做，现在创建您的免费 Moralis 帐户。您可以使用本文开头的链接，或者访问 Moralis 主页，点击“免费开始”按钮:

![Button on Moralis' homepage that says start for free.](img/330470d3368a8063d9873f835af83e7a.png)

无论您选择哪条路径，您都将进入注册页面，在这里您需要输入您的详细信息:

![Create your account page.](img/d2fb53aa1549627ea2f30edf8bd68012.png)

一旦您输入您的全名、电子邮件地址和密码，并接受条款和条件，您就可以点击“注册”按钮。然后，你只需要点击你收件箱里的链接来确认你的账户。

准备好您的 Moralis 帐户后，您可以获得您的 Moralis Web3 API 密钥。为此，请在您的管理区选择“Web3 APIs”选项。然后，使用 API 密钥旁边的复制图标:

![Web3 API page.](img/3d6b89514298d4bc286b65dfe76187b8.png)

我们将很快向您展示粘贴 API 密钥的位置。然而，首先，您必须在您的项目中安装 Moralis SDK。为此，使用您的终端并输入以下命令之一(取决于您使用的软件包管理器):

```js
npm install moralis
```

```js
yarn add moralis
```

```js
pnpm add moralis
```

### 步骤 2:获取地址拥有的所有 NFT

安装了 Moralis SDK 后，您可以使用本文顶部提供的代码行。如果您还记得的话，端点“ *getWalletNFTs* ”是脚本的核心。它使用必需的“*地址*和可选的“*链*参数。因此，你必须决定你将关注哪条链，探索哪个地址。当然，您可以按照我们的思路，使用“index”脚本中的示例地址，并关注以太坊链。

通过查看下面的代码行，您可以看到我们使用了" *EvmChain。以太坊*”来定义我们要关注的链条。因此，如果您将注意力转移到任何其他链上，您就需要更改那一行代码。

以下是支持的 EVM 兼容链和您需要用以下代码片段替换"*以太坊*"的代码片段:

*   伊琳说"好"
*   以太坊 Sepolia:“Sepolia”
*   Polygon Mainnet: “POLYGON”
*   多边形孟买测试网:“孟买”
*   BNB 智能连锁 Mainnet:“BSC”
*   BNB 智能链测试网:“BSC_TESTNET”
*   雪崩 C 链:“雪崩”
*   雪崩富士测试网:“富士”
*   Fantom: “FANTOM”
*   克罗诺斯维护网:“克罗诺斯”
*   CRONOS Testnet:“CRONOS _ Testnet”

*注意:除了上面的链，还可以使用 Moralis 拉斯* [*索拉纳 API*](https://moralis.io/solana-api/) *。然而，由于 Solana 处于非 EVM 兼容的链中，您需要调整其他代码行并使用不同的 API 端点。*

![JS vs TS.](img/7e8151dbfc5d5b400e940fd7bce23f99.png)

#### 使用 JavaScript 或类型脚本

下面是与简介中相同的代码。然而，我们在下面针对 TypeScript (TS)进行了优化，尽管它最初是 JavaScript (JS)格式的。这就是使您能够在以太坊上获得 address 拥有的所有 NFT 的“index.ts”脚本的样子:

```js
import Moralis from "moralis";
import { EvmChain } from "@moralisweb3/evm-utils";

const runApp = () => {
  await Moralis.start({
    apiKey: "YOUR_API_KEY",
    // ...and any other configuration
  });

  const address = "0xd8da6bf26964af9d7eed9e03e53415d37aa96045";

  const chain = EvmChain.ETHEREUM;

  const response = await Moralis.EvmApi.nft.getWalletNFTs({
     address,
     chain,
  });

  console.log(response);
}

runApp();
```

无论您使用 JS 还是 TS，不要忘记用您的 Web3 API 密钥替换“ *YOUR_API_KEY* ”占位符。此外，也可以随意使用其他地址和链，如上所述。

### 第三步:执行程序并探索结果

准备好“index.js”或“index.ts”文件后，就该执行程序了。因此，请使用以下命令之一:

```js
node index.js
```

```js
node index.ts
```

运行适当的命令后，您将在终端中看到结果。下面是以太坊上“*0 xd 8 da 6 BF 26964 af 9d 7 eed 9 e 03 e 53415d 37 aa 96045*”地址的结果:

```js
{
  "total": 1456,
  "page": 1,
  "page_size": 100,
  "cursor": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjdXN0b21QYXJhbXMiOnsid2FsbGV0QWRkcmVzcyI6IjB4ZDhkYTZiZjI2OTY0YWY5ZDdlZWQ5ZTAzZTUzNDE1ZDM3YWE5NjA0NSJ9LCJrZXlzIjpbIjE2NjMyMzgxNzUuMDc3Il0sIndoZXJlIjp7Im93bmVyX29mIjoiMHhkOGRhNmJmMjY5NjRhZjlkN2VlZDllMDNlNTM0MTVkMzdhYTk2MDQ1In0sImxpbWl0IjoxMDAsIm9mZnNldCI6MCwib3JkZXIiOltdLCJ0b3RhbCI6MTQ1NiwicGFnZSI6MSwidGFpbE9mZnNldCI6MSwiaWF0IjoxNjY2NjgyNTUyfQ.E5DkWYvRTaFnVhgedRuT3IW-rb2V-ikFKwP2cg2Qf78",
  "result": [
    {
      "token_address": "0x57f1887a8bf19b14fc0df6fd9b2acc9af147ea85",
      "token_id": "4765809967066625256798886812262830659450023020194524584471225959000376492819",
      "amount": "1",
      "owner_of": "0xd8da6bf26964af9d7eed9e03e53415d37aa96045",
      "token_hash": "ba6d44b5f16be94283cecffeb784b7ca",
      "block_number_minted": "15572796",
      "block_number": "15573017",
      "contract_type": "ERC721",
      "name": "Ethereum Name Service",
      "symbol": "ENS",
      "token_uri": null,
      "metadata": null,
      "last_token_uri_sync": null,
      "last_metadata_sync": "2022-09-20T06:06:08.153Z",
      "minter_address": null
    },
    {
      "token_address": "0x57f1887a8bf19b14fc0df6fd9b2acc9af147ea85",
      "token_id": "84453794918345416145331514647027903846664455083247396107154093349515123913389",
      "amount": "1",
      "owner_of": "0xd8da6bf26964af9d7eed9e03e53415d37aa96045",
      "token_hash": "7c0212cd3daf1b6b64f193c6dc102fb4",
      "block_number_minted": "15572811",
      "block_number": "15573017",
      "contract_type": "ERC721",
      "name": "Ethereum Name Service",
      "symbol": "ENS",
      "token_uri": null,
      "metadata": null,
      "last_token_uri_sync": null,
      "last_metadata_sync": "2022-09-20T06:09:09.838Z",
      "minter_address": null
    },
    {
      "token_address": "0x57f1887a8bf19b14fc0df6fd9b2acc9af147ea85",
      "token_id": "16476931145019337030786748713476010946621971075817308111460324192065814192354",
      "amount": "1",
      "owner_of": "0xd8da6bf26964af9d7eed9e03e53415d37aa96045",
      "token_hash": "627ffc76405a90ee940cb91f7e90b294",
      "block_number_minted": "15572818",
      "block_number": "15573017",
      "contract_type": "ERC721",
      "name": "Ethereum Name Service",
      "symbol": "ENS",
      "token_uri": null,
      "metadata": null,
      "last_token_uri_sync": null,
      "last_metadata_sync": "2022-09-20T06:11:34.545Z",
      "minter_address": null
    },
  ],
  "status": "SYNCED"
}
```

我们鼓励您针对不同链上的不同地址运行上述程序，并探索您的终端返回的结果。然后，通过创建一个实际的 dapp 来进一步使用您的新功能，该 dapp 将显示用户的 NFT，或者根据他们对特定 NFT 的所有权授予他们访问权限。如果这听起来很有趣，请确保在我们的文档中使用我们的“ *NFT 门户网站*”教程。

然而，如果你对区块链游戏开发感兴趣，我们的 Web3 Unity 内容正是你所需要的。后者在 [Moralis YouTube 频道](https://www.youtube.com/c/MoralisWeb3)和 [Moralis 博客](https://moralis.io/blog/)等你。

![Tutorial page showing multiple Unity lessons.](img/fcc1b8cb7f466b264729428c4a9bc94f.png)

## 如何获取一个地址拥有的所有 NFT–3 步流程–总结

我们在今天的文章中涉及了很多内容。首先，我们对 NFTs 和 Web3 钱包做了一个快速的概述，在这里你也了解了什么是区块链地址。接下来，我们仔细研究了 Moralis NFT API 端点——“getWalletNFTs”。这是您发现可以使用 Moralis 文档测试这个端点(以及所有其他端点)的地方。您还学习了如何轻松地选择编程语言并复制适当的代码行。最后，我们向您介绍了演示如何毫不费力地获得 address 拥有的所有 NFT 的三步教程。因此，您有机会完成以下三个步骤:

1.  树立 Moralis 观
2.  创建一个脚本来获取地址拥有的所有 NFT
3.  执行程序并探索结果

通过使用这里获得的知识和技能，你可以很容易地开始创造一些杀手 dapps。有了 Moralis 文档，您应该能够使用自己喜欢的编程框架来完成这项工作。此外，你可以坚持 NFT 公用事业或转移你的重点到其他类型的 dapps。无论哪种情况，您都可以从其他 Moralis 资源中获得额外的指导。我们的 YouTube 频道和博客都是免费支持你正在进行的加密教育的好渠道。我们最近的一些话题涵盖了最好的[加密钱包 API](https://moralis.io/crypto-wallet-integration-using-the-best-crypto-wallet-api/) ，最好的 [Web3 提供商](https://moralis.io/web3-provider-why-blockchain-developers-should-use-one/)， [Web3 商业版](https://moralis.io/web3-for-business-how-and-why-you-can-integrate-web3-into-your-enterprise/)，一个 [Web3 JS 教程](https://moralis.io/web3-js-tutorial-for-blockchain-developers/)，构建一个 [Web3 Unity 多人游戏](https://moralis.io/how-to-build-a-web3-multiplayer-game-using-unity-multiplayer/)，等等。

当然，你还可以通过注册[Moralis 学院](https://academy.moralis.io/)来加速你成为区块链专家的进程。在那里你可以探索区块链发展的方方面面。如果你是加密领域的新手，我们建议从[区块链和比特币基础](https://academy.moralis.io/courses/blockchain-bitcoin-101)开始。******