---
description: A rule-based reversal setup for failed attempts to auction beyond established value or range.
icon: rotate-left
---

# Failed Auction Reversal

The Failed Auction Reversal trades re-entry into a prior auction after an outside test fails to establish value. Entry follows confirmed failure; the first excursion supplies location only.

![Failed auction reversal sequence from outside test to rotation](../.gitbook/assets/diagrams/failed-auction.svg)

## Conditions

- A clear prior range, value edge, session extreme, or composite boundary
- An excursion outside that attracts breakout flow or stops
- Little time or volume developing outside
- Re-entry and hold inside the boundary
- Enough room to the next reference for positive expectancy

## Execution model

{% stepper %}
{% step %}
## Frame the boundary

Mark the exact zone, expected liquidity, POC, and opposite edge before price arrives.
{% endstep %}

{% step %}
## Observe failure

Require rejection, ineffective aggression, or absorption followed by a reclaim.
{% endstep %}

{% step %}
## Trigger

Enter on the reclaim close, a failed retest from inside, or an internal structure break away from the extreme.
{% endstep %}

{% step %}
## Define risk

Invalidate beyond the failed extreme or where renewed outside acceptance disproves the thesis. Target POC first, then the opposite value edge when rotation persists.
{% endstep %}
{% endstepper %}

## No-trade conditions

Skip when value is migrating through the boundary, correlated markets confirm discovery, event risk makes structure unreliable, or the first target cannot justify the stop.

{% hint style="warning" %}
The setup requires three separate observations: an attempted auction, failed outside acceptance, and flow consistent with continuation traders exiting. A touch of support or resistance satisfies none of them.
{% endhint %}

**Validation sample:** Collect at least 50 cases. Record boundary type, time and volume outside, entry model, initial risk, maximum favorable and adverse excursion, target reached, and rule adherence. Report results by regime instead of pooling all failures.
