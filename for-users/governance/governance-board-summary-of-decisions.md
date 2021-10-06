# Governance Board Summary of Decisions

The [Bridge Governance Board](./#bridge-governance-board) is responsible for enacting updates related to bridge functionality, contract upgrades, and other parameters impacting bridge operations. The following items have been implemented by the board.

## Add Syncnode as Governor / xDai Bridge Oracle

🗳 **Justification:**  Increase decentralization by extending the governance and the bridge validators set to include Syncnode.

✅ **Governor Set Implemented:** January 22, 2021   
✅ **Oracle Implemented:** January 7, 2021 

## Upgrade Bridge Contracts

🗳 **Justification:**  A number of updates were made to the contracts to facilitate user engagement, support costs for xDai transfers, and provide logic for rebasing tokens. The minimum amount per token transaction was reduced to 1 wei \(primarily to support LP tokens or other token fractions\) and fees were set to 0.1% for xDai to Dai transfers.

✅ **Implemented:** March ****15, 2021 

## **Return user funds**

🗳 **Justification:**  A user accidentally [sent over 2000 USDC ](https://blockscout.com/xdai/mainnet/tx/0x2837cd89972f2e37a1cb631e60dbb761213010fe526a089c99f48ed483f63956)to the USDC token contract on xDai. After confirming the users identity, the board agreed to call the `claimTokensFromTokenContract` method and return the amount to the user. 

✅ **Implemented:** April 15, 2021

## Reduce USDC withdrawal fees to 0 for 3 months 

🗳 **Justification:** Current exit fees for USDC transfers on OmniBridge are currently 0.1%. The primary purpose of this temporary 3-month reduction to 0 fees is to attract more protocols utilizing USDC and OmniBridge for their activities.

✅ **Implemented:** June 15, 2021 

## Increase finalization time on Ethereum Mainnet

🗳 **Justification:**    
Increase the amount of blocks required for confirmation on the Ethereum Mainnet to 20, increaseing bridge operation reliability and security \(less chances for re-orgs\). This update slightly delays user transfers from 2.5 minutes to ~4 minutes.

✅ **Implemented:** August 20, 2021 

## Add 01Node & Peerion Representatives to the Governance Board

🗳 **Justification:**  Increase decentralization by extending the governance and the bridge validators set.

✅ **Implemented:** September ****22, 2021 

## Add 1Hive Representative to the Governance Board

🗳 **Justification:**  Increase decentralization by extending the governance and the bridge validators set.

✅ **Implemented:** October ****04**,** 2021 

## Upgrade Bridge Contracts

🗳 **Justification:** Add new functionality including increased AMB request ability, contracts to send requests, and fix a security vulnerability identified through the Bug Bounty program.

✅ **Implemented:** October 4**,** 2021 

## Include Compounding for xDai Bridge

🗳 **Justification:** Add compounding to support bridge operations. [Details here.](../bridges/converting-xdai-via-bridge/dai-compounding.md)

✅ **Implemented:** October 6**,** 2021 

