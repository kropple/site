---
description: Mechanism for additional value capture of Dai locked in the bridge
---

# Dai Compounding

_Updated October 5, 2021_

The latest TokenBridge upgrade includes the ability to allocate Dai locked in the TokenBridge contract to the [Compound interest rate market](https://compound.finance/). Locked funds accumulate interest and COMP tokens, and these funds can be used to support bridge operations. 

### Initial Mechanisms

1. As a part of the bridge upgrade, an amount of locked Dai \([_Current Amount Locked - ~22,000,000 Dai_](https://etherscan.io/token/0x6b175474e89094c44da98b954eedeac495271d0f?a=0x4aa42145aa6ebf72e164c9bbc74fbd3788045016) __\) is transferred to Compound.
2. 1,000,000 Dai remains in the bridge contract as a reserve supporting daily operations.

![](../../../.gitbook/assets/blank-diagram-2-%20%281%29.png)

### User Actions

1. **Dai bridged from Ethereum to xDai:** Following the upgrade, any amount of Dai bridged from Ethereum to xDai ****is added to the bridge reserve. It is not automatically transferred to Compound.
2. **xDai bridged from xDai to Ethereum:** Bridge requests from xDai to Ethereum will use the Dai in the reserve. If a request is initiated that exceeds the available reserve amount, the requested amount exceeding the amount held in reserve + 1,000,000 Dai \(required reserve\) is withdrawn immediately from Compound. The 1,000,000 Dai replenishes the reserve.  `if current_reserve < requested  withdraw requested - current_reserve + required_reserve`

![](../../../.gitbook/assets/user2.png)

### Interest & Funds

1. Interest on the Dai supplied to Compound and COMP tokens will be collected periodically \(approximately monthly\) and transferred to an EOA through a manual method call. Funds will be used to support bridge operations such as gas refunds for users or other tbd mechanisms which can be discussed and decided on by the bridge governors.
2. Once the reserve reaches a significantly higher amount than what is required for daily operations, bridge governors can decide to send this excess amount to Compound.

### Upgradability / Governance

1. Bridge governors can vote to turn off the compounding mechanism at any time. If turned off, all Dai tokens will be returned to the bridge contract.
2. Bridge governors can vote to change the interest receiving address if required \(currently must be an EOA or a contract supporting the [`onInterestReceived`](https://github.com/poanetwork/tokenbridge-contracts/blob/master/contracts/interfaces/IInterestReceiver.sol) method\).

### Risks

1. An unlikely scenario can arise where the amount of Dai requested for withdrawal is not available on Compound \(due to high borrowing demand\). In this case, a user will need to wait until Compound liquidity is available to execute the request. 
2. Compound protocol is a trusted entity. If compromised the protocol could attack the contracts in various ways, e.g., through reentrancy or by simply stealing funds. 

{% hint style="info" %}
Note: TVL metrics displayed in sources such as [DeFiLama ](https://defillama.com/protocol/xdai-stake)and [DeFiPulse](https://defipulse.com/xdai) will reflect reflect different values once Dai is sent to Compound. We will incorporate metrics into the [xDai Bridge Dune Analytics Dashboard](https://dune.xyz/maxaleks/xDai-Bridge) to reflect current invested amount as well as locked reserve amount.
{% endhint %}

### OmniBridge Upgrade

An upgrade is planned for the OmniBridge following the TokenBridge upgrade. OmniBridge will utilize Aave in the same manner to earn interest on additional tokens with similar parameters in place. Additional details posted shortly.

### Resources:

The compounding functionality recently underwent a [thorough security audit from ChainSecurity](../../../for-developers/security-audits.md#omnibridge-audit-by-chainsecurity-1).

* **TokenBridge contracts**: [https://github.com/poanetwork/tokenbridge-contracts/tree/master/contracts/upgradeable\_contracts](https://github.com/poanetwork/tokenbridge-contracts/tree/master/contracts/upgradeable_contracts)
* **OmniBridge contracts**: [ https://github.com/omni/omnibridge/tree/master/contracts/upgradeable\_contracts](%20https://github.com/omni/omnibridge/tree/master/contracts/upgradeable_contracts)



