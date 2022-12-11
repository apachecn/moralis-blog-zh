# 创建 Lambda 函数–了解如何创建 AWS Lambda 函数

> 原文：<https://moralis.io/creating-a-lambda-function-learn-how-to-create-an-aws-lambda-function/>

**您有兴趣学习如何创建 AWS Lambda 函数吗？如果是这样的话，你就很幸运了！本文提供了创建 Lambda 函数的全面教程。为了说明这个过程，我们将向您展示如何通过创建和部署一个具有多种功能的 Lambda 应用程序来集成 Moralis 的 NodeJS SDK 和 AWS。更重要的是，由于[Moralis 规范](https://moralis.io)的可访问性，你只需三步就能做到:**

1.  先决条件
2.  配置 AWS 和设置项目
3.  创建 Lambda 应用

通过遵循上面的步骤，您将学习如何创建、测试、部署和运行 AWS Lambda 函数。因此，您将能够直接通过 Lambda 运行 JavaScript 代码！如果您渴望立即进入教程，请随意跳到“ [Lambda 函数示例-如何创建 AWS Lambda 函数](https://docs.google.com/document/d/13ljDgQv6jQp4Fr6ihSlbnBJLSuC-YF858Kgl10hAhL4/edit?pli=1#heading=h.yd1w6gfnjpug)的演示”部分。您还可以在下面的 GitHub 资源库中找到该项目的完整代码:

[**Complete AWS Lambda GitHub Documentation**](https://github.com/MoralisWeb3/examples-aws-lambda-nodejs/tree/main/aws-node-project)

### 概观

亚马逊网络服务(AWS)是数百万客户使用的最完善、最全面的云计算平台之一。AWS 拥有一个广泛的网络相关服务生态系统，其中之一就是 AWS Lambda。AWS Lambda 是一个事件驱动的无服务器计算服务，允许您运行代码而无需担心底层基础设施。因此，要运行程序，您所需要做的就是以 AWS Lambda 函数的形式上传代码。然而，它们是什么，以及如何创建 AWS Lambda 函数？

如果你想知道上述问题的答案，请继续阅读，我们将探索 Lambda 函数的复杂性以及如何创建它们。通过阅读本文，您将很快学会如何通过 AWS Lambda 运行 JavaScript 代码！但是，假设您需要进一步熟悉这项服务的内容，并且正在寻找更详细的细分。在这种情况下，我们强烈建议在继续之前查看我们在 [AWS Lambda 上的指南以及它在](https://moralis.io/exploring-aws-lambda-and-what-it-is-used-for/)上的用途！

![Exploring AWS Lambda and What It is Used For article banner.](img/f07d776912fe6a232c86bc09e84dd0dc.png)

如果你已经知道如何创建 AWS Lambda 函数，但对 Web3 开发有进一步的兴趣，请在我们的 [Web3 博客](https://moralis.io/blog/)查看更多的 Moralis 内容。例如，学习创建[多边形 webhooks](https://moralis.io/polygon-webhooks-how-to-use-webhooks-on-polygon/) 或阅读 [Web3 for enterprise](https://moralis.io/web3-for-enterprise-business-applications-in-web3/) ！

然而，如果你想加入我们的教程，[注册 Moralis](https://admin.moralis.io/register) ，因为你需要一个帐户来创建一个 AWS Lambda 函数！

![Sign Up with Moralis and Start Creating Lambda Functions](img/776315699d4da3e5c69ca048fbcedf78.png)[**Sign Up with Moralis**](https://admin.moralis.io/login)

## 什么是 AWS Lambda 和 Lambda 函数？

AWS Lambda 是由 Amazon Web Services (AWS)提供的无服务器和事件驱动的计算服务。Lambda 允许您从任何后端服务或应用程序运行代码，而无需提供或管理服务器。因此，AWS Lambda 负责整个计算基础设施，您只需要提供想要执行的代码！

![AWS Lambda](img/e6d8907f6bde15f0304292a23c46ba19.png)

所有提供给 AWS Lambda 的代码都被组织成“Lambda 函数”。Lambda 函数包含配置信息，如资源要求、名称、入口点等。此外，因为 Lambda 具有事件驱动的架构，所以服务运行函数来响应事件。事件的一些突出例子可以是 HTTP 请求、DynamoDB 表更新、亚马逊 S3 中的对象修改等。

由于函数是基于事件触发的，Lambda 只在被请求时调用它们。这与“随用随付”的支付结构相结合，确保您只为自己消耗的计算资源付费。因此，您可以从 Lambda 获得几个优势，比如降低成本和更灵活的可伸缩性机会！

如果你想了解更多关于这个服务的细节，我们强烈推荐我们的文章[进一步详细解释 AWS Lambda 函数和架构](https://moralis.io/how-aws-lambda-works-functions-and-architecture-explained/)。

尽管如此，通过更好地理解这个服务需要什么，下一节将更深入地探讨创建 Lambda 函数的过程！

## 创建 Lambda 函数的过程

现在您对 AWS Lambda 已经比较熟悉了，本节提供了创建 Lambda 函数的“过程概述”。也就是说，有许多方法可以创建 AWS Lambda 函数，您有几种选择。事实上，您可以通过以下四种方式创作函数:

*   **AWS 命令行界面(CLI)**–创建 Lambda 函数的第一个选项是通过 AWS CLI。CLI 支持 macOS、Windows 和 Linux(有关如何使用 CLI 的更多信息，请参见“ *Lambda 函数示例……*”一节)。

![AWS CLI + AWS Lambda = Creating a Lambda Function](img/f65189d4aad05cd7ee8c106dfcbac767.png)

*   **AWS 管理控制台**–第二个选项是使用基于网络的 AWS 管理控制台工具。Lambda 控制台提供了一个代码编辑器，允许您快速测试和修改代码。

*   **cloud formation**–可以使用 AWS CloudFormation(一种基础设施即代码(IaC)服务)来创建定义功能的模板。

*   **AWS SDK**–您的最终选择是使用 AWS SDK。如果您想使用特定于语言的 API 直接创建 AWS Lambda 函数，这是一个不错的选择。

然而，这涵盖了创建 AWS Lambda 函数的四种方法。然而，下面的部分分解了一个 Lambda 函数的例子，以使它更容易理解。因此，如果您想了解如何创建 AWS Lambda 函数，请继续阅读！

## Lambda 函数示例–演示如何创建 AWS Lambda 函数

随着对 AWS Lambda 和服务功能的复杂性有了更深刻的理解，是时候深入本教程的中心部分了。因此，下面几节将说明如何创建 Lambda 函数。此外，为了演示这个过程，本教程将向您展示如何毫不费力地将 Moralis 的 NodeJS SDK 与 Lambda 集成。有可能以多种不同的方式做到这一点；然而，在本指南中，我们将开发和部署一个 Lambda 应用程序，该应用程序具有两个与区块链相关的功能:“ *getNativeBalance* ()”和“ *getWalletNfts* ()”。

![Moralis](img/dbb61e4b9fe988071e47adaa3151456f.png)

由于 Moralis 使 Web3 开发变得更加容易，您可以通过三个简单的步骤创建 AWS Lambda 函数:

1.  先决条件
2.  配置 AWS 和设置项目
3.  创建 Lambda 应用

通过遵循这些步骤，您将了解如何将 Moralis 的 NodeJS SDK 与 AWS 无缝集成，从而立即创建 AWS Lambda 函数。结果，您获得了使用 Lambda 运行 Web3 JavaScript 函数的能力，这很可能对未来的区块链开发工作有所帮助！

如果这听起来令人兴奋，请加入我们，在接下来的小节中学习如何创建 AWS Lambda 函数。首先，让我们从强制性的先决条件开始！

### 步骤 1:先决条件

要创建 AWS Lambda 函数，您需要满足以下七个先决条件:

1.  **建立一个 Moralis 账户**–首先，你需要一个 Moralis 账户。所以，如果你还没有，[马上和 Moralis 家](https://admin.moralis.io/register)签约吧！

2.  **创建 AWS 账户**——除了注册 Moralis，你还需要一个 [AWS 账户](https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-creating.html)来创建 AWS Lambda 功能。

3.  **安装一个 IDE**–要为应用程序编写代码，你需要安装一个 IDE。如果你不确定使用哪种 IDE，可以考虑 VSC，本教程中使用的环境。

4.  **安装 NodeJS**——手边有了 IDE，你还需要安装 NodeJS 运行时环境，你可以通过[点击这里](https://nodejs.org/en/)下载。

5.  **设置 AWS CLI**——接下来，安装并设置 [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html#getting-started-install-instructions) 。

6.  **安装无服务器框架**–[安装无服务器框架](https://www.serverless.com/framework/docs/getting-started#installation)，因为这是用来设置项目的。

7.  **创建 IAM 用户**–最后，您必须创建一个 IAM 用户。为此，请登录 AWS 并打开 IAM 控制台。从那里，点击导航栏中的“用户”和“添加用户”，进入以下页面:

![Set permissions page.](img/2d5eb5f10cbe86c0afb5306a5990b67f.png)

您需要添加一个用户名，并选中每种凭据类型的复选框。从这里开始，转到第二部分，将“AdministratorAccess”附加为一个策略:

![Add user page.](img/9b8f4800388eff32f603081b2758f2d8.png)

最后，介绍剩余的每个步骤，并根据您的偏好配置 IAM 用户。但是，当您到达最后一部分时，请注意，您需要将您的 AWS 凭证下载为。csv”文件:

![Success message after adding a user.](img/aaaa0049753e2e1e80f3c4d708723b68.png)

### 步骤 2:配置 AWS 和设置项目

既然您已经介绍了强制性的先决条件，那么这一步将围绕配置 AWS 和设置新项目展开。本节从前者开始，向您展示如何配置您的 AWS 凭证！

首先，你需要打开一个新的终端。如果你决定选择 VSC 作为你的 IDE，你可以点击顶部的“终端”，然后点击“新终端”:

![New terminal drop-down menu inside VSC.](img/b22d48d478fa734bea6565b61a58a50e.png)

终端启动后，继续运行以下命令:

```js
aws configure
```

这将自动提示您的终端，您需要添加您的“ *AWS 秘密访问密钥*和“ *AWS 访问密钥 ID* ”。最后，它应该是这样的:

```js
AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE
AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
Default region name [None]: ENTER
Default output format [None]: ENTER
```

这涵盖了 AWS 凭证配置。下一小节将向您展示如何用无服务器框架建立一个新项目！

#### 设置项目

要设置项目，首先创建一个新文件夹。从那里，用 IDE 打开该文件夹，并在终端中运行以下命令:

```js
serverless
```

当您运行“*无服务器*命令时，终端会为您提供一些选项。在这种情况下，您需要选择“Starter”选项:

![](img/0873f1e36afa426c6587af2c0b8338ed.png)

接下来，为项目添加一个名称，您可以通过立即按 enter 键来设置一个默认名称。但是，您也可以自己输入自定义名称:

![](img/8d15adf40d07117d5949201fb3047c02.png)

命名项目后，一个新的无服务器框架模板将自动下载到您的本地存储库中。下载完成后，终端会提示您登录。但是，对于本教程，这不是必需的，您可以通过输入“ *n* ”并按 enter 键来进行:

![](img/35a3f56b46c3b24330b71c2aad90144b.png)

终端将询问您是否想要部署这个项目。你可以暂时不去想。再次输入“ *n* ”继续，然后按回车键:

![](img/358be76ec41a703e2b78e1bf695c63ef.png)

一旦按下 enter 键，您应该会发现 IDE 中有一个类似于下面的示例项目:

![](img/582fff363ebdaef98e92afac3e759a30.png)

但是，在继续第三步之前，您需要对项目进行一些配置。首先，创建一个名为“函数”的新文件夹:

![](img/ed9aeff3bd231d0de8b8f10f1ba734f6.png)

从那里，将“handler.js”文件移动到“函数”中:

![](img/c5a3034e20ea4e83dd51fa9948100f92.png)

然后，您可以打开“serverless.yml”并为“handler.js”文件设定一个新位置:

![](img/757360ad9a1259274c6a69bd2dfbdffe.png)

最后，您必须添加您的 Moralis API 密钥，方法是将“serverless.yml”文件中的代码替换为以下内容:

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

此外，如果您检查上面的代码，您会很快注意到您需要用您的 Web3 API 密钥替换" *replace_me* "参数。您可以通过登录 Moralis 并导航至“Web3 APIs”选项卡找到密钥:

![](img/0e45df4a5bc490da24e8747bb4400580.png)

## 步骤 3:创建 Lambda 应用程序

现在，有了初始模板，是时候仔细看看本教程的核心部分，并向您展示如何创建 Lambda 函数了。首先，您需要安装 Moralis 依赖项。这样，打开一个新的终端，将“ *cd* ”放入项目的根文件夹中。在那里，通过运行以下命令安装 Moralis:

```js
npm install moralis
```

在下面的小节中，我们将介绍该应用的两个功能:“ *getNativeBalance* ()”和“ *getWalletNfts* ()”。第一个函数将获取 Web3 钱包的本地令牌余额；同时，第二个返回钱包的 NFTs。尽管如此，我们还是从“ *getNativeBalance()* ”开始吧。

#### " *getNativeBalance()* "函数

首先，将现有的“handler.js”文件的名称改为“getNativeBalance.js”:

![](img/5a711bee9fd74e8f3d2f091582f82250.png)

接下来，继续打开文件，将“*module . exports . hello”*替换为“ *module.exports.handler* ”:

![](img/354f2375c7ac7f849bde5ebfa92f2748.png)

此外，请确保更改“serverless.yml”中的函数名和处理程序:

![](img/8c664b16560dd660eed4a2bfdcef97a4.png)

从那里，您需要添加 Moralis 的" *getNativeBalance* "功能。为此，首先在文件顶部输入 Moralis 要求:

```js
const Moralis = require('moralis').default;
```

然后，您可以通过添加以下代码片段，用您的 API 密钥初始化 Moralis:

```js
const startMoralis = async () => {
  await Moralis.start({
    apiKey: process.env.MORALIS_API_KEY
  });
};

startMoralis();
```

最后，用下面的代码替换文件中的" *module.exports.handler"* "部分，该代码实现了获取 wallet 本机余额的 SDK 方法:

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

最终，这应该是“getNativeBalance.js”文件的最终状态:

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

这是它的第一个功能！让我们按照相同的步骤来实现下一节中的" *getWalletNfts* ()"函数！

#### " *getWalletNfts* ()"函数

要创建“ *getWalletNfts* ()”函数，您需要在“functions”文件夹中添加一个新文件，并将其命名为“getWalletNfts.js”:

![](img/53c34d2da5fdd233aaa758ee3c67e5a8.png)

从那里，打开文件并添加以下代码:

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

最后，打开“serverless.yml”文件，将下面的代码片段添加到文件的“ *functions* 部分:

```js
getWalletNfts:
    handler: functions/getWalletNfts.handler
```

![](img/98ec3d97fa2f8e883b4a5e6ae96fdea8.png)

恭喜你！您现在已经完成了创建 Lambda 函数的过程！然而，在继续之前，进行测试以确保一切正常是个好主意。因此，在项目的根文件夹中创建一个新的“event.json”文件:

![](img/30a00e0770a28a90bdd9d4645f5ba30f.png)

然后，您需要将“*地址*和“*链*参数添加到文件中，该文件看起来像这样(确保添加您想要查询信息的地址和正确的链 ID):

```js
{
    "address": "0x99EXAMPLEADDRESS",
    "chain": "chain_id"
}
```

接下来，您可以通过打开终端并运行下面的命令来测试这两个功能:

```js
serverless invoke -f FUNCTION_NAME --path event.json
```

但是，请注意，您必须用其中一个函数名替换“ *FUNCTION_NAME* ”。因此，如果您决定测试“ *getNativeBalance* ()”，如果该函数工作，终端应该返回以下消息:

![](img/ba96f0a9dd2663a15dbcf60a302745e9.png)

基本就是这样！接下来要做的就是将应用程序部署到 AWS Lambda，我们将在下面的附加步骤中介绍这一点！

### 额外步骤:部署您的 AWS Lambda 函数

既然已经成功创建了 Lambda 函数，剩下的工作就是将项目上传到 AWS Lambda。幸运的是，部署 AWS Lambda 函数相对简单。打开终端，确保您位于项目的根文件夹中，并运行以下命令:

```js
serverless deploy
```

如果应用程序成功部署，终端应该返回类似下面的消息:

![](img/fc3fa4b7ea785cdd6e6a0d81812fcb05.png)

这涵盖了整个 [AWS Lambda NodeJS](https://moralis.io/aws-lambda-nodejs-tutorial-how-to-integrate-a-nodejs-sdk-example/) 教程从头到尾！您现在知道了如何创建 AWS Lambda 函数并将其部署到服务中。因此，您现在可以通过 Lambda 运行 JavaScript 代码，并在所有未来的 Web3 开发工作中使用您新获得的技能！

如果你在教程中遇到了麻烦，请务必查看 Moralis 的 [AWS Lambda Web3 文档](https://docs.moralis.io/docs/using-aws-lambda#lambda-app-with-multiple-functions)。这些文档从头到尾涵盖了整个过程，并且很可能会回答您可能有的任何问题！

## 摘要–如何创建 AWS Lambda 函数

在本教程中，您学习了如何创建 AWS Lambda 函数，多亏了 Moralis，您只需三个步骤就能完成:

1.  先决条件
2.  配置 AWS 和设置项目
3.  创建 Lambda 应用

按照教程，您可以通过 AWS Lambda 轻松构建、测试、部署和运行 JavaScript 代码。因此，现在您已经熟悉了如何创建 AWS Lambda 函数，您可以将新获得的知识与额外的 Moralis 工具相结合来构建复杂的 Web3 项目！

如果这听起来很有趣，考虑一下其他的 Moralis 工具，比如各种各样的[web 3 API](https://moralis.io/web3-apis-exploring-the-top-5-blockchain-apis/)。其中，你会发现 [Auth API](https://moralis.io/authentication/) 。使用这个工具，您可以轻松地在您的区块链项目中实现多种身份验证机制。如果这听起来令人兴奋，请查看我们的文章，了解如何[使用 RainbowKit 添加登录功能](https://moralis.io/how-to-add-a-sign-in-with-rainbowkit-to-your-project-in-5-steps/)或[添加比特币基地钱包登录功能](https://moralis.io/how-to-add-coinbase-wallet-login-functionality/)！因此，如果你想获得更无缝的开发者体验，并使用像 Moralis 的 Web3 APIs 这样的工具，请立即注册 Moralis ！