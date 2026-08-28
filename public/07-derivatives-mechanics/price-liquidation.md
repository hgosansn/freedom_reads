---
description: Separate last, index, mark, stop-trigger, liquidation, and bankruptcy prices.
icon: gauge-high
---

# Price references and liquidation

| Price | Operational meaning |
|---|---|
| Last | Most recent trade on the venue |
| Index | Reference assembled from external spot markets under venue rules |
| Mark | Fair-price estimate derived from index and basis inputs |
| Stop trigger | Selected reference that activates a conditional order |
| Liquidation price | Estimated price or account state at which forced reduction begins |
| Bankruptcy price | Internal level at which allocated margin is exhausted |

These prices can differ. A last-price candle does not prove that the mark price did or did not reach liquidation. Bybit, for example, states that mark price triggers liquidation, while cross and portfolio accounts are liquidated from an account maintenance-margin ratio rather than a fixed displayed price ([liquidation rules](https://www.bybit.com/en/help-center/article/FAQ-Order-Execution-and-Liquidation)).

## Protection test

Before entry:

1. Select the stop trigger source deliberately.
2. Compare planned stop, current mark, and estimated liquidation.
3. Stress mark-last divergence and adverse stop slippage.
4. Confirm the stop is reduce-only and sized to the resulting position.
5. Recheck after partial fills, added margin, funding, or another cross-margin position.

Liquidation calculations are venue, product, tier, and account-mode specific. Use the venue preview as a warning indicator, not as a guaranteed exit price.
