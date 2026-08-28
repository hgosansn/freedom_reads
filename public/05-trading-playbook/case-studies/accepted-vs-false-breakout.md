---
description: Use one boundary to distinguish an accepted breakout from a failed auction.
icon: code-branch
---

# Case: Accepted or false breakout

Reference boundary `R = 100.00`. Do not place either order at the first trade above `R`.

| Observable after the break | Branch A | Branch B |
|---|---|---|
| Time outside | Exceeds frozen minimum | Returns inside before minimum |
| Value and volume | Builds above `R` | Fails to build above `R` |
| Re-entry | No | Closes back below `R` |
| Authorized model | Breakout acceptance | Failed auction reversal |
| Retest order | Buy `R + d` from above | Sell `R - d` from below |

If neither definition completes, place no order. The two models are mutually exclusive at authorization time even though they share the same boundary. Record the first timestamp at which classification becomes possible.
