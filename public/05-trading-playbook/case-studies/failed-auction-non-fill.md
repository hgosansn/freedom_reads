---
description: Preserve failed-auction discipline when the authorized retest never occurs.
icon: forward-step
---

# Case: Failed auction with no fill

A prior high at `100.00` is swept to `100.80`. Price returns below `100.00` within two intervals and closes at `99.90`, satisfying the frozen failure rule. The retest-limit variant authorizes a sell at `99.95` on the first retest from below.

| Field | Value |
|---|---|
| Entry | Sell limit `99.95` after reclaim |
| Invalidation | Stop-market above `100.90` |
| Cancellation | POC `98.60` trades before entry, or retest window expires |
| Outcome | Price moves directly to `98.60`; order never fills |

Cancel at POC. Do not sell at `98.60`: the remaining target distance no longer pays for the structural stop. Log the opportunity, authorized order, non-fill, and maximum favorable excursion from the theoretical entry separately.
