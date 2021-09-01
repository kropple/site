---
description: Arbitrum Optimistic Rollup Deployment
---

# AoX: Arbitrum on xDai

Arbitrum has been deployed to xDai - AoX! We are currently working on configs and bridge installation, [Blockscout is already configured for AoX](https://blockscout.com/xdai/aox/). Look for more info and instructions coming soon.

For information on Arbitrum and usage basics, see the [Arbitrum docs](https://developer.offchainlabs.com/docs/developer_quickstart). Note that AoX is still being finalized on xDai, and some functionality is not yet available. 

## Basic Info

| Item | Value |
| :--- | :--- |
| RPC | [https://arbitrum.xdaichain.com/](https://arbitrum.xdaichain.com/) |
| WSS | [wss://arbitrum.xdaichain.com/wss](wss://arbitrum.xdaichain.com/wss) |
| Chain ID | 200 |
| Explorer | [https://blockscout.com/xdai/aox/](https://blockscout.com/xdai/aox/) |
| Rollup Contract | [0xc6a64a792618d834ba7f4126274f57db043ce095](https://blockscout.com/xdai/mainnet/address/0xc6A64a792618D834ba7F4126274F57DB043CE095/transactions) |
| Inbox Contract | [0x556c18a6fdcd52562ec1130212f6113e3f818335](https://blockscout.com/xdai/mainnet/address/0x556c18a6FDcd52562Ec1130212f6113e3F818335/transactions) |
| Outbox Contract | [0x0532D745F467fE541620564166749586f9fFe799](https://blockscout.com/xdai/mainnet/address/0x0532D745F467fE541620564166749586f9fFe799/transactions) |

## MetaMask Custom Network

![](../../.gitbook/assets/xdai-arbitrum.png)

## Deposits to AoX

Simple deposit functionality for users / bridge implementation is still in development. Devs can use the following ABI to call the  `depositEth` method. Use 0 for `maxSubmissionCost` and attach an amount of xDai tokens to the transaction. It may take several minutes for execution finalization. 

* [Deposit Example Transaction](https://blockscout.com/xdai/mainnet/tx/0x9cf6d6b352e5788ed2edea164431980d237c287ecf4a4ae0e7aca234ca9c42b1)
* ABI ⬇ 

```text
[
  {
    "inputs": [
      {
         "internalType": "address[]",
         "name": "_validator",
         "type": "address[]"
      },
      {
         "internalType": "bool[]",
         "name": "_val",
         "type": "bool[]"
      }
    ],
    "name": "setValidator",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  }
]
```

### MyCrypto Deposit Example

1. Connect to the xDai chain and click **Send**.
2. Choose the inbox contract as the recipient [0x556c18a6fdcd52562ec1130212f6113e3f818335](https://blockscout.com/xdai/mainnet/address/0x556c18a6FDcd52562Ec1130212f6113e3F818335/transactions)
3. Click on Show Advanced Options and enter the encoded call for the depositEth method in the data field. Click Next to finalize the tx. `0x0f4d14e90000000000000000000000000000000000000000000000000000000000000000`

![](../../.gitbook/assets/my-crypto-1.png)

{% hint style="success" %}
Once completed, it may take several minutes for the transaction to arrive at your address on the rollup. Switch to the rollup in Metamask to view the deposit.
{% endhint %}

### Withdrawals

_Instructions in process_

### Contract Deployment

#### Hardhat

Simply use the xDai Arbitrum RPC url in your `hardhat.config.ts`:

```text
module.exports = {
  solidity: '0.7.3',
  networks: {
    arbitrum: {
      url: 'https://arbitrum.xdaichain.com/',
      gasPrice: 0,
    },
  },
}
```

