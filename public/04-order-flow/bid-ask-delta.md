---
description: Read executed volume at the bid and ask and relate delta to actual price progress.
icon: arrow-right-arrow-left
---

# Bid / Ask / Delta

Trades executed at the ask are classified as aggressive buying; trades at the bid are aggressive selling. **Delta** is ask volume minus bid volume for a candle, price level, or session.

Delta measures aggression, not net capital entering the market. Every trade has a buyer and seller. Its value comes from comparing aggressive effort with price result.

## Effort versus result

- Positive delta with rising price: buying is effective.
- Positive delta with stalled or falling price: buying may be absorbed or trapped.
- Negative delta with falling price: selling is effective.
- Negative delta with stable or rising price: selling may be absorbed.

Interpret this at a meaningful location. A delta extreme in the middle of value is usually less useful than one at an auction boundary.

## Data limitations

Crypto order flow is venue-specific. A footprint from one exchange excludes activity elsewhere, and trade-classification methods can differ. Use a consistently liquid venue, compare spot with perpetuals when relevant, and avoid combining feeds without understanding normalization.

{% hint style="info" %}
Delta divergence is an observation, not an entry. It needs location, structural response, and an invalidation point.
{% endhint %}

**Drill:** Screenshot 30 high-delta candles at predefined levels. Label whether aggression produced progress over the next three candles and whether the level held.
