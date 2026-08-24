---
description: Organize trading decisions from market context to risk so lower-timeframe signals never override higher-order information.
icon: layer-group
---

# The trading decision hierarchy

A signal has no independent meaning. The same positive delta can confirm continuation above accepted value or mark trapped buyers at a range high. Decisions become coherent when evidence is processed in a fixed order.

## The hierarchy

1. **Regime:** balance, trend, or transition.
2. **Location:** value, range edge, breakout area, prior extreme, or liquidity pool.
3. **Narrative:** the falsifiable path price is expected to take.
4. **Setup:** a named playbook pattern with known statistics.
5. **Trigger:** observable authorization to enter now.
6. **Risk:** invalidation, size, targets, and management.

Higher layers constrain lower ones. A five-minute trigger cannot repair a poor daily location, and attractive reward-to-risk cannot make an invalid thesis valid.

## Build a conditional plan

Replace prediction with branching logic:

> If BTC auctions above the prior value-area high and builds volume there, look for breakout acceptance. If it trades above but returns rapidly into value, evaluate a failed-auction reversal. If neither occurs, do nothing.

Each branch specifies evidence, response, and non-action. This keeps the trader responsive without becoming reactive.

## Evidence weighting

Treat confluence as independent evidence, not a collection of correlated indicators. Market structure and a moving average derived from the same price series are not two independent facts. Stronger confluence combines different dimensions: location, auction behavior, and order-flow response.

{% hint style="warning" %}
Never start with an entry signal and work backward to justify it. That reverses the hierarchy and encourages confirmation bias.
{% endhint %}

**Drill:** For 20 historical sessions, write only the regime and two conditional branches before viewing the session outcome. Score whether your conditions were observable and whether you respected the no-trade branch.
