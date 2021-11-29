---
description: Preparing and running an independent validator node
---

# Get Started

{% hint style="warning" %}
Instructions are in process and not yet complete. Testnet implementation only.
{% endhint %}

## 1) Setup and run your xDai node&#x20;

You can select either OpenEthereum or Nethermind as your client of choice. Follow these instructions to get started:

* [Nethermind](../../../for-developers/install-xdai-client/nethermind.md)
* [OpenEthereum](../../../for-developers/install-xdai-client/parity.md)

## 2) Generate a validator account using the deposit CLI

These instructions use native python, see the `Readme` for other options.

1. git clone  [https://github.com/openethereum/sbc-deposit-cli](https://github.com/openethereum/sbc-deposit-cli) and cd into sbc-deposit-cli root folder.&#x20;
2.  Check you are using Python Version >= Python3.7

    ```
    python3 -V
    ```
3.  Run the helper script to install dependencies

    ```
    ./deposit.sh install
    ```
4.  Run the following command to access the interactive CLI

    ```
    ./deposit.sh new-mnemonic --chain stake
    ```
5. Generate your keys following the prompts.
   1. Choose how many validators you want to run.
   2. Choose a password to store validator keystore(s) (you will need this password later for beacon client implementation, so save securely).
   3. Write down your 24 word mnemonic (KEEP OFFLINE).
   4. Confirm you mnemonic.
   5. deposit data and keystore.json files will be created in a newly created validator\_keys folder.

## 3) Choose beacon chain client and setup a node

Current instructions use Sokol testnet implementation_._ **Node should be completely synced before proceeding to step 4: Deposit Staking Token**

### Prysm

Follow the instructions here: [https://github.com/openethereum/sbc-prysm-launch/tree/gbc-testnet](https://github.com/openethereum/sbc-prysm-launch/tree/gbc-testnet)

Once complete, check the sync status of your node:

```
curl http://localhost:3500/eth/v1alpha1/node/syncing
```

&#x20;If your node is done synchronizing, you will see the response:

```
 {"syncing":false}
```

### Lighthouse

Follow the instructions here: [https://github.com/openethereum/sbc-lighthouse-launch/tree/gbc-testnet](https://github.com/openethereum/sbc-lighthouse-launch/tree/gbc-testnet)

## 4) Deposit staking token&#x20;

(UI for staking contract in process, staking will require two transactions. The first will wrap deposit tokens into a metaToken, and the second will deposit the mToken using the  `transferAndCall` method).

## 5) Check status

&#x20;[https://beacon.blockscout.com/ ](https://beacon.blockscout.com)
