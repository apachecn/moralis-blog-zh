# ERC 1155–探索 ERC-1155 令牌标准

> 原文：<https://moralis.io/erc1155-exploring-the-erc-1155-token-standard/>

**ERC1155，简称“以太坊征求意见稿 1155”，是一种令牌标准，主要用于** [**NFTs**](https://moralis.io/non-fungible-tokens-explained-what-are-nfts/) **(不可替代令牌)。随着 NFT 越来越受欢迎，越来越多的艺术家想要创建 NFT，有一个像 ERC1155 这样的令牌标准来规范这些令牌是有益的。此外，对于那些有志于开始使用** [**区块链开发**](https://moralis.io/best-languages-for-blockchain-development-full-tutorial/) **和想要** [**创建 NFT**](https://moralis.io/how-to-create-nfts-and-upload-to-opensea/)**的人来说，了解以太坊的领先标准之一——ERC-1155 令牌标准是他们开发之旅中必不可少的一部分。因此，请跟随我们探索 ERC-1155 令牌标准，了解什么是 ERC1155，并发现各种令牌标准之间的主要差异。因此，您将准备好开始使用 ERC-1155 令牌标准创建 ERC1155 NFTs 的旅程。**

在深入研究 [NFT 令牌开发](https://moralis.io/nft-token-development-the-ultimate-guide/)之前，了解众所周知的 NFT 标准以巩固您的基础是明智的。早期的 NFT 爱好者使用 ERC-721，因为它是以太坊下第一个普及的不可替换令牌标准。然而，以太坊的社区找到了改进 ERC-721 并扩大其功能的方法。ERC1155 已成为最新的 NFT 标准，有望实现有趣的改进。在本文中，您将看到为什么今天的开发人员青睐 ERC-1155 标准。

您会发现，ERC1155 令牌标准借鉴了以前的可替代和不可替代令牌标准，如 ERC-20 和 ERC-721。然而，它提供了几个新的优势，包括其智能合约同时代表多个令牌的能力。此外，与旧标准相比，某些批处理操作使它更有效。开发人员和 NFT 创建者将会喜欢 ERC1155 的更新如何使交易更容易管理。它们还降低了交易成本，因为它们降低了以太坊的汽油费。此外，ERC1155 汇集了可替换、不可替换和半可替换的令牌属性，从而提供了更大的灵活性。

## ERC-1155 简明介绍

要获得 ERC-1155 的简明视频解释，请观看来自 [Moralis 的 YouTube 频道](https://www.youtube.com/channel/UCgWS9Q3P5AxCWyQLT2kQhBw)的这段视频:

https://www.youtube.com/watch?v=XNWd8Nl3rhA

## 什么是 ERC1155？

ERC1155 不仅仅是一种 NFT 令牌标准。它为多令牌管理和事务奠定了基础。使用 ERC1155，单个部署的合同可以包括不可替代、可替代和半可替代令牌的各种组合。

ERC1155 令牌标准由金恩团队首创，它借鉴了 ERC20 和 [ERC721 令牌](https://moralis.io/erc-721-token-standard-how-to-transfer-erc721-tokens/)等令牌标准。它还引入了自己的改进。以前，在 ERC-20 或 ERC-721 下，您必须为每个可替换或不可替换的令牌部署单独的合同。这导致以太坊的区块链充满了冗余的字节码。此外，通过将每个合同分成单独的地址，旧的标准限制了某些功能。

![](img/b1396feb12b0c9ca221645489af931db.png)

为了让 NFT 和更广泛的令牌生态系统成长并扩展到其他应用程序中，社区显然需要创建一个新的标准。如果游戏平台和其他类型的基于令牌的 dApps(去中心化应用程序)想要将 NFTs 纳入其中，他们必须找到一种新的方法来最小化交易量和合同的低效率。于是，ERC1155 诞生了。

使用 ERC1155，现在可以在单个实例中转移不同类型的令牌，从而节省交易成本。此外，还可以在 ERC1155 标准的基础上，以原子互换和多个令牌的 escrows 形式创建交易。由于 ERC1155 消除了这一多余步骤，系统不再需要单独批准代币合同。

## 可替代、不可替代和半可替代

为了进一步研究 ERC1155，让我们简要回顾一下可替换、不可替换和半可替换令牌的定义及其相应的令牌标准。

### 可替代代币

可替代代币采用货币的属性，可以像使用法币一样使用。因此，可替换令牌不是唯一的；也就是说，你可以用一个代币换另一个同类的代币。而且，没有编程的区别。就像一美元是一美元一样，一个可替代的硬币或代币可以与另一个互换，对价值的理解是一样的。可替代代币主要用作货币、费用或某种支付的单位。

![](img/7c6595f45c3da9de6051ea3892ea9601.png)

#### 可替代性和可分性

当某物是可替代的，它也是可分割的。例如，一个比特币(BTC)可以被分割成小至 0.00000001 BTC 的分数。换句话说，BTC 被编程为可被除尽到小数点后八位，最小的分数称为“Satoshi”。因此，虽然比特币在过去几年中价值飙升，但它仍然可以用于小额支付。

![](img/13be231091e2592dbd03d94a9e28fed9.png)

此外，重要的是要记住，使用加密货币或加密令牌，部门或更小的单位可以通过智能合同事先设置。可替换的加密货币或代币的其他示例包括 Dogecoin、Litecoin、Monero、以太坊 ERC-20 代币和 [BEP20](https://moralis.io/what-is-bep20-full-binance-smart-chain-token-guide/) (币安智能链)代币。然而，除了上面提到的，还有很多其他的。

#### ERC-20 令牌标准

ERC-20 是以太坊上的一个标准，用于编码一类可替换的令牌。

可替换令牌的使用案例包括:

*   数字货币或交易媒介，如稳定币。
*   被编程为同类股票和债券的证券代币或加密资产。

### 不可替换令牌(NFT)

![](img/e9efd60cc985b52a756c20e6cb189d7e.png)

如前所述，ERC1155 是创建 NFT 的标准。但是[首先什么是 NFT](https://moralis.io/non-fungible-tokens-explained-what-are-nfts/)？NFT 与可替换令牌相反。它们是具有唯一属性的令牌，因此不能相互互换。每个令牌代表唯一、独立且不同的价值、属性或资产。

如果你已经注意到 NFT 最近在涨价，那是因为它们代表了一种独特的价值形式。此外，它们还代表了排他性，这在数字艺术领域是一个很大的用例。此外，虽然数字创作可能被认为是丰富的，但 NFT 为它们添加了信息和出处，将它们转化为数字上独一无二的东西。

这怎么可能？通过智能合约的强大功能，您可以创建内置签名，作为所有权的证明和身份验证的方法。此外，智能合同持有 NFTs 元数据和到艺术品或独特创作本身的链接。这些都包含在代码中，这些代码用 [Solidity](https://moralis.io/solidity-explained-what-is-solidity/) 编写，通常在以太坊的区块链上，尽管币安智能链(BSC)、Polygon(以前的 Matic)等平台正在迎头赶上。随着 NFT 以太坊 dApps 的大规模增长，这些另类区块链在 NFT 平台建造者中越来越受欢迎。

当今不断发展的 Web3 生态系统为您提供了许多启动 NFT 令牌基础架构的方法。此外，Moralis 允许您在各种平台上构建 NFT。此外，作为一个终极的 Web3 开发平台，Moralis 提供了一整套支持，包括 [Moralis Speedy Nodes](https://moralis.io/speedy-nodes/) 、 [Moralis NFT API](https://moralis.io/announcing-the-moralis-nft-api/) 等等，这样你就可以在创纪录的时间内[创建 NFT](https://moralis.io/how-to-create-nfts-and-upload-to-opensea/)或构建 [NFT 游戏](https://moralis.io/what-are-nft-games-and-how-to-make-nft-games/)。

### ERC 队以 721 比 1155 胜 ERC 队

最流行的非功能性测试标准是 ERC-721 和 ERC-1155。

作为 NFTs 中第一个广泛使用的令牌标准，ERC-721 令牌标准是最容易识别的 NFT 令牌标准。此外，该标准允许应用程序使用 Moralis 的[以太坊 API](https://moralis.io/ethereum-api-develop-ethereum-dapps-with-moralis/?utm_source=blog&utm_medium=post&utm_campaign=Want%2520the%2520Latest%2520in%2520%253Cspan%253EBlockchain%2520Development%253F%253C%252Fspan%253E) 进行 NFTs。

从技术上讲，ERC-721 定义了智能合约必须实现的最小接口。这个最小接口允许拥有、交易和管理唯一的令牌。ERC-721 不需要连接到令牌的元数据的标准。此外，它不限制添加补充最低要求的功能。

ERC-721 最初是达帕实验室的首席技术官迪特·雪莉(Dieter Shirley)的 EIP(以太坊改进提案)草案，后来成为游戏 CryptoKitties 的基础。公认的 ERC-721 标准的作者是迪特尔·雪莉、威廉·恩特里肯、雅各布·埃文斯和纳斯塔西亚·萨克斯。

![](img/baa76b11aa76a06dde68d8b9983887b7.png)

重要的是要记住，NFTs 智能合约的一个关键特性是它们不包含艺术品、图像或文件本身，而只包含它们的链接或 URIs 及其元数据。此类令牌引用此类文件和信息的链外资源，因此区块链本身不负责托管此类数据。

ERC-1155 在某些方面是 ERC-721 的改进，因为它的代码不仅适用于不可替换令牌(NFT ),也适用于半可替换令牌，我们将在下一节看到。

### 带有 ERC1155 的半可替换令牌

ERC1155 是创建半可替换令牌的新方法。然而，什么是半可替换令牌呢？这些是新类型的令牌，它们合并了之前的令牌标准的不同属性。就当是两全其美吧。让我们来做一个有用的类比:你可以创建一张商店优惠券——因此是一个可替代的代币——它在你兑现之前一直保持价值。兑现优惠券后，它的美元价值为零，您不能将它作为常规的可替代代币进行交易。因此，具有改变的属性的兑现的优惠券变得唯一，具有关于兑现的项目、客户、价格等的信息。因此，它变得不可替代。然而，诸如 ERC1155 之类的半可替换令牌标准能够表示这两种属性。

根据金恩的博客，ERC1155 是一种定义令牌的新方法。多个项目可以存储在一个合同中，使用最少的数据量来区分它们。此外，金恩写道，“契约状态包含每个令牌 ID 的配置数据以及管理集合的所有行为。”

因此，这个新的令牌标准允许您创建实用令牌(例如 BNB)和 NFT(例如 CryptoPunks 或 CryptoKitties)。它的优化也使交易更加高效和安全。与 ERC-721 不同，ERC1155 将交易捆绑在一起，从而降低了汽油费。此外，它能够同时创建高效的 NFT 和可替换令牌，这表明它是从 ERC-20 和 ERC-721 发展而来的。

## ERC 1155 合同

使用 ERC1155 合约，现在可以同时转让多种类型的令牌。您可以在 ERC1155 标准的基础上构建多种功能，如各种令牌的原子互换和 escrows(在交易中很有用)。这样，您就不需要像 ERC-721 那样单独授权单个令牌合约。此外，如前所述，您可以在一个 ERC1155 契约中组合多个 NFT 和可替换令牌类型。

在这张由金恩创建的简单图表中，您可以看到这一新标准如何简化任意数量令牌的令牌交换(例如代表独特物品的不同种类的 NFT)，这是一个在游戏中很有价值的用例:

![](img/51813f9145641319bd915b278b6df8e2.png)

**多个令牌的原子交换**

正如你所看到的，整批交易通过两个简单的步骤获得批准和交易，这证明了 ERC1155 合同可以为你节省以太坊燃气费。

ERC1155 合同还允许您一次向多个收件人发送多个项目。这种类型的 ERC1155 交易在下图中很容易理解，该图也是由金恩创建的:

![](img/11002fb512ed386611e9cefeb8dcd34e.png)

**在一次转账中将多个代币转移到不同的账户**

如您所见，将不同类型的项目转移给多个用户只需要一份合同和一次交易。ERC1155 轻便、高效，并且消除了冗余。此外，从这个例子中，您现在理解了 ERC1155 是不可替换的。

## ERC1155 合同样本

下面是一个游戏中令牌化物品的简单契约示例:

```js
// contracts/GameItems.sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.6.0;

import "@openzeppelin/contracts/token/ERC1155/ERC1155.sol";

contract GameItems is ERC1155 {
    uint256 public constant COPPER = 0;
    uint256 public constant CRYSTAL = 1;
    uint256 public constant ELDER_SWORD = 2;
    uint256 public constant KNIFE = 3;
    uint256 public constant WAND = 4;

    constructor() public ERC1155("https://game.example/api/item/{id}.json") {
        _mint(msg.sender, COPPER, 10**18, "");
        _mint(msg.sender, CRYSTAL, 10**27, "");
        _mint(msg.sender, ELDER_SWORD, 1, "");
        _mint(msg.sender, KNIFE, 10**9, "");
        _mint(msg.sender, WAND, 10**9, "");
    }
}
```

这将初始化一个 ERC1155 协定。此外，本合同中的游戏物品是可替换的和不可替换的。在这种情况下，铜是可替代的，而“长老剑”是不可替代的。

在“GameItems”下，还可以观察到每个物品都对应一个数字。这仅仅意味着每个整数，如“铜”或“水晶”，实际上只是“0”、“1”等的别名。引擎盖下，这些名字简单读作“0”、“1”、“2”、“3”、“4”。

在 ERC1155 合同的构造器部分，您会发现几个“mint 调用”。mint 调用创建新的令牌类型。在这里，作为游戏币，铜以“10 <sup>18</sup> 的数量铸造，水晶以“10 <sup>27</sup> 的数量铸造。长老剑被铸造成单个数量或“1”，这表明该物品是 NFT。它是独一无二的，因为它只有一个。虽然刀和魔杖的数量很大，但它们也可能是 NFT，因为它们代表彼此独立的单独物品，不是货币。更重要的是，您可以在同一个合同中不断添加项目，而不需要创建新的合同。

### ERC 1155–黄金标准

大型 NFT 市场使用各种版本的智能合约。ERC1155 允许用户创建新项目，而无需在这些市场上部署新合同。因此，当你在以太坊上[建造 dApps 时，ERC1155 呈现出一种优势。此外，它在 NFT 市场构建中更有意义，使其成为今天创建的 NFT 平台的新的高级标准。除了 Moralis，它提供了新的强大的方法来优化您的 NFT dapp 和平台，ERC1155 可以将您的区块链开发游戏带到一个新的水平。](https://moralis.io/how-to-build-dapps-on-ethereum/)

有了这些优势，就没有什么理由回到旧的、更麻烦的标准上去；然而，它仍然是简单项目中的一个选项，也是任何新手[区块链开发者](https://moralis.io/how-to-become-a-blockchain-developer/)或 NFT 程序员有用的学习工具。

## ERC 1155–探索 ERC-1155 令牌标准–摘要

凭借其独特的优势，ERC1155 现在被视为 NFT 平台开发的“黄金标准”。它允许您将多种令牌类型结合在一起，并在单个部署的契约和事务中容纳多个用户或接收者。这确实是对过去 NFT 标准的改进，有许多自己的新特点，比如创造了半可替代的代币。

结合 Moralis 强大的 [Web3](https://moralis.io/the-ultimate-guide-to-web3-what-is-web3/) 开发工具，使您可以快速建立区块链节点，将后端工作转移到其基础设施，并快速构建 dApps，ERC1155 可以帮助您创建下一代成功的 [NFT 游戏](https://moralis.io/what-are-nft-games-and-how-to-make-nft-games/)，市场和平台！

![](img/be284859b5e7d4df274ed35a8889f185.png)

[立即注册您的免费 Moralis 帐户](https://admin.moralis.io/register?utm_source=blog&utm_medium=post&utm_campaign=Want%2520the%2520Latest%2520in%2520%253Cspan%253EBlockchain%2520Development%253F%253C%252Fspan%253E),借助 Moralis 的出色支持和无与伦比的 Web3 基础设施，开始您激动人心的新 ERC1155 开发之旅！