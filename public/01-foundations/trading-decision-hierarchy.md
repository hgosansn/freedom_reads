---
description: Organize trading decisions from market context to risk so lower-timeframe signals never override higher-order information.
icon: layer-group
---

# The trading decision hierarchy

Signals inherit meaning from context. Positive delta can confirm continuation above accepted value or identify ineffective buying at a range high. Process evidence in a fixed order so a lower-timeframe print cannot override auction context.

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

Count independent evidence. Market structure and a moving average derived from the same price series are one price-based input, not two confirmations. A stronger evidence stack combines location, auction behavior, and order-flow response.

{% hint style="warning" %}
Starting with an entry signal and working backward reverses the hierarchy. Reject any trade whose context and location were documented only after the trigger appeared.
{% endhint %}

**Study protocol:** For 30 historical sessions, freeze the chart at the decision time and write the regime plus two conditional branches. Score each condition as observable, ambiguous, or retrospective. Retain only conditions that two independent reviewers could classify consistently.
