---
description: Reject a trend-pullback order when external structure enters transition.
icon: road-barrier
---

# Case: Pullback during transition

The four-hour auction has higher highs and higher lows, but the daily auction reaches a prior weekly high. The first pullback zone is `102.00` to `102.40`. Before entry, price breaks the last four-hour higher low at `101.20`, then accepts below it.

## Classification

- The old trend label describes completed history.
- The current external auction is now in transition.
- The location-first buy at `102.20` is canceled.
- A reclaim may later create a different model, but it cannot restore the canceled specification retrospectively.

No limit order is placed. This case prevents a common error: treating an attractive discount to a previous trend as proof that the trend remains accepted.
