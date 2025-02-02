# STAKE weighted voting with Snapshot

STAKE holders participate in the governance process through a snapshot integration.&#x20;

🗳 [xDai Voting Page](https://snapshot.org/#/xdaistake.eth)

Community members can vote on proposals and introduce proposals for voting by other members. Once a proposal passes, the xDai team works with validators to support the protocol update.&#x20;

Note that **proposals are not automatically enacted, and some community proposals may not be accepted depending on the viability of the idea or total STAKE amount/ number of voters participating.**

{% hint style="info" %}
### **Who can Vote?**

[Snapshot](https://docs.snapshot.org) voters can use STAKE balances on Ethereum & on xDai. Those holding STAKE in the following ways can vote without needing to change any allocations or parameters.

1. STAKE holders on Ethereum Mainnet and on xDai Chain (STAKE held in an address).
2. STAKE liquidity providers for Uniswap v2 and Uniswap v3 (Ethereum Mainnet).
3. STAKE liquidity providers for SushiSwap (Ethereum Mainnet and xDai Chain). Staked LP token holders are eligible for voting.
4. EasyStaking participants (Ethereum Mainnet).
5. POSDAO validators (xDai Chain).
6. POSDAO delegators (xDai Chain).
7. STAKE liquidity providers for HoneySwap (xDai Chain). Staked LP token holders are eligible for voting.
8. STAKE deposited in Agave (xDai chain). Snapshot voting power based on ratio of available liquidity to total liquidity (amount borrowed within the protocol is not considered when determining voting power). **Voting power will be less than the amount deposited based on this ratio**.
9. STAKE delegated via Gnosis safe (Ethereum Mainnet only). [More info.](delegate-stake-voting-weight-with-gnosis-safe.md)

Others who want to vote must withdraw STAKE from a protocol to participate. Once the voting period is complete, STAKE can be moved back. Examples of protocols on xDai not supported by snapshot voting include:

* Elk finance
* Symmetric
* Swapr

_**Note**: Multisig wallet holders on xDai are not able to delegate voting power due to limitations of Snapshot. Snapshot's delegation contract is deployed on Ethereum Mainnet._ [_More info_](https://docs.snapshot.org/guides/delegation)_._&#x20;

_As a workaround, you can consider temporarily sending STAKE tokens to a regular address. You will be able to withdraw STAKE and send it back to a multisig wallet after you vote, there is no need to wait until the snapshot voting period is complete._
{% endhint %}

## Vote on an Existing Proposal

1\) Go to the xDai Snapshot Page: [https://snapshot.page/#/xdaistake.eth](https://snapshot.page/#/xdaistake.eth) and join the xDai Chain space if you haven't already.

2\) Connect your wallet to Ethereum using MetaMask or another application. This wallet should include the STAKE you want to use for voting purposes (or the connected wallet used with protocols like EasyStaking, Uniswap or Honeyswap. Balances will be combined for your weighted vote).

![](../../../.gitbook/assets/snapshot1.png)

3\) Click to select the proposal you would like to vote on.

![](../../../.gitbook/assets/snapshot2.png)

4\) Read the proposal and scroll to the bottom. Cast your vote by selecting a vote and clicking the vote button.

![](../../../.gitbook/assets/snapshot3.png)

5\) Sign the transaction in your web3 wallet. A vote does not require ETH.

![](../../../.gitbook/assets/snapshot4.png)

## Create a Proposal

Community members can create a proposal for a vote. This is the first step in suggesting or enacting an upgrade. Creating a proposal currently requires a minimum of 10 STAKE in a wallet.

If accepted by the community, the xDai team will assess the viability of the idea and see what next steps are required. **A passed vote does not guarantee a protocol change, but is viewed as a community suggestion and taken into consideration by the team.**

1\) Go to the xDai Snapshot Page: [https://snapshot.page/#/xdaistake.eth](https://snapshot.page/#/xdaistake.eth) and connect your web3 wallet.

2\) Click on New Proposal.

![](../../../.gitbook/assets/snapshotb1.png)

3\) Fill in all relevant details and Publish. Include the following:

1. Title
2. Proposal Body
3. Voting Items
4. Start and End Dates for the Proposal \* _(start and end dates use a calendar pop-up which may be off by 1 day. Adjust accordingly.)_
5. Click Publish.

![](../../../.gitbook/assets/snapshotb2.png)

4\) Sign the transaction.&#x20;

![](../../../.gitbook/assets/snapshotb3.png)

5\) Your proposal will appear in the Community section with the suggested parameters \*_Note: spam proposals will be deleted._

![](../../../.gitbook/assets/snapshotb4.png)

__

