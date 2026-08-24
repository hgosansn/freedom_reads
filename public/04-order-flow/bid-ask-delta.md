---
description: Read executed volume at the bid and ask and relate delta to actual price progress.
icon: arrow-right-arrow-left
---

# Bid / Ask / Delta

Trades executed at the ask are classified as aggressive buying; trades at the bid are aggressive selling. **Delta** is ask volume minus bid volume for a candle, price level, or session.

Delta measures aggression, not net capital entering the market. Every trade has a buyer and seller. Its value comes from comparing aggressive effort with price result.

![Effective aggression, absorption, and exhaustion as effort versus price result](../.gitbook/assets/diagrams/effort-result.svg)

## Effort versus result

- Positive delta with rising price: buying is effective.
- Positive delta with stalled or falling price: buying may be absorbed or trapped.
- Negative delta with falling price: selling is effective.
- Negative delta with stable or rising price: selling may be absorbed.

Interpret delta at a predefined auction location. An extreme in the middle of value has weak directional information; the same print at a boundary tests whether aggressive flow can move the auction.

## Data limitations

Crypto order flow is venue-specific. A footprint from one exchange excludes activity elsewhere, and trade-classification methods can differ. Use a consistently liquid venue, compare spot with perpetuals when relevant, and avoid combining feeds without understanding normalization.

{% hint style="info" %}
Delta divergence records a mismatch between aggression and price. Entry still requires location, structural response, and a defined invalidation.
{% endhint %}

**Study protocol:** Sample 100 high-delta intervals at predefined levels. Normalize delta by local volume, then record price progress over one, three, and ten intervals. Segment by location and volatility regime.
