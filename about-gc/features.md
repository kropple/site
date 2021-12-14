---
description: The following features make GC a unique and secure scalability solution.
---

# Features

## xDai Stable Transaction Coin

A stable coin means peace of mind. Predictable currencies allow buyers and sellers to exchange value without the risks of volatility. In the Gnosis Chain implementation, transactions are conducted using xDai, a stable coin with 1:1 value ratio to Dai. Because transactions occur on a bridged chain, they are extremely fast and inexpensive. In addition, transactions and fees are paid with a single coin.

## STAKE Multi-Chain Staking & GovernanceToken

{% hint style="warning" %}
STAKE is still protecting the current implementation, however it is being phased out in favor of GNO protecting the Gnosis Beacon Chain. [Learn how to swap STAKE for GNO here](../for-stakers/stake-token/stake-gno-swap.md).
{% endhint %}

The STAKE token is used by validators and delegators to secure the Gnosis chain. Users may participate in chain consensus, either as validators running nodes, or delegators placing stake on those nodes. Participants place STAKE to secure the chain, and receive rewards in both STAKE and xDai (for validators) thanks to[ unique reward mechanics](../for-stakers/stake-token/stake-reward-mechanics/).

STAKE also serves in a governance capacity (this is being replaced by GNO). Community members can [create and vote on proposals](../for-users/governance/stake-weighted-voting/) to change or update the protocol.

Additional chains will also have the opportunity to use STAKE to secure their chains, making this the first multi-chain enabled staking token.

## Neutral Network

The Gnosis chain provides a vital public utility for users - the ability to transfer stable value free of speculative concerns, volatility, or FUD (fear, uncertainty & doubt). GC is an independent network, built to support transactions that hold value. When DAI is bridged to GC, it moves to a platform with a clear, transparent purpose; secure & stable transactions on a fast, neutral network.

Open governance, open access, and token stability create a trusted environment for users as well as applications built on top of GC.

## Scalability&#x20;

GC supports low cost, stable transactions for projects and users. High Ethereum gas prices and congestion have made it difficult for the ecosystem to function efficiently. GC provides a compatible chain for projects requiring nano-transactions or complex transactions that may be prohibitively expensive on Ethereum.  GC can scale both vertically (infrastructure and chain parameter optimization) and horizontally (additional chain deployments) to meet capacity requirements.&#x20;

## On-Chain Randomness

Using a RANDAO-based Random Number Generator, validators produce random numbers used for validator selection. These random seeds are also available for usage by contracts deployed to GC. This allows for true on-chain randomness, eliminating the need to rely on a centralized service or 3rd party application. More information on how the RNG works is [available here](../for-developers/on-chain-random-numbers/).

## POSDAO Green Consensus

The GC currently uses a delegated Proof of Stake (DPOS) consensus mechanism called POSDAO. The [POSDAO white paper](../for-validators/posdao-whitepaper.md) describes all aspects of this new consensus protocol including a complete overview of the theory, rationale, security, and a detailed implementation section.

:green\_book:[ More on the GC energy efficient network](news-and-information/energy-efficiency/)

## Bridges to Ethereum

Two bridges connect GC to Ethereum, supporting seamless two-way asset transfer between chains. Tokens are acquired on the mainnet, then bridged to GC using either the Dai-xDai bridge for transactional tokens, or the OmniBridge for any cross-chain transfers. Once a user is finished transacting or staking, tokens can be bridged back to the mainnet with ease.

### L2 Chain Bridges

Additional bridges exist to move tokens between xDai and other EVM chains, including moving assets between [Binance Smart Chain](https://bsc-to-xdai-omnibridge.web.app) and Polygon (using the [xpollinate Connext state channel bridge](https://www.xpollinate.io)).

### Bridged Tokens

View tokens bridged to GC from Ethereum with the [OmniBridge UI ](https://xdai-omnibridge.web.app)built by [RaidGuild](https://raidguild.org).

* [Tokens bridged from Ethereum](https://blockscout.com/xdai/mainnet/bridged-tokens/eth)
* [Tokens bridged from BSC](https://blockscout.com/xdai/mainnet/bridged-tokens/bsc)

{% embed url="https://blockscout.com/xdai/mainnet/bridged-tokens" %}
