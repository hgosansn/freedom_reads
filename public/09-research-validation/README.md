---
description: Turn trading observations into falsifiable, reproducible, and forward-tested entry models.
icon: flask
---

# Research and Validation

A chart pattern is not evidence until its definition is frozen before outcomes are revealed. This module separates exploration, estimation, validation, and live monitoring so that attractive hindsight does not become a limit order.

## Evidence ladder

1. **Observation:** describe a recurring event without performance claims.
2. **Hypothesis:** state population, trigger, comparator, outcome, and horizon.
3. **Pilot:** test data capture and classification, not profitability.
4. **In-sample estimate:** freeze definitions and estimate distributions.
5. **Out-of-sample validation:** evaluate once on untouched data.
6. **Forward simulation:** run the complete decision and order process in time order.
7. **Limited deployment:** trade at reduced risk with drift monitoring.

Read [Experimental design](experimental-design.md), [Metrics and uncertainty](metrics-uncertainty.md), [Bias controls](bias-controls.md), and [Forward validation](forward-validation.md).

{% hint style="warning" %}
A sample count is not proof. Define the sampling frame, stopping rule, exclusions, and decision threshold before collecting the validation set.
{% endhint %}
