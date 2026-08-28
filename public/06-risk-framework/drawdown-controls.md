---
description: Precommit size reductions, trading halts, and review gates as equity declines.
icon: chart-line-down
---

# Drawdown controls

Drawdown measures the decline from the highest closed-equity peak.

`drawdown % = (peak equity - current equity) / peak equity × 100`

Use closed equity for the formal threshold and monitor open risk separately.
Do not reset the peak to make the percentage look smaller.

## Why drawdown needs policy

Recovery becomes nonlinear as losses deepen:

| Drawdown | Gain required to recover |
|---:|---:|
| 10% | 11.1% |
| 20% | 25.0% |
| 30% | 42.9% |
| 50% | 100.0% |

The objective is not to predict the next trade. It is to prevent normal model
uncertainty, execution errors, or behavioral deterioration from becoming ruin.

## Precommitted states

Define thresholds from the strategy's clean historical and forward-simulation
drawdowns:

| State | Required action |
|---|---|
| Normal | Base trade and portfolio limits apply |
| Caution | Reduce new-trade risk; trade only validated models |
| Defensive | Reduce heat further; require formal review before each session |
| Halt | No new live risk; investigate data, execution, regime, and adherence |

Set the percentages before trading. A threshold is meaningless if it can be
overridden because the next setup looks attractive.

## Session stop

Calculate session loss as:

`session risk consumed = realized losses + current unrealized losses + remaining open stop risk`

When the session limit is reached:

1. cancel all unfilled entry orders;
2. manage existing positions only under their written rules;
3. prohibit recovery trades and risk increases;
4. complete the post-trade review before the next permitted session.

## Resume gate

Resume after a halt only when:

- data and venue behavior are verified;
- all trades are classified by model and rule adherence;
- execution errors are separated from model losses;
- the model remains within its validated distribution or is returned to
  simulation;
- the next risk state and size are written.

{% hint style="warning" %}
A loss limit controls exposure, not emotion. Reaching it is an automatic state
transition, not a prompt to debate whether one more trade is justified.
{% endhint %}
