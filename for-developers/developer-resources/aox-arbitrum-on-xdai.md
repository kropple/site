---
description: Arbitrum Optimistic Rollup Deployment
---

# AoX: Arbitrum on xDai

Arbitrum has been deployed to xDai - AoX! We are currently working on configs, bridge installation and explorer integration. Look for more info and instructions coming soon.

For information on Arbitrum and usage basics, see the [Arbitrum docs](https://developer.offchainlabs.com/docs/developer_quickstart). Note that AoX is still being finalized on xDai, and some functionality is not yet available.

## Basic Info

| Item | Value |
| :--- | :--- |
| RPC | [http://23.239.11.93:8547](http://23.239.11.93:8547/) |
| WSS | [http://23.239.11.93:8548](http://23.239.11.93:8548/) |
| Chain ID | 42161 |
| Rollup Contract | [0x21AB1Fc6b116dD577409E47b8a7Af87A72b892a2](https://blockscout.com/xdai/mainnet/address/0x21AB1Fc6b116dD577409E47b8a7Af87A72b892a2) |
| Inbox Contract | [0x2bd67c9b0045bc1B7cBD2b495E10265A372F830a](https://blockscout.com/xdai/mainnet/address/0x2bd67c9b0045bc1B7cBD2b495E10265A372F830a) |
| Outbox Contract | [0x5877eF3A233A95A580a0c96aF88f1A08f1773959](https://blockscout.com/xdai/mainnet/address/0x5877eF3A233A95A580a0c96aF88f1A08f1773959) |

![](../../.gitbook/assets/aox%20%281%29.png)

## Deposits to AoX

Simple deposit functionality for users / bridge implementation is still in development. Devs can use the following ABI to call the  `depositEth` method. Use 10000000 for `maxSubmissionCost` and attach an amount of xDai tokens to the transaction. It may take several minutes for execution finalization. 

* [Deposit Example Transaction](https://blockscout.com/xdai/mainnet/tx/0xacdd93bc41fada9fa6381fe99063d318e513e09842f252d150ff92185c8c937f)
* ABI ⬇ 

```text
[{"type":"function","stateMutability":"payable","outputs":[{"type":"uint256","name":"","internalType":"uint256"}],"name":"depositEth","inputs":[{"type":"uint256","name":"maxSubmissionCost","internalType":"uint256"}]}]
```



