---
description: Manage open risk with rules tied to market information rather than open profit and loss.
icon: sliders
---

# Management

Trade management answers how new information changes exposure after entry. The objective is not to eliminate discomfort; it is to preserve the setup's expectancy while controlling unacceptable risk.

## Predefine the model

- **Set and hold:** stop and target remain unchanged. Best for clean testing.
- **Structural trail:** stop follows confirmed swings or accepted value.
- **Scale and trail:** realize part at a defined objective and manage the remainder.
- **Time stop:** exit if the expected response does not occur within a tested window.

## Information-based decisions

Move risk only when the market has invalidated the original adverse path. Reaching an arbitrary profit amount does not necessarily justify breakeven. In many setups, a normal retest occurs after initial progress; premature protection converts valid trades into scratches.

Valid reasons to reduce exposure may include failed follow-through, opposing acceptance, event risk not present at entry, or correlated market breakdown. Write these contingencies before entry where possible.

## Operational risks

Crypto runs continuously. Plan for exchange outages, API failure, funding timestamps, low-liquidity hours, and inability to monitor. Use server-side protective orders when supported, avoid relying only on alerts, and understand reduce-only and trigger-price settings.

{% hint style="danger" %}
Never remove a protective stop because price is close to it. New analysis made under loss pressure is not independent evidence.
{% endhint %}

**Drill:** Replay one setup under set-and-hold and structural-trail rules. Compare expectancy, drawdown, average win, and management errors over at least 50 cases.
