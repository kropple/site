# Technical Prerequisites

### The Basics

Since SBC is a smaller-stakes environment, it is a great place to refine new skills. Be sure to read directions and ask questions if they come up! &#x20;

* **Using the Terminal**:  You will be required to enter commands into a terminal window. These will be simple copy-paste instructions, but familiarity with using a terminal is helpful.&#x20;
* **Key Management**: You will use a cli to derive a key-pair for validating blocks as well as a mnemonic you will use later to derive a withdrawal pair. It is important to store these safely (offline if possible).

### xDai Node

To process validator deposits it is recommended to run your own xDai node. It will be possible to link SBC to an existing node through a JSON RPC endpoint, however we recommend running your own node to promote decentralization. xDai Nodes can be run with 2 clients and the following recommended minimum specs:

* OS: Ubuntu (Nethermind & OE), Windows & MacOs (Nethermind only)
* CPU: 2 cores
* RAM: 4GB
* Disk: 50gb SSD
* Git installed `git --version`

\-> [Nethermind Node Setup](../../../for-developers/install-xdai-client/nethermind.md)

\-> [OpenEthereum Node Setup](../../../for-developers/install-xdai-client/parity.md)

### Connectivity

A reliable internet connection is key - bandwidth should not be throttled or capped. Upload bandwidth should be a minimum of 700 MB/hour with increases likely. Brief periods offline may result in small inactivity penalties, but this will be recouped quickly as long as the outage is short.

Note that synching xDai may take up to 12 hours depending on your setup.&#x20;





