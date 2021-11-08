# STAKE Staking Token FAQ

## If I only need xDai coins for transactions, what is STAKE used for?

STAKE is a volatile token used as a staking token to protect the xDai chain. It enables delegated staking and community participation in xDai consensus. It is also used for [STAKE weighted proposal initiation and voting](../../for-users/governance/stake-weighted-voting/).

You do not need STAKE to use the xDai chain for regular transactions. You only need STAKE if you want to be a validator or delegator on the xDai chain or to participate in governance.

More on the [Dual Token Model](../../for-stakers/stake-token/stake-reward-mechanics/dual-token-model.md)

## How do I get STAKE on Ethereum?

* From another user on the Ethereum Mainnet (Wallet transfer, airdrop, payment)
* From a centralized exchange. STAKE is offered at [Huobi Global](https://www.huobi.com/en-us/exchange/),  [AscendEX (formerly BitMax)](https://bitmax.io/#/trade/usdt/stake) and others.
* From a decentralized exchange. Stake is offered at [UniSwap](https://uniswap.exchange/swap/0x0ae055097c6d159879521c384f1d2123d1f195e6) and others.&#x20;
* For a full list see [https://www.coingecko.com/en/coins/xdai-stake#markets](https://www.coingecko.com/en/coins/xdai-stake#markets)

## How do I get STAKE on xDai?

* Move STAKE from Ethereum to xDai with the [OmniBridge](https://omni.xdaichain.com/bridge).
* Acquire on xDai with [Honeyswap](../project-spotlights/1hive/honeyswap.md), [SushiSwap](https://app.sushi.com/swap) or other [DEXs on xDai](../project-spotlights/#defi).
* Bridging POA to WPOA and [performing a token swap](https://www.poa.network/for-users/about-poa-token/poa-merger-and-stake-swap).
* Purchase STAKE on xDai directly on [AscendEX](https://ascendex.com/en/global-digital-asset-platform).

{% hint style="warning" %}
Note: **STAKE deposits on xDai are only available on AscenDEX**. For Huobi, Gate and other exchanges you need to bridge STAKE to Ethereum first.** Do not send STAKE on xDai directly to those exchanges without bridging first**.  If you have additional questions, please ask in the [discord #support channel](https://discord.gg/mPJ9zkq).&#x20;
{% endhint %}

## What are the STAKE contract addresses?

Ethereum Mainnet\
[0x0Ae055097C6d159879521C384F1D2123D1f195e6](https://etherscan.io/token/0x0Ae055097C6d159879521C384F1D2123D1f195e6)

xDai Chain\
[0xb7D311E2Eb55F2f68a9440da38e7989210b9A05e](https://blockscout.com/xdai/mainnet/address/0xb7D311E2Eb55F2f68a9440da38e7989210b9A05e/transactions)

## I've got STAKE but can't find it in my wallet.

You may need to add a custom token:

Click on the [fox icon in BlockScout](https://blockscout.com/xdai/mainnet/tokens/0xb7D311E2Eb55F2f68a9440da38e7989210b9A05e/token-transfers) or the OmniBridge to quickly add to MetaMask, or add manually. [Instructions for adding with MetaMask](../../for-stakers/stake-token/get-stake/add-stake-to-metamask.md).

## I want to stake STAKE Now! Is it possible?

Yes!&#x20;

* Staking on Ethereum with [EasyStaking](https://easy-staking.xdaichain.com)&#x20;
* Staking on xDai with [Public POSDAO](../../for-stakers/staking-protocol/)

## STAKE with DeFi: How do I trade / farm / lend STAKE?

There are many DeFi applications on xDai. Here you can trade with STAKE, lend or borrow STAKE, or add STAKE to different liquidity pools. Below is a short list. For more on what is possible in the xDai ecosystem, see [xdai.world](https://www.xdai.world).

* [HoneyComb](https://1hive.io/#/farm)  | XCOMB
* [Sushiswap](https://app.sushi.com/farm)  | SUSHI/STAKE
* [Component Finance](https://xdai.component.finance/?tab=farmList\&token0=1\&token1=3)  |  CMP
* [Swapr](https://swapr.eth.link/#/pools) | DXD
* [Levinswap](https://farm.levinswap.org) | LEVIN
* [Baoswap](https://farms.baoswap.xyz) | BAO
* [Xion](https://xion.finance/farm) | XGT
* [Elk Finance](https://app.elk.finance) | ELK
* [Symmetric](https://xdai-pools.symmetric.exchange/#/explore)  | SYMM
* [Minerva Streaming Farm](https://farm.minerva.digital) | MIVA
* [Agave](https://agave.finance) Lending | CPT

## Is public staking available on xDai?

Yes, public staking is [now active on xDai](../news-and-information/project-updates/public-posdao-announcement.md).

## How much STAKE will I need for public staking?

The current projected minimum amounts needed to validate or delegate on the xDai chain.

* **Validators:** 2K STAKE (reduced from initial 20K amount)
* **Delegators:** 200 STAKE\* (Initial amount was 1K, reduced to 200 [through a community proposal](../../for-users/governance/stake-weighted-voting/))

## What is the STAKE Marketcap?

You can find information on the STAKE Marketcap and supply here: [https://www.coingecko.com/en/coins/xdai-stake](https://www.coingecko.com/en/coins/xdai-stake)

## How do I transfer STAKE from the Ethereum Mainnet to the xDai chain?

When public POSDAO staking on xDai begins, you will need to move your STAKE to xDai in order to use it there.

Video: [Moving STAKE between Ethereum and xDai with the OmniBridge](https://youtu.be/qbuBqur9lcE)

## Why is STAKE an ERC677?

ERC677 is very similar to an ERC20, but includes additional functionality. We use the `transferandCall` functionality to enable easier bridge conversions, moving STAKE from the Ethereum Mainnet to the xDai chain and back.

For more information see the EIP677 standard [https://github.com/ethereum/EIPs/issues/677](https://github.com/ethereum/EIPs/issues/677).

## What is multi-chain staking?

xDai is the first developed use-case for STAKE. However, it may be adopted by other chains in the future and used as a staking token for their consensus as well. POSDAO consensus is an algorithm we’ve developed that may be adopted by other chains, and those chains would have the opportunity to also incorporate a ready-made solution with STAKE to protect their chain.

## Can I move STAKE on the xDai Chain directly to the Huobi Exchange or AscendEx exchange?

### Huobi

To move to Huobi, you will first **need to have your STAKE on the Ethereum mainnet as an ERC20**. If you currently have STAKE on xDai, you should[** bridge it back to Ethereum with the OmniBridge**](https://omni.xdaichain.com/bridge?from=100\&to=1\&token=0xb7D311E2Eb55F2f68a9440da38e7989210b9A05e) before sending to the Huobi exchange.&#x20;

If you send STAKE on xDai directly to Huobi, the xDai team cannot help with this issue and you will need to contact Huobi directly.

_Note: The transfer operation between xDai and STAKE can be costly, _[_more on gas fees associated with bridging to Ethereum_](bridges-xdai-bridge-and-omnibridge.md#metamask-is-showing-very-high-fees-to-claim-a-transaction-on-ethereum-tokens-bridged-from-xdai-to-ethereum-is-this-estimate-accurate)_._

### AscendEx (formerly BitMax)

It is possible to send STAKE on xDai to the AscendEx exchange. Be sure to connect to the correct chain when sending STAKE to AscendEx. [More information](https://bitmax.io/en/help-center/articles/1500003245861)

{% hint style="warning" %}
Note: if you have STAKE on xDai on AscendEx and want to transfer it to Huobi, be sure to exchange it to STAKE on Ethereum before transferring between exchanges.
{% endhint %}
