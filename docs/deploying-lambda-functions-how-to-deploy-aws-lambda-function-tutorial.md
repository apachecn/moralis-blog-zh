# 部署 Lambda 函数–如何部署 AWS Lambda 函数教程

> 原文：<https://moralis.io/deploying-lambda-functions-how-to-deploy-aws-lambda-function-tutorial/>

在本教程中，您将学习如何使用[](https://moralis.io)****部署 AWS Lambda 函数！此外，本教程还演示了如何创建和部署具有多种功能的 Lambda 应用程序。更重要的是，由于 Moralis 的能力和 Web3 开发工具，您将能够通过四个简单的步骤来实现这一点:****

***   部署 Lambda 函数-先决条件*   项目设置*   开发应用程序*   测试和部署 AWS Lambda 函数**

**如果你一直坚持到最后，你将学会如何通过 AWS Lambda 和 Moralis 运行 Web3 JavaScript 函数！此外，如果这听起来令人兴奋，并且您想直接进入教程，请立即跳到“ [*教程，了解如何使用 Moralis*](https://docs.google.com/document/d/13WNAysgt4Xg03nhcGhFn_bS0hy6p0Wg0adWIbItd_1I/edit?pli=1#heading=h.qxmeq75979i3) 部署 AWS Lambda 函数”部分！你也可以查看 Moralis 官方的 AWS Lambda 的 [Web3 文档页面或者下面 Lambda 应用的 GitHub 库:](https://docs.moralis.io/docs/using-aws-lambda)**

****完整的 AWS Lambda 应用代码—**[**https://github . com/moralis web 3/examples-AWS-Lambda-nodejs/tree/main/AWS-node-project**](https://github.com/MoralisWeb3/examples-aws-lambda-nodejs/tree/main/aws-node-project)**

**![](img/5b1b3afc01fef22484e10170042b78bc.png)[**Sign Up with Moralis**](https://admin.moralis.io/login)

### 概观

AWS 是“亚马逊网络服务”的缩写，是市场上最著名的云计算平台之一。AWS 由各种产品和服务组成，其中之一就是 AWS Lambda。此外，Lambda 是一种计算服务，使开发人员能够运行代码，而不必担心相关的管理任务，如管理操作系统访问控制、供应服务器、扩展等。相反，开发人员有更多的时间关注核心产品和业务逻辑。然而，这实际上是如何工作的，你如何上传一个 AWS Lambda 函数？

![AWS](img/8868d9c27802456feb35332934a93f52.png)

如果您有兴趣知道这个问题的答案，请加入我们，因为我们在本文中提供了如何使用 Moralis 上传 AWS Lambda 函数的完整演练。此外，在深入核心部分之前，本指南还提供了对 AWS Lambda 的简要介绍。但是，如果你觉得这不是一个足够的概述，或者想要更多关于服务的细节，请查看我们关于 [AWS Lambda 的指南以及它用于](https://moralis.io/exploring-aws-lambda-and-what-it-is-used-for/)的用途！

Moralis [AWS Lambda NodeJS](https://moralis.io/aws-lambda-nodejs-tutorial-how-to-integrate-a-nodejs-sdk-example/) 集成负责本教程中显示的可访问性。然而，它只是 Moralis 给你带来的众多便利之一。另一个很好的例子是由 Moralis 提供的各种[web 3 API](https://moralis.io/web3-apis-exploring-the-top-5-blockchain-apis/)！例如，如果你想了解更多这方面的知识，请查看 [EVM API](https://moralis.io/evm-api/) ，让你轻松创建 EVM 兼容的项目！

然而，在继续这篇文章之前，[在 Moralis](https://admin.moralis.io/register) 上注册，因为需要一个帐户才能继续！更重要的是，创建一个帐户是完全免费的，只需要几秒钟就可以设置好！

## AWS Lambda 和 Lambda 函数介绍

在向您展示如何上传函数之前，理解 AWS Lambda 的复杂性是有益的。因此，这个初始部分通过一个快速介绍简要地探索了 AWS Lambda 和服务的功能！那么，AWS Lambda 到底是什么？

![](img/15a45f2a9e40253c39c6bee9d874e703.png)

AWS Lambda 是基于事件驱动的无服务器架构的计算服务。AWS Lambda 负责与计算基础设施相关的繁重工作。因此，该服务提供了运行代码的机会，而无需管理或供应服务器。这进一步意味着您可以运行来自任何后端服务和应用程序的代码，您所需要的只是代码！

向 AWS Lambda 上传代码时，需要以“Lambda 函数”的形式组织。这些函数附有信息，如资源需求、入口点、名称等。此外，AWS Lambda 只在被请求时运行函数，您只需为它们消耗的计算时间付费。因此，当需求波动时，AWS Lambda 提供了削减成本和扩大规模的绝佳机会！

尽管如此，如果你想进一步了解这个服务以及它是如何工作的，查看这篇文章[更详细地解释 AWS Lambda 函数和架构](https://moralis.io/how-aws-lambda-works-functions-and-architecture-explained/)！

这就是 AWS Lambda 的快速介绍。现在是时候进入本文的中心部分了，在这里我们将向您展示如何使用 Moralis 部署 AWS Lambda 函数！

## 关于如何使用 Moralis 部署 AWS Lambda 函数的教程

随着对 AWS Lambda 和该服务的功能有了更深入的理解，现在是讨论本文主要部分的时候了。因此，以下部分将演示如何使用 Moralis 部署 AWS Lambda 函数。这样，您将学习如何创建和上传一个 AWS Lambda 应用程序，该应用程序具有多个基于 Web3 的功能。因此，在本教程结束时，您将知道如何使用 Moralis 通过 Lambda 运行 Web3 JavaScript 代码！

![](img/bbe526810ddfeef0a8b0ea32b29b0b25.png)

由于 Moralis 的能力，我们可以将这个"*如何部署 AWS Lambda 函数*"教程分成三个部分，每个部分都以简单明了的方式解释了该过程的核心部分:

*   部署 Lambda 函数-先决条件
*   项目设置
*   开发应用程序
*   测试和部署 AWS Lambda 函数

因此，如果您想学习如何上传 AWS Lambda 函数，请跟随我们更详细地讨论前面提到的部分。然而，事不宜迟，让我们直接进入教程的第一部分，并涵盖所需的先决条件！

## 部署 Lambda 函数-先决条件

在开始开发和部署 Lambda 函数之前，有几个先决条件需要处理。更具体地说，总共有七个:

1.  Moralis 账户–你首先需要的是一个 Moralis 账户。因此，如果你还没有，[立即加入 Moralis 家](https://admin.moralis.io/register)！

2.  **集成开发环境(IDE)**–接下来，您需要下载并安装一个 IDE。我们推荐 Visual Studio 代码(VSC ),因为这是我们在整个教程中使用的环境。

3.  **NodeJS**–为了跟进，您需要 NodeJS 运行时环境，可以从这里下载:【https://nodejs.org/en/】T2。

4.  **无服务器框架**——另外，你还需要无服务器框架。你可以通过[点击这里](https://www.serverless.com/framework/docs/getting-started#installation)找到如何设置框架的教程。

5.  **AWS 账户**–进入 AWS 网站[创建账户](https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-creating.html)。

6.  **AWS 命令行界面(CLI)**——接下来需要设置 AWS CLI，在这里可以找到设置指南[。](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html#getting-started-install-instructions)

7.  **IAM 用户**–最后，最后一个先决条件是 IAM 用户。登录 AWS 并打开 IAM 控制台来创建用户。然后，您必须单击导航菜单中的“用户”和“添加用户”。执行此操作时，您应该会看到以下页面，您必须在其中输入用户名并选中两种 AWS 凭据类型的复选框:

![](img/4648cd18532248f4a91b0436f11b0542.png)

在添加新用户的第二阶段，还要确保添加“AdministratorAccess”权限:

![](img/9167f6590ba845128dc3a5db5ec8d839.png)

最后，根据您的需求完成前面的每个步骤来配置您的帐户。当您进行到第五步，也是最后一步时，请确保下载一个。csv”文件:

![](img/45a5eefd9195bf353f9cfba85fae90ee.png)

这涵盖了七个先决条件！现在，让我们通过向您展示如何设置项目来进行学习吧！

## 项目设置

是时候立项了！首先，我们将向您展示如何配置您的 AWS 凭证。因此，要继续，请打开一个新的终端。如果您使用的是 VSC，您可以点击顶部的“终端”，然后点击“新终端”:

![](img/d3f69edf940c7b5dc1eba9477b80c60b.png)

现在，由于您在上一节中安装了 AWS CLI，您可以通过运行以下命令来配置您的 AWS 凭据:

```js
aws configure
```

一旦运行“ *aws configure* ”，您将需要在终端中输入一些数据并进行一些选择。因此，首先输入您的“ *AWS 访问密钥 ID* ”。其次，对“ *AWS 秘密访问密钥”*进行同样的操作。最后，对于区域名称和输出格式，按 enter 键。最终，它应该是这样的:

```js
AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE
AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
Default region name [None]: ENTER
Default output format [None]: ENTER
```

### 建立框架

在这一小节中，我们将向您展示如何使用无服务器框架工具来设置项目的准系统状态。因此，若要继续，请创建一个新文件夹并用 IDE 打开它。然后，您可以打开一个新的终端并运行以下命令:

```js
serverless
```

然后，您必须做出一些决定，首先，为初始提示选择“Starter”选项:

![](img/e4a48c25be8dc99bb8980841c2a340c0.png)

接下来，您需要命名项目。在这里，您可以自己输入一个名称，也可以立即单击 enter 选择一个默认选项:

![](img/196eb0e4ee7572c2fe204eeff8b17d3b.png)

当你点击“回车”选择名称时，一个无服务器的框架项目将被下载。当它完成时，终端会要求您登录。然而，对于本教程，您可以通过输入“ *n* ”并按 enter 键跳过这一步:

![](img/78e661aaf2fb0d5dce11a6c9f03be349.png)

从那里，您可以选择部署项目。但是，您可以将此推迟一会儿，然后再次输入“ *n* ”并按 enter 键继续:

![](img/e3b0dd87291f63a5f5eaa2f1627254de.png)

如果您准确地遵循了这些步骤，您现在应该有一个与下图所示结构相似的项目:

![](img/18d777ee079958721e09d3fe0a788264.png)

但是，这只是一个模板，还需要做一些配置。首先，创建一个新的“函数”文件夹:

![](img/3590c2af056fc532934e96694bb558a6.png)

然后，您可以将“handler.js”文件移动到这个新创建的文件夹中:

![](img/64f4bad5854ed0b3294af93f0b421f1e.png)

最后，您需要添加您的 Moralis API 密钥，这可以通过用以下代码片段替换“serverless.yml”文件中的代码来完成:

```js
service: aws-node-project

frameworkVersion: '3'

provider:
  name: aws
  runtime: nodejs14.x
  environment:
    MORALIS_API_KEY: 'replace_me'

functions:
  hello:
    handler: functions/handler.hello
```

如果仔细观察代码，您会注意到“ *replace_me* ”部分，您需要向其中添加密钥。要找到密钥，请登录 Moralis 管理面板，点击左侧的“Web3 APIs”。从那里，复制密钥并将其输入到代码中:

![](img/d27f334bbf7f42acd992fa5ee0eecce6.png)

## 开发应用程序

随着无服务器框架模板的使用和必要配置的完成，现在是本教程的核心部分，我们将向您展示如何为 Lambda 应用程序添加代码。具体来说，在下面几节中，我们将向您展示如何创建两个函数:“ *getNativeBalance()* ”和“ *getWalletNfts()* ”。

然而，在深入研究这些函数的代码之前，您必须安装 Moralis 依赖项。因此，再次打开终端，将“*CD”*放入项目的根文件夹，并运行以下命令:

```js
npm install moralis
```

运行上面的命令将安装 Moralis，现在您已经准备好开始创建第一个" *getNativeBalance()* "函数了！

### **【getNativeBalance()**函数**

**首先，将“handler.js”文件的名称改为“getNativeBalance.js”:**

**![](img/58d0894d7c9a68c357de495cba88e2d4.png)

然后，您可以打开文件，并通过将“ *module.exports.hello* ”替换为“ *module.exports.handler* ”来继续操作:

![](img/50bd7caaabf483298db29b7955e2ee4d.png)

在这里，您需要在“serverless.yml”文件中更改函数的名称和处理程序:

![](img/36f9bab957b6d1b1d9a81fe382326f3a.png)

接下来，导航回“getNativeBalance.js”文件并添加 Moralis 的“ *getNativeBalance()* ”功能，首先输入 Moralis 要求:

```js
const Moralis = require('moralis').default;
```

接下来，您必须用前面指定的 Web3 API 密钥初始化 Moralis。因此，在 Moralis 要求下输入以下代码片段:

```js
const startMoralis = async () => {
  await Moralis.start({
    apiKey: process.env.MORALIS_API_KEY
  });
};

startMoralis();
```

最后，您需要做的最后一件事是用下面的代码替换完整的" *module.exports.handler* "部分。这样，您将实现正确的 SDK 方法:

```js
module.exports.handler = async (event) => {
  // Get native balance
  const nativeBalance = await Moralis.EvmApi.balance.getNativeBalance({
    address: event.address,
    chain: event.chain
  });

  // Format the native balance formatted in ether via the .ether getter
  const nativeBalanceEther = nativeBalance.result.balance.ether;

  return {
    result: nativeBalanceEther
  }
};
```

这涵盖了第一个" *getNativeBalance()* "函数，现在您应该有一个类似于下面的文件:

```js
'use strict';
const Moralis = require('moralis').default;

const startMoralis = async () => {
  await Moralis.start({
    apiKey: process.env.MORALIS_API_KEY
  });
};

startMoralis();

module.exports.handler = async (event) => {
  // Get native balance
  const nativeBalance = await Moralis.EvmApi.balance.getNativeBalance({
    address: event.address,
    chain: event.chain
  });

  // Format the native balance formatted in ether via the .ether getter
  const nativeBalanceEther = nativeBalance.result.balance.ether;

  return {
    result: nativeBalanceEther
  }
};
```

### *getWalletNfts()**函数*

*接下来我们要添加的函数是“ *getWalletNfts()* ”，我们可以按照与初始函数相同的步骤。然而，由于我们之前使用了“handler.js”文件，您需要从头开始创建一个新文件。因此，在“functions”文件夹中创建一个名为“getWalletNfts.js”的新文件:*

*![](img/2f0cc6cdaa168a7602fadc4c8b48e7ea.png)

接下来，打开“serverless.yml”并将函数添加到“*functions”*部分:

![](img/37ed5368954f01b716016f54ace302d6.png)

最后，将以下代码添加到“getWalletNfts.js”文件中:

```js
'use strict';
const Moralis = require('moralis').default;

const startMoralis = async () => {
  await Moralis.start({
    apiKey: process.env.MORALIS_API_KEY,
  });
};

startMoralis();

module.exports.handler = async (event) => {
  // Get wallet NFTs
  const nfts = await Moralis.EvmApi.nft.getWalletNFTs({
    address: event.address,
    chain: event.chain,
    limit: 10
  });

  return {
    result: JSON.stringify(nfts)
  }
};
```

以上就是" *getWalletNfts()* "函数！剩下的工作就是测试和部署 Lambda 的功能，我们将在下一节向您展示如何做！

## 测试和部署 AWS Lambda 函数

现在您已经完成了 Lambda 应用程序和两个函数，是时候确保一切正常工作了。因此，我们将从向您展示如何运行本地测试开始这一部分。因此，首先，创建一个名为“event.json”的新文件:

![](img/74a38378e0c420149a6a5a6eefb44170.png)

在这里，将钱包地址和链 ID 作为参数添加到文件中。它应该是这样的:

```js
{
    "address": "0x99EXAMPLEADDRESS",
    "chain": "chain_id"
}
```

一旦添加了钱包地址和链 ID，就可以运行测试了。因此，假设您想要尝试“ *getNativeBalance()* ”函数。在这种情况下，打开一个新的终端，并运行以下命令:

```js
serverless invoke -f getNativeBalance --path event.json
```

如果该功能正常工作，终端应该返回一个类似于下面的成功消息:

![](img/44ae3ada47f8958656aac15fb550dd92.png)

一旦您知道函数按预期工作，您必须部署您的 AWS Lambda 应用程序。为了部署 Lambda 函数，请确保您位于项目的根文件夹中，并在新的终端中运行以下命令:

```js
serverless deploy
```

如果部署过程成功，您应该会收到如下消息:

![](img/2863809f737595cf06408d2c8bf4ab0a.png)

就是这样！恭喜您，您现在已经成功地使用 Moralis 部署了 AWS Lambda 函数！

如果你有任何问题，请查看官方 AWS Lambda 文档。您还可以加入 Moralis 的 Discord 频道，从我们的工程师那里获得专家帮助！

## 摘要–如何部署 AWS Lambda 函数

在本文中，您了解了如何使用 Moralis 部署 AWS Lambda 函数。此外，由于 AWS Lambda NodeJS 集成的可访问性，您只需简单的四个步骤就能做到:

1.  部署 Lambda 函数-先决条件
2.  项目设置
3.  开发应用程序
4.  测试和部署 AWS Lambda 函数

上面的步骤将教你如何创建和部署一个具有多种功能的 Lambda 应用程序。因此，您可以使用 Moralis 通过 AWS Lambda 直接运行 Web3 JavaScript 代码！

如果你觉得这篇关于部署 Lambda 函数的教程很有帮助，你可能想在 Moralis 的 [Web3 博客](https://moralis.io/blog/)查看更多内容。例如，学习如何[将 IPFS 用于 NFT 元数据](https://moralis.io/ipfs-nft-how-to-use-ipfs-for-nft-metadata/)或探索[多边形 webhooks](https://moralis.io/polygon-webhooks-how-to-use-webhooks-on-polygon/) ！

此外，如果你想成为一名更熟练的区块链开发者，去看看[Moralis 学院](https://academy.moralis.io)！该学院为新的和更有经验的开发人员提供了很好的区块链课程。例如，如果你是这个领域的新手，通过下面的课程学习 Web3 开发的基础知识:“[以太坊基础](https://academy.moralis.io/courses/ethereum-101)”。

![](img/fc7a6bf5592ce8576971d33668613f29.png)

尽管如此，无论你是想继续部署 AWS Lambda 功能还是构建其他 Web3 项目，[都要注册 Moralis](https://admin.moralis.io/register) ！这样，您可以充分利用区块链技术的力量，获得更加无缝的 Web3 开发体验！*****