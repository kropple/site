---
description: Arbitrum Optimistic Rollup Deployment
---

# AoX: Arbitrum on xDai

Arbitrum has been deployed to xDai - AoX! We are currently working on configs, bridge installation and explorer integration. Look for more info and instructions coming soon.

For information on Arbitrum and usage basics, see the [Arbitrum docs](https://developer.offchainlabs.com/docs/developer_quickstart). Note that AoX is still being finalized on xDai, and some functionality is not yet available.

## Basic Info

| Item | Value |
| :--- | :--- |
| RPC | [https://arbitrum.xdaichain.com/](https://arbitrum.xdaichain.com/) |
| WSS | [wss://arbitrum.xdaichain.com/wss](wss://arbitrum.xdaichain.com/wss) |
| Chain ID | 200 |
| Rollup Contract | [0xc6a64a792618d834ba7f4126274f57db043ce095](https://blockscout.com/xdai/mainnet/address/0xc6A64a792618D834ba7F4126274F57DB043CE095/transactions) |
| Inbox Contract | [0x556c18a6fdcd52562ec1130212f6113e3f818335](https://blockscout.com/xdai/mainnet/address/0x556c18a6FDcd52562Ec1130212f6113e3F818335/transactions) |
| Outbox Contract | [0x0532D745F467fE541620564166749586f9fFe799](https://blockscout.com/xdai/mainnet/address/0x0532D745F467fE541620564166749586f9fFe799/transactions) |

## Deposits to AoX

Simple deposit functionality for users / bridge implementation is still in development. Devs can use the following ABI to call the  `depositEth` method. Use 0 for `maxSubmissionCost` and attach an amount of xDai tokens to the transaction. It may take several minutes for execution finalization. 

* [Deposit Example Transaction](https://blockscout.com/xdai/mainnet/tx/0x9cf6d6b352e5788ed2edea164431980d237c287ecf4a4ae0e7aca234ca9c42b1)
* ABI ⬇ 

```text
[{"type":"function","stateMutability":"payable","outputs":[{"type":"uint256","name":"","internalType":"uint256"}],"name":"depositEth","inputs":[{"type":"uint256","name":"maxSubmissionCost","internalType":"uint256"}]}]
```



