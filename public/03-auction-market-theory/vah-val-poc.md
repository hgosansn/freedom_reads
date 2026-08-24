---
description: Apply value-area high, value-area low, and point of control as auction references rather than automatic signals.
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

A naked POC—one not revisited in later sessions—is a contextual reference, not a promise that price must return. Strong imbalance can leave many behind.

| Observation | Implication to test |
|---|---|
| Stable POC, overlapping value | Balanced trade persists |
| POC migrating with price | Directional acceptance strengthens |
| Price extends, POC does not follow | Move may lack developing acceptance |

{% hint style="warning" %}
Profile references vary by venue and session definition. Record the exchange, instrument, and profile window in every review.
{% endhint %}

**Drill:** For 20 prior-day profiles, record first touch of VAH and VAL, the response, and whether price reached POC before invalidation.
