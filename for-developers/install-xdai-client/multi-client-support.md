---
description: Gnosis Chain is supported by OpenEthereum & Nethermind
---

# Multi-Client Support

A blockchain client is the software that runs on every node in the chain. It is responsible for connecting with other nodes, verifying transactions, and relaying and syncing blocks across the network. Some examples of popular Ethereum clients include [Geth](https://geth.ethereum.org) and [OpenEthereum](https://github.com/openethereum/openethereum) (formerly Parity) and newer clients like [Hyperledger Besu](https://besu.hyperledger.org/en/stable/) and [Nethermind](http://nethermind.io). If you want to run a blockchain node, you first need to setup a client on that node.

Ethereum clients are designed to implement the protocol correctly and support multiple consensus features. Each uses different methods to achieve this. The Gnosis Chain is an Ethereum-based stable sidechain with several unique consensus features in POSDAO, and client modifications are necessary for support. POSDAO consensus on GC is now supported by 2 open-source clients, **OpenEthereum and Nethermind.**

Gnosis Chain (then called xDai chain) was originally supported by Parity using the AuRa Authority Round consensus model. Parity is written in Rust, and recently transitioned to a DAO ownership model and rebranded as OpenEthereum. While Gnosis Chain with POSDAO still uses the AuRa method to seal blocks in version 1, other changes were required to support validator selection, rewards, malicious reporting and other features in POSDAO. These were implemented in Parity stable version 2.7.2, then ported to the first OpenEthereum release 3.0+.

We've also collaborated with the Nethermind team to incorporate POSDAO consensus. The Nethermind client is written in .Net, and is fast, light-weight and user-friendly. POSDAO is now supported and [a majority of validators are running this client](https://dai-netstat.poa.network).

Both clients fully support the underlying consensus, which is important for transaction verification and interoperability with the Ethereum Mainnet. Gnosis Chain offers 5 second blocks, and every transaction within a block is verified once the block is signed. The results of these transactions can then be immediately bridged to the mainnet with guaranteed accuracy. There is no need to wait for fraud proofs or other verification methods to interact with the Ethereum mainnet.

## Why multi-client support is important

1. **Safety and security.** Enabling multiple clients prevents a single source of failure. It is possible a client specific attack may occur which renders a client unusable, but does not impact the blockchain as a whole. If multiple clients are running proportionally, a client-centered attack will not completely bring down the system.&#x20;
2. **Checks and balances**: A client may be coded incorrectly, or handle a use case in a different way from another client. If there are any discrepancies, these can be quickly identified and investigated. This is especially important with new consensus algorithms like POSDAO, where certain edge cases may present themselves at a later time.&#x20;
3. **Diversity, transparency & choice**: Ecosystem diversity is important for all aspects of a blockchain network. Wallets, block explorers and clients should all have multiple implementations to promote decentralization and options for users. This creates transparency and user choice. Some node operators may prefer to run OpenEthereum and others Nethermind based on their machine specs, language preferences or for other reasons. Users should always have a choice in preferred tools.  Support from multiple clients brings redundancy and diversity to the Gnosis chain, creating an additional layer of trust for node operators and chain users.&#x20;
