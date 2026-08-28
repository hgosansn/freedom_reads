---
description: Freeze every entry model parameter before validation or live order placement.
icon: sheet-plastic
---

# Frozen Model Specification

The model pages define the logic and formulas. This sheet turns one selected variant into a versioned implementation. Complete it before collecting validation data. A blank, qualitative, or discretionary field means the model is not deployable.

## Identity and data

| Field | Frozen value |
|---|---|
| Model and variant | Exact course model plus entry variant |
| Version | Immutable identifier and effective date |
| Venue, symbol, product | Exact market and contract |
| Analysis frame | Profile session, timezone, anchor, and higher timeframe |
| Execution frame | Event interval or data aggregation used to classify triggers |
| Price increment | Tick size and rounding rule by order side |
| Quantity increment | Minimum size and round-down rule |
| Required feeds | Price, volume, profile, delta, CVD, open interest, or funding |

## State definitions

| Field | Frozen value |
|---|---|
| Context | Observable regime and location requirements |
| Authorization trigger | Exact event that permits order submission |
| Acceptance | Minimum time, closes, volume, and value behavior |
| Rejection | Maximum time beyond, re-entry, and response requirement |
| Retest | Eligible retest number, direction, depth, and maximum delay |
| Disqualifier | Conditions that prevent authorization |

## Order ticket

| Field | Frozen value |
|---|---|
| Entry formula | Reference `R`, signed offset `d`, and tick rounding |
| Order type | Passive limit, marketable limit, stop-market, or stop-limit |
| Time in force | Good-till-canceled, day, immediate-or-cancel, or venue equivalent |
| Post-only | Required, forbidden, or not applicable |
| Trigger source | Last, mark, or index price for conditional orders |
| Maximum chase | Normally zero for passive retest variants |
| Cancellation | Expiry, target-first, context change, or invalidation event |
| Partial fill | Minimum useful fill, timeout, and protection rule |

## Risk and exits

| Field | Frozen value |
|---|---|
| Structural invalidation | Observable thesis failure |
| Stop order | Type, trigger source, stop price, and optional limit price |
| Execution buffer | Formula for ticks, spread, and volatility |
| Size | Risk budget divided by estimated loss per unit, rounded down |
| Target 1 | First opposing auction objective and quantity fraction |
| Target 2 | External objective or trailing condition and quantity fraction |
| Management | Permitted transitions only; no unlisted discretion |

## Change control

Changing any decision field creates a new model version. Finish or formally abandon the old sample, record the reason without inspecting the new holdout, and validate the new version independently. Never pool results merely because both versions share a model name.

{% hint style="danger" %}
Do not optimize the offset, retest window, stop buffer, and acceptance rule independently on the same validation set. They are one joint specification.
{% endhint %}
