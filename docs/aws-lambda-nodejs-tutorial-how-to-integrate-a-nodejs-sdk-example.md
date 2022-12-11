# AWS Lambda NodeJS 教程–如何集成 NodeJS SDK 示例

> 原文：<https://moralis.io/aws-lambda-nodejs-tutorial-how-to-integrate-a-nodejs-sdk-example/>

您是否正在寻找将 NodeJS SDK 与 AWS Lambda 集成的方法？如果是这样的话，你就在你应该在的地方！这篇 AWS Lambda NodeJS 教程提供了一个简单的例子，说明如何将 [Moralis](https://moralis.io) NodeJS SDK 与 Lambda 集成。这样，我们将向您展示如何通过三个步骤创建一个具有多种功能的 Lambda 应用程序:

1.  先决条件
2.  AWS 凭据配置和项目设置
3.  开发应用程序

如果您继续学习，您将学习如何使用 Lambda 构建、测试、部署和运行 Web3 JavaScript 函数！此外，如果您想直接进入教程，请跳到" *AWS Lambda NodeJS 教程-如何集成 NodeJS SDK 的示例*"部分！此外，您可以查看我们的 [AWS Lambda 文档](https://docs.moralis.io/docs/using-aws-lambda)页面了解更多信息！您也可以访问我们的 GitHub 知识库页面，查看下面的项目。

[**Complete GitHub AWS Lambda NodeJS Project Repo**](https://github.com/MoralisWeb3/examples-aws-lambda-nodejs/tree/main/aws-node-project)

### 概观

亚马逊网络服务(AWS)是目前最全面、最常用的云计算平台之一。该平台由大量 PaaS、SaaS 和 IaaS 产品组成，提供数百种服务来优化大型和小型组织的云体验。此外，在这个庞大的云计算解决方案生态系统中，我们发现了 AWS Lambda。Lambda 是一种无服务器、事件驱动的计算服务，用于执行代码，无需提供或管理服务器。更重要的是，由于 Lambda 是亚马逊最突出的服务之一，这就是本文的重点所在！

具体来说，本文将进一步研究如何通过 NodeJS 集成使用 AWS Lambda 运行 JavaScript 代码。这样，我们将通过创建一个具有多种功能的简单应用程序来说明如何将 Moralis 的 NodeJS SDK 与 Lambda 集成。因此，如果您继续学习，您将学会如何使用 AWS Lambda 构建、测试、部署和运行兼容 Web3 的 JavaScript 函数！

此外，如果您对 Web3 开发空间感兴趣，我们建议您查看更多的 Moralis 工具。例如，Moralis 提供了一系列企业级[web 3 API](https://moralis.io/web3-apis-exploring-the-top-5-blockchain-apis/)，让您能够充分利用区块链技术的力量！在这些工具中，你还可以找到 [Web3 Streams API](https://moralis.io/streams/) ，使你能够通过 [Web3 webhooks](https://moralis.io/web3-webhooks-the-ultimate-guide-to-blockchain-webhooks/) 将[的链上数据](https://moralis.io/on-chain-data-the-ultimate-guide-to-understanding-and-accessing-on-chain-data/)传输到你的应用程序的后端。要了解更多，请查看我们关于[以太坊网钩](https://moralis.io/ethereum-webhooks-what-they-are-and-how-to-use-webhooks-for-ethereum/)的文章。

然而，如果您想将 NodeJS SDK 与 Lambda 集成或构建 Web3 项目，请立即注册 Moralis 以获得更无缝的区块链开发体验！

## 探索 AWS Lambda

AWS(亚马逊网络服务)是最大的云计算平台之一，为全球数百万客户提供服务。AWS 生态系统由数百个服务组成，最重要的例子之一就是 AWS Lambda！

![AWS Lambda NodeJS Code Editor](img/ddab4fee93236c3dc82b91e65338ad1b.png)

AWS Lambda 是一个事件驱动的无服务器计算服务。有了 Lambda，您不需要担心管理或供应服务器，因为 Lambda 会为您处理繁重的工作。因此，有了 Lambda，你可以运行任何应用程序或后端服务的代码，你所需要的只是代码。

当使用 Lambda 时，您将代码组织成函数，Lambda 只在被请求时运行它们。此外，AWS Lambda 具有“按需付费”的计费结构，这意味着您只需为您消耗的计算时间付费。因此，当使用 AWS Lambda 时，您有极好的扩展机会，并且可以变得更具成本效益。

总而言之，AWS Lambda 是市场上最重要的计算服务之一，为全球数百万客户提供服务。此外，使用 Lambda 时，您可以访问完全由 AWS 管理的完整计算解决方案。因此，您无需关注后端基础架构，可以将更多时间用于为客户创造更高的价值！

## 什么是 aws lambda node.js

在进入本教程的中心部分之前，我们将简要地用这一部分来回答这个问题，“什么是 AWS Lambda NodeJS？”。然而，这个问题的答案相对简单，因为 AWS Lambda 的 NodeJS 集成使得使用 Lambda 执行 JavaScript 代码成为可能。

NodeJS 是一个开源的、跨平台的 JavaScript 运行时环境。更重要的是，AWS Lambda 为运行您的代码来处理事件的 NodeJS 提供了运行时。因此，您的代码运行在一个包含 AWS 的 JavaScript SDK 的环境中，同时还有来自访问管理角色的凭证和由您管理的 AWS 身份。

**支持的运行时间:**

![Supported runtimes for AWS Lambda NodeJS.](img/d0dcff6370b5e710b01447e0d471a8ce.png)

然而，简单地说，AWS Lambda NodeJS 使得使用服务运行 JavaScript 代码成为可能。现在，对 NodeJS 集成有了更好的理解，让我们更仔细地看看如何将这个运行时环境与 AWS Lambda 集成的例子！

## AWS Lambda NodeJS 教程–如何集成 NodeJS SDK 的示例

随着对 NodeJS 有了更深刻的理解，现在是时候通过一个示例项目向您展示如何将 Moralis 的 NodeJS SDK 与 AWS Lambda 集成来涵盖本教程的核心部分了。通过这样做，您将学习如何创建一个简单的 Lambda 应用程序，它有两个函数:“ *getNativeBalance* 和“ *getWalletNfts* ”。

![Moralis](img/18da7d69c6024f51ab1aa8c2a13ed26f.png)

此外，为了让这篇 AWS Lambda NodeJS 教程更容易理解和理解，本文将通过三个步骤向您展示如何创建这个应用程序:

1.  先决条件
2.  AWS 凭据配置和项目设置
3.  开发应用程序

如果你完成了上面的步骤，你将学会如何轻松地集成 Moralis 的 NodeJS SDK 和 AWS Lambda。通过跟随，您将能够通过 Lambda 运行兼容 Web3 的功能，而无需管理或提供服务器！

然而，让我们直接进入 AWS Lambda NodeJS 教程的第一步，并涵盖必要的先决条件！

### 步骤 1:先决条件

在向您展示如何创建应用程序之前，您必须了解必要的先决条件，总共有七个先决条件:

*   **创建一个 Moralis 账户**——如果你还没有，你需要注册一个。创建一个帐户是免费的，只需要几秒钟！

*   **安装 IDE**–接下来，您必须安装并设置您选择的 IDE。对于本教程，我们使用 VSC，但你可以自由选择你最舒适的环境。但是，请注意，如果您选择另一个选项，该过程可能偶尔会有所不同。

*   **安装 NodeJS**–对于本教程，您需要安装 NodeJS 运行时环境。你可以使用以下链接下载 NodeJS:【https://nodejs.org/en/[。](https://nodejs.org/en/)

*   **创建一个 AWS 账户**——如果您还没有，请访问 AWS 的[官方网站](https://aws.amazon.com)并立即创建一个账户。

*   **AWS CLI(命令行界面)**–接下来，安装 AWS CLI。点击[这里](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html#getting-started-install-instructions)，你会找到一份全面的设置指南。

*   **无服务器框架**——你还需要安装无服务器框架，你可以在这里[找到安装的教程](https://www.serverless.com/framework/docs/getting-started#installation)。

*   **创建 IAM 用户**–最后，您需要创建一个 IAM 用户，这可以通过登录您的 AWS 帐户并打开 IAM 控制台来完成。从那里，点击导航面板中的“用户”和“添加用户”。这会将您带到以下页面，您需要在其中添加用户名并选择两种 AWS 凭据类型:

![Add user details page to access key.](img/1f66541ff00b765a56b831d2da8f7f28.png)

接下来，选中“管理员访问”框:

![Add user permission page.](img/602e41b06e76a79105f7061aeadd0ee1.png)

按照您的偏好完成每个步骤来配置帐户。但是，在第五步中，下载您的 AWS 凭证。csv”格式:

![Download button for csv format.](img/b6e18dfdb9c2e379d63fae8468022812.png)

这包括了先决条件！让我们直接进入 AWS Lambda NodeJS 教程的第二步，向您展示如何设置项目！

### 步骤 2: AWS 凭证配置和项目设置

现在，涵盖了所有的先决条件，AWS Lambda NodeJS 教程的第二步将向您展示如何配置您的 AWS 凭证和设置项目。首先，我们将从前者开始，向您展示如何配置您的 AWS 凭证。因此，您可以从这里开始，打开一个新的终端。如果您使用的是 VSC，您可以点击 IDE 顶部的“终端”选项卡，然后点击“新建终端”:

![Creating a new terminal inside VSC.](img/b4a5c7f2179fb25c0bda5fc78beeb29e.png)

由于您在第一步中安装了 AWS CLI，因此从这里开始，通过运行以下命令来配置凭据:

```js
aws configure
```

运行该命令会提示您的终端，您必须添加您的“ *AWS 访问密钥 ID* 和“ *AWS 秘密访问密钥*”。它应该是这样的:

```js
AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE
AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
Default region name [None]: ENTER
Default output format [None]: ENTER
```

#### 项目设置

现在您已经完成了 AWS 凭证的配置，这一小节将介绍应用程序本身的设置过程。因此，首先，创建一个新文件夹并用 IDE 打开它。从那里，再次打开一个新的终端并运行下面的命令:

```js
serverless
```

运行上面的命令时，您会看到几个选项，在本例中，选择“Starter”:

![Terminal options including AWS - Node.js - starter.](img/4a487e3b5fe440402dda98b279c2b2f5.png)

选择此选项后，系统会要求您命名项目。您可以单击 enter 设置默认名称，也可以自己输入一个名称:

![Terminal asking if user wants to create a new AWS NodeJS project or call a project.](img/a3cbdb4199a0cef9875d5027d99cb5b2.png)

一旦命名了项目，就会下载一个无服务器框架模板。完成后，您的终端将提示您登录。但是，对于这个项目来说，这不是必须的。因此，输入“ *n* ”并按回车键继续:

![User asked by terminal if user wants to create a new Serverless project.](img/4c227a8665b29b7f585c2c3e7c04b666.png)

最后，输入“ *n* ”并再次按 enter 键，因为您现在还不想部署项目:

![User inputting "n" in the terminal.](img/6fb912d485688bd40fc5e934c9ef63ef.png)

因此，您现在应该有一个类似于下面的示例项目:

![AWS Lambda NodeJS Example structure code inside Visual Studio Code.](img/54ac2f6332e82e8f61ddfa84601de3c7.png)

接下来，创建一个新的“函数”文件夹:

![Creating a functions folder inside VSC.](img/fb17211b9d1e8cea316088499d95de97.png)

从那里，将“handler.js”文件移动到此文件夹中:

![Showing handler.js file.](img/f35189f8c7b321f097ae851adc6b81d5.png)

然后，您可以打开“serverless.yml”文件，并为“handler.js”设置一个新位置:

![Showing the serverless.yml file and adding a functions handler location.](img/b4d1ef0fc6158841ecb332c5a001bb01.png)

此外，添加您的 Moralis API 键作为环境变量。为此，请用以下代码片段替换“serverless.yml”中的代码:

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

如果您检查上面的代码，您会注意到您需要设置" *MORALIS_API_KEY* "变量来等于您的 API 密钥。要获得密钥，请登录 Moralis，单击左侧的“Web3 APIs”选项卡，复制密钥，并将其插入代码:

![Moralis Web3 API key page.](img/13897f76680b00902d2045ba60a65be4.png)

这就是初始项目设置！让我们继续这个 AWS Lambda JS 教程的核心开发部分！

### 第三步:开发应用程序

首先，打开终端并导航到项目的根文件夹。您可以通过运行" *cd 'FOLDER_NAME'* "来完成此操作。在那里，您可以通过运行以下命令来安装 Moralis:

```js
npm install moralis
```

在接下来的两个小节中，您将学习如何创建两个函数，“ *getNativeBalance* 和“ *getWalletNfts* ”。第一个返回指定钱包的本机令牌余额，第二个返回钱包的 NFTs。然而，让我们从前者开始。

#### *getNativeBalance*函数

首先，让我们使用已经存在的“handler.js”文件，并将其重命名为“getNativeBalance.js”:

![Renaming file to getNativeBalance.js.](img/314114fb61ad76e8aa47f2e3baa3470f.png)

在那里，打开文件，将“ *module.exports.hello* ”替换为“ *module.exports.handler* ”:

![Replacing ”module.exports.hello” with ”module.exports.handler”.](img/08c98aff1e63df8a380e2b7fe85b23b6.png)

然后，您可以通过打开“serverless.yml”文件并更改函数的名称和处理程序来继续。它现在看起来应该类似于这样:

```js
service: aws-node-project

frameworkVersion: '3'

provider:
  name: aws
  runtime: nodejs14.x
  environment:
    MORALIS_API_KEY: 'replace_me'

functions:
  getNativeBalance:
    handler: functions/getNativeBalance.handler
```

接下来，是时候通过添加 Moralis 的“getNativeBalance”功能来定制函数了。为此，导航回“getNativeBalance.js ”,开始添加 Moralis 要求:

```js
const Moralis = require('moralis').default;
```

然后，您可以添加下面的代码片段，使用指定为环境变量的 Web3 API 键来初始化 Moralis:

```js
const startMoralis = async () => {
  await Moralis.start({
    apiKey: process.env.MORALIS_API_KEY
  });
};

startMoralis();
```

最后，用下面的代码替换整个" *module.exports.handler* "来实现所需的 SDK 方法:

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

最终，您的“getNativeBalance.js”文件应该看起来像这样:

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

这涵盖了初始的" *getNativeBalance* "函数。让我们按照相同的过程来实现下面小节中的“ *getWalletNfts* ”函数！

#### *getWalletNfts*函数

对于此功能，您需要在“functions”文件夹中创建一个新文件。在这种情况下，我们将文件夹称为“getWalletNfts.js”:

![Creating a folder called getWalletNfts.js inside VSC.](img/05d6a8bd1237b83fa4120b09dbb17151.png)

从那里，打开“serverless.yml”文件，并在“函数”部分添加以下代码:

```js
getWalletNfts:
    handler: functions/getWalletNfts.handler
```

![Showing the handler function.](img/8be990d64f6886f670927db30c9cf936.png)

最后，通过将以下代码添加到“getWalletNfts.js”文件来完成“ *getWalletNfts* ”函数:

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

这个 AWS Lambda NodeJS 教程到此为止！如果您已经了解了这么多，那么您现在应该知道如何使用 Moralis 将 NodeJS SDK 与 Lambda 集成在一起了！

但是，您应该进行本地测试，以确保一切正常。更重要的是，一旦您对应用程序感到满意，您应该将它部署到 Lambda。因此，我们将在本教程的最后部分向您展示这些过程是如何工作的！

## 结束 AWS Lambda NodeJS 教程——测试和部署

首先，您想要运行一个本地测试来确保您的 Lambda 应用程序按照预期的方式工作。因此，我们将在本节的开始部分向您展示如何在本地测试 Lambda 函数！

让我们首先在项目的根文件夹中创建一个名为“event.json”的新文件:

![Creating a new file called ”event.json” in the project’s root folder.](img/966578fa67557df302c2ddc52261b83a.png)

然后可以添加一个“*地址*和“*链*作为参数。它可能看起来像这样:

```js
{
    "address": "0x99EXAMPLEADDRESS",
    "chain": "chain_id"
}
```

然而，正如您从代码片段中看到的，您需要添加您想要余额的钱包地址和您想要查询的链的 ID。从那里，您可以测试这些函数，例如，在终端中输入以下内容来测试" *getNativeBalance* "函数:

```js
serverless invoke -f getNativeBalance --path event.json
```

如果测试成功，它应该会返回类似下面的消息:

![Message returned showing project's folder.](img/7d643110921071fd95a97dc2aca34912.png)

既然您已经确保一切正常，剩下的工作就是将您的项目部署到 AWS。为此，请确保您位于项目的根文件夹中，并在终端中运行以下命令:

```js
serverless deploy
```

如果部署成功，您应该会收到类似以下内容的消息:

![Message stating service deployed to stack.](img/20cbc49202d3c069fe7601356135a1a5.png)

恭喜你；现在，您已经成功构建并部署了一个具有多种功能的 Lambda 应用程序！

如果你在任何时候遇到任何问题，请查看本教程的 AWS Lambda 文档。如果还有任何问题，您也可以加入 Moralis Discord 社区，从我们的社区工程师那里获得帮助！

## 总结–AWS Lambda NodeJS 教程

本文提供了一个如何将 NodeJS SDK 与 AWS Lambda 集成的示例。为了演示这个过程，您学习了如何通过创建一个简单的应用程序来集成 Moralis 的 NodeJS SDK 和 Lambda，这个应用程序只需要三个步骤就可以实现多种功能:

1.  先决条件
2.  AWS 凭据配置和项目设置
3.  开发应用程序

如果您一直关注这个 AWS Lambda NodeJS 示例，那么您现在应该知道如何使用 Lambda 和 Moralis 的 NodeJS SDK 创建、测试、部署和运行 Web3 函数！因此，您现在可以使用相同的原则在将来通过 Lambda 运行 JavaScript 函数，这将证明对您的 Web3 开发工作很有帮助！

如果你觉得这篇文章有帮助，你可以在 Moralis 的 [Web3 博客](https://moralis.io/blog/)上找到更多的内容。例如，如果您想将 [Web3 基础设施](https://moralis.io/web3-infrastructure-exploring-the-best-solution-for-web3-development/)集成到您的企业中，请查看我们关于 [AWS Lambda 及其用途](https://moralis.io/exploring-aws-lambda-and-what-it-is-used-for/)或 [Web3 for business](https://moralis.io/web3-for-business-how-and-why-you-can-integrate-web3-into-your-enterprise/) 的文章！

更重要的是，你还应该知道，Moralis 是 Web2 和 Web3 开发之间的桥梁！因此，[立即与 Moralis](https://admin.moralis.io/register) 签约，充分利用区块链技术的力量，获得更加无缝的开发人员体验！