# Web3 AWS Lambda–通过 AWS Lambda Web3 提供程序使用 web 3 的 AWS

> 原文：<https://moralis.io/web3-aws-lambda-use-aws-for-web3-with-an-aws-lambda-web3-provider/>

**如果你对区块链编程感兴趣，并且想将 AWS Lambda 用于 Web3，请跟随本教程，它演示了如何通过三个简单的步骤构建和部署 Web3 AWS Lambda 应用:**

1.  涵盖先决条件
2.  设置新项目
3.  开发 Lambda 应用程序

通过涵盖以上步骤，您将学习如何通过将[Moralis 规范](https://moralis.io)节点 SDK 与服务集成来[创建 AWS Lambda 函数](https://moralis.io/creating-a-lambda-function-learn-how-to-create-an-aws-lambda-function/)。通过完成这个 Web3 AWS 教程，你将能够用 Lambda 运行 Web3 JavaScript 代码，你可以在所有未来的区块链项目中实现它！

如果这听起来令人兴奋，并且你想立即开始，你可以通过访问下面的“ *AWS Web3 教程*”部分进入教程。此外，你可以查看 AWS Lambda 的 [Web3 文档页面，以及下面的应用程序的完整 GitHub 库:](https://docs.moralis.io/docs/using-aws-lambda)

**完成 Web3 AWS Lambda 文档—[https://github . com/moralis web 3/examples-AWS-Lambda-nodejs/tree/main/AWS-node-project](https://github.com/MoralisWeb3/examples-aws-lambda-nodejs/tree/main/aws-node-project)T3】**

### 概观

你对 AWS 感兴趣并想利用 Lambda 创建复杂的 Web3 项目吗？如果是这样，请加入我们的 AWS Lambda 教程，教你如何开发和部署一个具有多种功能的 Web3 就绪 Lambda 应用程序。具体来说，您将学习如何创建获取本机令牌/NFT 余额的函数，并使用 AWS Lambda 运行代码！

此外，在向您展示如何创建 Lambda 函数的同时，本文还涵盖了该服务的复杂性以及它在 Web3 上下文中的含义。因此，我们将通过介绍最佳 AWS Web3 Lambda 解决方案——Moralis，来探讨如何让 AWS Web3 做好准备。然而，如果你想要一个更详细的分类，看看我们关于 [AWS Lambda 的文章以及它在](https://moralis.io/exploring-aws-lambda-and-what-it-is-used-for/)中的用途。

![Exploring Web3 WAS Lambda and what it is used for.](img/3754cb5adbb066549ba83c5c0676d6ad.png)

如果你已经熟悉这项服务，你可能想在 Moralis 的 [Web3 博客](https://moralis.io/blog/)查看更多内容。例如，看看我们回答问题的文章，“[什么是游戏公园](https://moralis.io/aws-gamesparks-guide-what-is-gamesparks/)？”。

尽管如此，在继续前进之前，[立即向 Moralis](https://admin.moralis.io/register) 注册，因为你必须有一个账户来跟进！此外，通过 Moralis 帐户，您可以访问其他工具，如 Moralis 的[web 3 API](https://moralis.io/web3-apis-exploring-the-top-5-blockchain-apis/)，以充分利用区块链技术的力量！

## AWS for Web3–什么是 AWS、Lambda 和 web 3？

为了充分理解 AWS 和 Lambda 在 Web3 环境中的作用，这一部分将分别分解这三个组件。因此，首先，我们将通过回答以下问题开始:“什么是 AWS？”。

![AWS](img/98b14f9cdffcf24b0a82f2c11a6c46fc.png)

AWS 是“Amazon Web Services”的缩写，它是全球范围内最广泛和被采用的云平台。AWS 提供 200 多种服务，从基础设施技术，如数据库、存储和计算解决方案，到新兴技术，如人工智能、机器学习等。通过利用 AWS，您可以利用最新的技术以更快的速度进行创新和实验，从而提供显著的竞争优势，尤其是在像 Web3 这样快速发展的行业中。

在亚马逊全面的 AWS 生态系统中，你会发现 Lambda，一种无服务器、事件驱动的计算服务。有了 AWS Lambda，开发人员可以运行代码，而不必担心服务器或集群。他们所需要做的就是以“Lambda 函数”的形式编写和上传代码，剩下的就交给服务了！

Lambda 函数是这个服务的主干，它们基于事件触发，这意味着 Lambda 只在必要时调用它们。一些突出的例子包括 HTTP 请求、亚马逊 S3 中的对象修改、DynamoDB 中的表更新等。此外，由于 Lambda 只在需要时运行函数，开发人员只需为代码消耗的计算时间付费。因此，Lambda 为扩展和降低成本提供了绝佳的机会。

简要介绍了 AWS 和 Lambda 如果你想了解更多关于这个服务的信息以及它是如何工作的，请查看我们的文章[来更详细地解释 AWS Lambda 函数和架构](https://moralis.io/how-aws-lambda-works-functions-and-architecture-explained/)！

尽管如此，既然您已经熟悉了 AWS Lambda，下面的小节将简要介绍最后一个组件:Web3！

### 什么是 Web3？

通俗地说，Web3 被广泛理解为最新的——也是第三代——互联网。最初的“阶段”或“生成”通常被称为 Web1。在这个阶段，用户主要消费和阅读内容，这表明体验是相对静态的。

随着知名社交媒体集团的崛起，网络从静态的内容消费转向更加动态和互动的元素。因此，用户不再局限于阅读信息，而是可以自己创建内容。然而，Web2 革命带来了与集中化相关的重大问题，例如将大量个人数据置于大型企业和社交媒体平台手中。为了解决这些问题，我们引入了第三代互联网:Web3。

![A chart depicting the history of the web and what came before AWS Lambda Web3.](img/8a37ac39a0f39271cffa5e64f5935592.png)

Web3 旨在保留 Web2 的积极动态方面，同时通过创建一个去中心化的互联网来消除中心化的问题。因此，Web3 的主要目的之一是创建一个数据不归大公司所有，而是由用户共享的互联网。这种转变为新兴和现有公司提供了通过创新和颠覆传统商业模式来争夺市场份额的巨大机遇！

如果你想了解更多关于 Web3 及其工作原理的信息，可以看看下面这篇文章:“[*web 3*](https://moralis.io/the-ultimate-guide-to-web3-what-is-web3/)终极指南”。

尽管如此，通过对 AWS、Lambda 和 Web3 的简要介绍，下一节将解释如何准备好 AWS Web3！

## 如何准备好 AWS Web3

在传统的 Web2 开发中，AWS 和 Lambda 通常用于构建应用程序、网站和其他软件项目。然而，随着 Web3 的兴起，区块链开发者现在正在寻找方便 AWS Web3 的方法。这样，他们可以在 Web3 开发工作中利用 Lambda 等著名服务来更快、更有效地创建 dapps！

![AWS Lambda logo in white.](img/7bc157fe38677a526d369c2f4b9cbf18.png)

不幸的是，这说起来容易做起来难，这就是为什么开发者对像 Moralis 这样的 Web3 基础设施提供商有很高的需求！Moralis 提供企业级 Web3 APIs 和其他工具，使 Web3 开发变得更加容易。此外，由于 Moralis 的许多集成特性，您可以组合 API、SDK 等。，跟 AWS 之类的其他平台！

因此，让 AWS Web3 做好准备的一个选项是 Moralis，我们将在下一节进一步阐述这一点，在下一节中，我们将探索最佳的 AWS Web3 Lambda 解决方案！

## 最佳 AWS Web3 Lambda 解决方案

如果你正在寻找开发 Web3 项目，并希望利用 AWS 服务，如 Lambda，最简单的方法是借助 Moralis，因为你可以快速集成 Moralis 的 NodeJS SDK 与 AWS Lambda！

![Moralis written in grey letters.](img/5f2dd21ee53255efc9a6d6e523d30102.png)

通过这样做，您可以通过这个 AWS 服务运行兼容 Web3 的 JavaScript 代码。此外，有多种方式可以集成 NodeJS SDK，两个突出的例子是创建和部署 Lambda 应用程序或开发 Lambda NodeJS Express API。尽管如此，通过集成 SDK，您可以利用 Lambda 的特性和优势，例如自动伸缩和成本降低，这在未来的开发工作中是有益的！

如果这听起来很令人兴奋，并且您想了解更多关于将 Moralis 的 NodeJS SDK 与 AWS Lambda 集成的信息，请继续阅读下一节，在那里我们将更详细地介绍 AWS Lambda Web3 教程！

## AWS Web3 教程

既然您对 AWS Lambda 以及为什么您可能希望在 Web3 开发中利用该服务有了更多的了解，本部分将涵盖一个全面的 AWS Lambda Web3 教程。此外，下面几节将向您展示如何将 Moralis 的 NodeJS SDK 与 Lambda 集成，从而允许您通过这个 AWS 服务运行 Web3 JavaScript 函数。为了说明这个过程，我们将开发和部署一个具有两个功能的 Lambda 应用程序:“ *getNativeBalance()* 和“ *getWalletNfts()* ”。

![Creating a Web3 Lambda Function - Learn How to Create an AWS Lambda Web3 Function](img/a837a415f36867b25b474ec345af71a0.png)

此外，由于 Moralis Lambda 集成的可访问性，您只需三个步骤就可以创建此应用程序并准备好 AWS Web3:

1.  涵盖先决条件
2.  设置新项目
3.  开发 Lambda 应用程序

所以，事不宜迟，让我们先了解必要的先决条件！

### 步骤 1:涵盖先决条件

要创建这个具有多种功能的 AWS Lambda 应用程序，您需要满足以下七个先决条件:

1.  [创建一个 Moralis 账户](https://admin.moralis.io/register)
2.  安装集成开发环境(IDE)
3.  建立一个 [AWS 账户](https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-creating.html)
4.  [安装 NodeJS](https://nodejs.org/en/)
5.  设置 [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html#getting-started-install-instructions)
6.  安装[无服务器框架](https://www.serverless.com/framework/docs/getting-started#installation)
7.  创建 IAM 用户

大多数先决条件都很简单，可以通过上面的链接解决。但是，在创建 IAM 用户时，您需要考虑一些事情。要创建用户，请登录 AWS 的管理控制台并打开 IAM 控制台。然后，您需要单击导航栏中的“用户”和“添加用户”。因此，它会将您带到以下页面:

![Set user details page on AWS account.](img/98e369214cf29c5ebbe4edbf44caf9e4.png)

到达上面的页面后，添加一个用户名，并确保包含两种凭据类型。进入第二部分时，选中“管理员访问”复选框:

![Set user permission page on AWS website.](img/bc6cb33e98a93e93f21977e436b7f2a8.png)

最后，完成剩下的步骤，直到到达最后一步，在最后一步中，您需要确保在一个。csv”文件:

![Success message displayed.](img/bed213daad0b4ca4ec59462ebb863afe.png)

### 步骤 2:设置新项目

在第二步中，我们将向您展示如何设置项目。但是，在这样做之前，您需要配置您的 AWS 凭证。因此，打开您的 IDE，启动一个新的终端，并运行以下命令:

```js
aws configure
```

一旦您运行上面的命令，它会提示您输入您的“ *AWS 秘密访问密钥*”。接下来，您必须添加您的“ *AWS 访问密钥 ID* ”。最后，还剩下两个提示，您只需点击“enter”即可。总而言之，它应该是这样的:

```js
AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE
AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
Default region name [None]: ENTER
Default output format [None]: ENTER
```

#### 项目设置

AWS 凭证配置完成后，我们现在将向您展示如何设置项目。首先，创建一个新文件夹。然后，用 IDE 打开它，并在新的终端中运行以下命令:

```js
serverless
```

这会触发你的终端，你必须做出几个决定。对于第一个问题，选择“开始”选项:

![AWS questions in your terminal.](img/6c90cea7994b6b32777ae31b2148ae33.png)

接下来，通过输入名称或立即点击“enter”来命名您的项目:

![Naming your project prompt.](img/482ece21d1adf0df28bf2350ecdbf9b7.png)

当您命名项目时，它将自动下载一个新的无服务器框架模板。完成后，终端会要求您登录。现在，您可以通过输入“ *n* 并点击“enter”来跳过这一步:

![Entering N into the terminal prompt.](img/420dac2841b21621391ccdead4435cdc.png)

在那里，您将被询问是否要部署这个项目。你现在可以通过再次输入“*n”*并点击“回车”来推迟:

![Inputting N and hitting enter in the prompt module.](img/ccbe4f0ef575615f7c5e4ebf44b43c1d.png)

因此，您现在应该在本地目录中有一个示例项目，如下所示:

![Local directory code structure for the AWS Lambda Web3 app.](img/28ff06aa3508bd8d68c45387906ead16.png)

接下来，添加一个名为“函数”的新文件夹:

![Functions folder.](img/159c062d558149be21de089e809e9e3d.png)

然后，您可以将“handler.js”文件移到该文件夹中:

![Handler.js folder inside VSC.](img/c0c5c79b4d0fdf379202084a449a9925.png)

最后，打开“serverless.yml”文件，用下面的代码片段替换其中的内容:

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

此外，请注意，您需要通过替换代码中的“ *replace_me* ”来添加您的 Moralis API 密钥。您可以通过登录 Moralis 并点击“Web3 APIs”选项卡来获取密钥:

![Web3 API page on Moralis' admin panel.](img/36925c693b8564b018d0862c5496cc0f.png)

### 步骤 3:开发 Lambda 应用程序

本节将向您展示如何添加应用程序的这两个功能。但是，在这样做之前，您需要安装 Moralis 依赖项。因此，将 *cd* 放到项目的根文件夹中，并在终端中运行下面的命令:

```js
npm install moralis
```

安装完依赖项后，我们将继续向您展示如何添加“ *getNativeBalance()* ”函数。该函数获取 Web3 钱包的本地余额。此外，我们还将添加“ *getWalletNfts()* ”函数，它对 Nfts 做同样的事情:

*   "*"–首先，将现有的“handler.js”文件重命名为“getNativeBalance.js”:*

*![Looking at the getNativeBalance.js file.](img/bfa1b9b1903626c043cd8169fdc2ee64.png)

从那里，打开“serverless.yml”并更改函数处理程序和名称:

![Adding handler function and name.](img/761aae5c50ee9e09bebae6a735dd512d.png)

最后，复制下面代码片段中的代码，替换“getNativeBalance.js”文件中的所有内容:

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

  // Format the native balance formatted in ether via the “.ether” getter
  const nativeBalanceEther = nativeBalance.result.balance.ether;

  return {
    result: nativeBalanceEther
  }
};
```

*   "***【getWalletNfts()***"–要添加这个函数，首先创建一个名为“getWalletNfts.js”的新文件:

![Creating the getWalletNfts.js file inside Visual Stuido Code.](img/9690a4c45b8603a1dbb644d43edad6e0.png)

然后，您可以打开“serverless.yml ”,将下面的代码输入到“*函数*”部分:

```js
getWalletNfts:
    handler: functions/getWalletNfts.handler
```

最后，打开“getWalletNfts.js”并添加以下代码片段中的代码:

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

至此，我们已经介绍了 Lambda 应用程序的两个功能和全部内容。从这里开始，剩下的工作就是测试应用程序并将其部署到 AWS。因此，我们将在最后一节向您展示如何做到这一点！

### 测试和部署应用程序

让我们从测试功能开始，以确保一切按预期运行。因此，在项目的根文件夹中创建一个名为“event.json”的新文件:

![Creating a file inside Visual Studio Code called event.json.](img/3cb7368e5ac2534d429ff824d5dd83eb.png)

从那里，你需要添加两个参数到这个文件中，“T0”地址“T1”和“T2”链“T3”:

```js
{
    "address": "0x99EXAMPLEADDRESS",
    "chain": "chain_id"
}
```

但是，请确保添加了要监视的钱包的地址和要查询的区块链的链 ID。添加参数后，您可以测试每个函数。为此，运行下面的命令，将“*FUNCTION _ NAME”*替换为函数的实际名称:

```js
serverless invoke -f “FUNCTION_NAME” --path event.json
```

如果您测试“*getNativeBalance()”*，如果一切正常，它应该会返回以下消息:

![Success message after running previous command.](img/334da0b2839ba6810e14dec4de322a00.png)

对结果满意后，您可以通过在终端中导航到应用程序的根文件夹并运行以下命令来部署它们:

```js
serverless deploy
```

当应用程序成功部署时，您的终端应该会显示以下输出:

![Success message stating that you have deployed your Web3 AWS Lambda application.](img/53ff7e445feef5a12b130358836ca10f.png)

本期 [AWS Lambda NodeJS](https://moralis.io/aws-lambda-nodejs-tutorial-how-to-integrate-a-nodejs-sdk-example/) 教程到此结束！您现在知道如何创建和[部署 AWS Lambda 函数](https://moralis.io/deploying-lambda-functions-how-to-deploy-aws-lambda-function-tutorial/)！然而，如果你在本教程中遇到了麻烦，请查看 AWS Lambda 的 [Web3 文档页面。希望该文档能够回答您的任何疑问！](https://docs.moralis.io/docs/using-aws-lambda)

## web 3 AWS Lambda–摘要

在本文中，您了解了如何将 Moralis 的 NodeJS SKD 与 AWS 集成。此外，您通过创建一个具有多种功能的 Lambda 应用程序实现了这一点。此外，多亏了 Moralis 的能力，您只需三个步骤就能准备好 AWS Web3:

1.  涵盖先决条件
2.  设置新项目
3.  开发 Lambda 应用程序

因此，如果您已经学习了这么多，您现在应该知道如何使用 AWS Lambda 运行 Web3 JavaScript 代码。因此，您现在可以利用这项服务的优势，例如降低成本，并且不必担心管理服务器！

如果你觉得这篇文章有帮助，可以考虑看看其他的 Moralis 指南。例如，您可能对我们的文章[感兴趣，探索终极的 ERC20 令牌 API](https://moralis.io/exploring-the-ultimate-erc20-token-api/) 。此外，请务必阅读我们的指南[如何使用多边形网钩](https://moralis.io/polygon-webhooks-how-to-use-webhooks-on-polygon/)！

然而，无论你从事什么样的 Web3 开发工作，都要马上和 Moralis 签约。你可以免费创建你的账户，只需要几秒钟！*