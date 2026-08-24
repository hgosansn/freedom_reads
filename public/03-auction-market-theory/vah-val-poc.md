---
description: Apply value-area high, value-area low, and point of control as references within a defined auction.
icon: lines-leaning
---

# VAH / VAL / POC

**VAH** is the upper boundary of the chosen value area, **VAL** is the lower boundary, and **POC** is the price with the greatest traded volume in that profile. Together they summarize the auction's distribution.

## Functional roles

- **VAH / VAL:** decision zones between accepted value and lower-volume territory.
- **POC:** the auction's most active price; often a magnet in balance and a trailing reference when value migrates.
- **Developing POC:** reveals where current-session activity is concentrating, but it can move sharply before the profile closes.

## Scenario logic

At VAH, rejection back into value can target POC and potentially VAL. Acceptance above VAH invalidates the rotational premise and can initiate discovery. The inverse applies at VAL.

A naked POC is a prior point of control that later sessions have not revisited. It remains a contextual reference; directional auctions can leave several untouched without reverting.

| Observation | Implication to test |
|---|---|
| Stable POC, overlapping value | Balanced trade persists |
| POC migrating with price | Directional acceptance strengthens |
| Price extends, POC does not follow | Test for thin discovery or failed extension |

{% hint style="warning" %}
Profile references vary by venue and session definition. Record the exchange, instrument, and profile window in every review.
{% endhint %}

**Study protocol:** For 50 prior-day profiles, record the first touch of VAH and VAL, opening location, approach velocity, response, MAE, and whether POC traded before invalidation. Separate trend and balance sessions.
