---
description: Distributed community validation on xDai
---

# Stake Beacon Chain \(R&D\)

{% hint style="info" %}
Stake Beacon Chain \(SBC\) is currently in R&D. Targeting a Q3 soft beta launch for small-scale, distributed staking. SBC is experimental and does not include any security guarantees.
{% endhint %}

‌The Stake Beacon Chain offers a new consensus opportunity for the xDai chain. It is in early development, and will start with a single client implementation \([likely Prysm](https://prysmaticlabs.com/), but this is not yet confirmed\) modified to support faster blocks and built for a wider community of validators.

‌While the Eth 2.0 staking deposit contract has attracted an impressive number of validators \(200K+\), these validators must each contribute 32 ETH to participate. This amount is out of reach for most blockchain users. In addition, centralized exchanges are pooling funds to create largely connected staking pools which may limit overall decentralization.

**‌**The SBC is designed for users with small staking amounts who still want to participate as independent validators within an Ethereum-consistent and rea;-world value environment. It provides a similar experience and uses a similar methodology for validator set rotation to prevent collusion. When the stakes are lower, the amount staked can also be lower while providing security and protection through enhanced decentralization.

## **Initial Parameters**

| **Variable** | **Value** |
| :--- | :--- |
| Required STAKE | 32 STAKE |
| Block times | 7 seconds |
| Validator Slots per Epoch | 16 \( [_N &gt; 1 honest proposer/epoch as per V. Buterin_](https://notes.ethereum.org/@vbuterin/rkhCgQteN?type=view#Why-32-ETH-validator-sizes)\) |
| Validators per slot | 128 **\(**[_explanation on minimum committee size_](https://medium.com/@chihchengliang/minimum-committee-size-explained-67047111fa20)_\)_  |
| Epoch times | 1.85 minutes |
| Slashing | Repeated reductions to 16 STAKE then removal |
| MVP for launch \(pending system tolerance tests\) | 2048 validators 65,536 STAKE |
| Security Goal | 650K STAKE prior to merge |

Validators with a small amount of STAKE \(32 STAKE\) will be able to stake and run a node through a simplified, step-by-step process. 

‌Stake will be locked in the contract and not available for immediate withdrawal, as is the case with the current Eth 2.0 deposit contract. STAKE will be deposited from the xDai side, significantly reducing transaction costs. Once active, stakers will receive a staking derivative which can be used to earn additional incentives on aligned DEXs within the xDai ecosystem.

The system will be designed to support 7 second blocks, significantly faster than the 12 second blocks on Eth 2.0. Slashing will also be incorporated in accordance with the Eth 2.0 contracts, where stakers will be slashed for incongruous behavior and deactivated once the 16 STAKE minimum threshold is reached for failure to properly run a node.

SBC will support all the same functionality and tools as Eth 2.0. While block times will slow slightly from the current 5 second model on xDai, blocks will be larger and over time rollups will provide the ability for additional transactional throughput and prioritization features.

Currently, the xDai chain is secured by ~650K STAKE by validators and their delegators. The goal is to match or exceed this amount. With 32 STAKE per validator, the system will require 20K+ validators to achieve the same level of security.

_Additional technical details coming soon as we explore this exciting implementation!_  






  

