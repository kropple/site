---
description: Distributed community validation on xDai
---

# Stake Beacon Chain \(R&D\)

{% hint style="info" %}
Stake Beacon Chain \(SBC\) is currently in R&D. Targeting a Q3 soft beta launch for small-scale, distributed staking. SBC is experimental and does not include any security guarantees.
{% endhint %}

‌The Stake Beacon Chain offers a new consensus opportunity for the xDai chain. It is in early development, and will start with modified client implementations \(Prysm/Lighthouse\) to support faster blocks and built for a wider community of diverse validators.

‌While the Eth 2.0 staking deposit contract has attracted an impressive number of validators \(200K+\), these validators must each contribute 32 ETH to participate. This amount is out of reach for many blockchain users. In addition, centralized exchanges are pooling funds to create largely connected staking pools which may limit overall decentralization.

**‌**The SBC is designed for users with small staking amounts who still want to participate as independent validators within an **Ethereum-consistent and real-world value environment**. It provides a similar experience and uses a similar methodology for validator set rotation to prevent collusion. With a lower-stakes chain, the amount staked can also be lower while providing security and protection through enhanced decentralization.

## **Initial Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Variable</b>
      </th>
      <th style="text-align:left"><b>Value</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Required STAKE</td>
      <td style="text-align:left">32 STAKE</td>
    </tr>
    <tr>
      <td style="text-align:left">Block times</td>
      <td style="text-align:left">7 seconds</td>
    </tr>
    <tr>
      <td style="text-align:left">Validator Slots per Epoch</td>
      <td style="text-align:left">16 (<a href="https://notes.ethereum.org/@vbuterin/rkhCgQteN?type=view#Why-32-ETH-validator-sizes"><em>N &gt; 1 honest proposer/epoch as per V. Buterin</em></a>)</td>
    </tr>
    <tr>
      <td style="text-align:left">Validators per slot</td>
      <td style="text-align:left">128<b> (</b><a href="https://medium.com/@chihchengliang/minimum-committee-size-explained-67047111fa20"><em>explanation on minimum committee size</em></a><em>) </em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Epoch times</td>
      <td style="text-align:left">1.85 minutes</td>
    </tr>
    <tr>
      <td style="text-align:left">Slashing</td>
      <td style="text-align:left">Repeated reductions to 16 STAKE then removal</td>
    </tr>
    <tr>
      <td style="text-align:left">Clients</td>
      <td style="text-align:left">Ongoing testing with Prysm and Lighthouse clients.</td>
    </tr>
    <tr>
      <td style="text-align:left">Custom Deposit Contract</td>
      <td style="text-align:left">
        <ul>
          <li>ERC20-enabled deposits</li>
          <li>Upgradeability</li>
          <li>Claiming on accidental locks</li>
          <li>Custom network keys generation (deposit-cli)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Explorer</td>
      <td style="text-align:left">Modified version of <a href="http://beaconcha.in/">beaconcha.in</a> 
      </td>
    </tr>
    <tr>
      <td style="text-align:left">MVP for launch (pending system tolerance tests)</td>
      <td style="text-align:left">
        <p>2048 validators
          <br />65,536 STAKE</p>
        <p>47.4% APY</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Security Goal Prior to Merge</td>
      <td style="text-align:left">
        <p>20K+ validators</p>
        <p>640K+ STAKE</p>
        <p>15% APY</p>
      </td>
    </tr>
  </tbody>
</table>

Validators with a small amount of STAKE \(32 STAKE\) will be able to stake and run a node through a simplified, step-by-step process similar to [Ethereum launchpad](https://launchpad.ethereum.org/en/).

‌STAKE will be locked in the contract and not available for immediate withdrawal, as is the case with the current Eth 2.0 deposit contract. Modifications to the deposit contract will enable ERC20 token deposits \(STAKE\) and additional upgradeability features.

STAKE will be deposited from the xDai side, significantly reducing transaction costs. Once active, stakers will receive a staking derivative which can be used to earn additional incentives on aligned DEXs within the xDai ecosystem.

The system will be designed to support 7 second blocks, significantly faster than the 12 second blocks on Eth 2.0. Slashing will also be incorporated in accordance with the Eth 2.0 contracts, where stakers will be slashed for incongruous behavior and deactivated once the 16 STAKE minimum threshold is reached for failure to properly run a node.

Early stakers will be incentivized by an APY of nearly 50% \(47.4%\) for securing the chain. This incentive is quickly reduced as more validators onboard. For example with 4096 validators it is 33.7%. A sustainable ~15% APY is achieved when the security goal of 20,000 validators is met.\*

SBC will support all the same functionality and tools as Eth 2.0. While block times will slow slightly from the current 5 second model on xDai, blocks will be larger and over time rollups will provide the ability for additional transactional throughput and prioritization features.

Currently, the xDai chain is secured by ~640K STAKE by validators and their delegators. The goal is to match or exceed this amount. With 32 STAKE per validator, the system will require 20K+ validators to achieve the same level of security.

{% hint style="info" %}
\*[_ARP Calculator available here_](https://www.desmos.com/calculator/svnsuuyhf9) _where the Y axis is APR and the X axis is the number of validators divided by 100 and shifted by 20 \(2048 validators at point 0, 4096 validators at point ~20, 20'000 validators at ~180\)._

* F - some block reward factor
* T - time between blocks_=_
* S - amount of slots in an epoch
* N - amount of validators required for the launch.
{% endhint %}

