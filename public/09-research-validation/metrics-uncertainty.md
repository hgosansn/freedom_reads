---
description: Evaluate fills, losses, expectancy, drawdown, and uncertainty rather than win rate alone.
icon: chart-column
---

# Metrics and uncertainty

Measure the decision chain, not only completed trades:

| Layer | Metrics |
|---|---|
| Opportunity | Eligible events, classification agreement, missing-data rate |
| Order | Placement rate, fill rate, adverse selection, cancellation reason |
| Trade | Win rate, average win and loss, MAE, MFE, hold time |
| Strategy | Net expectancy, drawdown, exposure, turnover, cluster loss |
| Execution | Fees, spread, slippage by size and volatility, rejected orders |

`expectancy = P(win) × average win - P(loss) × average loss - average costs`

Report medians, tails, and interval estimates beside averages. Bootstrap by the natural dependency block, such as day or session, rather than shuffling individual trades when signals cluster.

Compare realized limit-order fills with all eligible opportunities. Excluding non-fills creates selection bias and can make an unusable entry appear profitable.
