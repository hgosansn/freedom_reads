---
description: Cancel a resting fade when the auction begins accepting outside balance.
icon: ban
---

# Case: Canceled balance fade

The same balance has VAL `99.80`, but price trades below it for three execution intervals, volume builds at `99.40`, and POC begins migrating down before the resting buy is filled.

## Decision sequence

1. Initial context authorizes a buy at `99.80`.
2. Price trades through the edge without a fill because the order is behind queue.
3. The frozen acceptance rule completes below balance.
4. Cancel the remaining order immediately.
5. Reclassify as potential downside discovery; do not widen the fade zone.

The order is canceled even if price later rotates upward. That later outcome was unavailable at the cancellation timestamp. A canceled valid order is recorded separately from a losing trade and from an operator error.
