# Governance Board Summary of Decisions

The [Bridge Governance Board](./#bridge-governance-board) is responsible for enacting updates related to bridge functionality, contract upgrades, and other parameters impacting bridge operations. The following items have been implemented by the board.

## Add Syncnode as Governor / xDai Bridge Oracle

:ballot\_box: **Justification:**  Increase decentralization by extending the governance and the bridge validators set to include Syncnode.

:white\_check\_mark: **Governor Set Implemented:** January 22, 2021 \
:white\_check\_mark: **Oracle Implemented:** January 7, 2021&#x20;

## Upgrade Bridge Contracts

:ballot\_box: **Justification:**  A number of updates were made to the contracts to facilitate user engagement, support costs for xDai transfers, and provide logic for rebasing tokens. The minimum amount per token transaction was reduced to 1 wei (primarily to support LP tokens or other token fractions) and fees were set to 0.1% for xDai to Dai transfers.

:white\_check\_mark: **Implemented:** March **** 15, 2021&#x20;

## **Return user funds**

:ballot\_box: **Justification:**  A user accidentally [sent over 2000 USDC ](https://blockscout.com/xdai/mainnet/tx/0x2837cd89972f2e37a1cb631e60dbb761213010fe526a089c99f48ed483f63956)to the USDC token contract on xDai. After confirming the users identity, the board agreed to call the `claimTokensFromTokenContract` method and return the amount to the user.&#x20;

:white\_check\_mark: **Implemented:** April 15, 2021

## Reduce USDC withdrawal fees to 0 for 3 months&#x20;

:ballot\_box: **Justification:** Current exit fees for USDC transfers on OmniBridge are currently 0.1%. The primary purpose of this temporary 3-month reduction to 0 fees is to attract more protocols utilizing USDC and OmniBridge for their activities.

:white\_check\_mark: **Implemented:** June 15, 2021&#x20;

## Increase finalization time on Ethereum Mainnet

:ballot\_box: **Justification:**  \
Increase the amount of blocks required for confirmation on the Ethereum Mainnet to 20, increaseing bridge operation reliability and security (less chances for re-orgs). This update slightly delays user transfers from 2.5 minutes to \~4 minutes.

:white\_check\_mark: **Implemented:** August 20, 2021&#x20;

## Add 01Node & Peerion Representatives to the Governance Board

:ballot\_box: **Justification:**  Increase decentralization by extending the governance and the bridge validators set.

:white\_check\_mark: **Implemented:** September **** 22, 2021&#x20;

## Add 1Hive Representative to the Governance Board

:ballot\_box: **Justification:**  Increase decentralization by extending the governance and the bridge validators set.

:white\_check\_mark: **Implemented:** October **** 04**,** 2021&#x20;

## Upgrade Bridge Contracts

:ballot\_box: **Justification:** Add new functionality including increased AMB request ability, contracts to send requests, and fix a security vulnerability identified through the Bug Bounty program.

:white\_check\_mark: **Implemented:** October 4**,** 2021&#x20;

## Include Compounding for xDai Bridge

:ballot\_box: **Justification:** Add compounding to support bridge operations. [Details here.](../bridges/converting-xdai-via-bridge/dai-compounding.md)

:white\_check\_mark: **Implemented:** October 6**,** 2021&#x20;
