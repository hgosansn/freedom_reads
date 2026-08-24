---
description: Use cumulative volume delta to track the running balance of aggressive buying and selling.
icon: chart-area
---

# CVD

Cumulative volume delta (CVD) is the running sum of ask volume minus bid volume. Rising CVD indicates net aggressive buying over the selected window; falling CVD indicates net aggressive selling.

## Useful comparisons

- **Price and CVD rise:** aggressive buying supports the move.
- **Price rises while CVD falls:** passive buyers may be lifting price, sellers may be absorbed, or the selected feed may not represent the move.
- **Price falls while CVD rises:** buying is ineffective and may be absorbed.
- **Price holds while CVD trends:** persistent aggression is being met by passive liquidity.

Divergence identifies a mismatch between executed aggression and price. It can persist throughout a trend when passive participants continue to absorb and reprice inventory.

## Choose the right series

Spot CVD can help judge organic demand; perpetual CVD reflects leveraged aggression. Comparing both may reveal whether derivatives are leading. Reset periods also matter: session CVD answers a different question from an anchored CVD beginning at a swing or event.

## Reliability checklist

Confirm venue coverage, trade classification, reset time, missing data, and whether historical values repaint after reconnection. Keep settings fixed during a study.

{% hint style="info" %}
CVD identifies which side crossed the spread. Price response measures the effectiveness of that aggression.
{% endhint %}

**Study protocol:** Anchor CVD at 50 structural pivots using fixed venue coverage. Categorize alignment and divergence, then measure continuation and reversal rates by location, regime, and spot-perpetual confirmation.
