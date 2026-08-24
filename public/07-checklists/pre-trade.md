---
description: Validate setup, evidence, execution, and portfolio risk immediately before placing an order.
icon: list-check
---

# Pre-trade

Pause before every order. The purpose is to prevent urgency from bypassing the decision hierarchy.

## Thesis

- [ ] What is the regime on the analysis timeframe?
- [ ] Is this location defined by the selected profile, external structure, or measured liquidity?
- [ ] Which named playbook setup is present?
- [ ] What observable evidence confirms it now?
- [ ] What would prove the thesis wrong?
- [ ] Am I interpreting current information rather than chasing a move I missed?

## Trade construction

- [ ] Entry price or trigger is explicit.
- [ ] Stop is beyond structural invalidation and allows normal noise.
- [ ] Primary target follows from the auction path.
- [ ] Reward relative to risk passes the setup's tested threshold.
- [ ] Size is calculated from fixed account risk, including fees and slippage.
- [ ] Liquidation is safely beyond the stop; leverage and margin mode are understood.

## Portfolio and operations

- [ ] Combined open risk remains within the session limit.
- [ ] Correlated positions are counted as concentrated exposure.
- [ ] No high-impact event falls inside the unplanned holding window.
- [ ] Correct instrument, venue, direction, quantity, order type, and reduce-only setting are selected.
- [ ] Protective order is live or will be placed atomically.

## Final gate

Complete this sentence:

> Because the market is **[context]** at **[location]**, if **[trigger]** occurs I will enter **[direction]**, invalidate at **[condition/price]**, and target **[objective]**, risking **[amount]**.

{% hint style="warning" %}
Reject the order if any bracket remains undefined. “I will manage it live” supplies no testable risk rule.
{% endhint %}
