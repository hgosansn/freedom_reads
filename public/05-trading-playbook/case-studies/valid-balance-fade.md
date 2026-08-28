---
description: Price, size, and manage a qualified long balance-edge fade.
icon: circle-check
---

# Case: Valid balance fade

At 13:00 UTC, BTC is rotating inside a four-hour balance: VAL `99.80`, POC `101.50`, VAH `103.20`. The tested lower-edge zone is `99.70` to `99.90`. No scheduled event falls inside the holding window.

| Frozen field | Value |
|---|---|
| Variant | Location-first resting limit |
| Entry | Zone midpoint, buy `99.80` |
| Invalidation | Acceptance below `99.40` |
| Expected stop fill | Stop-market at `99.30`, last-price trigger |
| Cancellation | Two execution intervals below `99.40`, or POC trades first |
| Target 1 / 2 | POC `101.50` / VAH `103.20` |

With a `100 USDT` risk budget, `0.05%` entry and exit fees, and `0.10` adverse stop slippage per unit:

`loss per unit = 0.50 + 0.0499 + 0.04965 + 0.10 = 0.69955`

`quantity = floor_to_step(100 / 0.69955)`

At a `0.001` quantity step, the maximum is `142.948` units. The example uses abstract units; a real BTC contract must use its venue multiplier and notional limits.

Price touches `99.80`, fills, rejects the edge, and reaches POC. The valid review question is whether execution matched the specification, not whether the trade won.
