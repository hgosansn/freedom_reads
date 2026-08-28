---
description: Detect look-ahead, survivorship, selection, overfitting, and multiple-testing bias.
icon: filter-circle-xmark
---

# Bias controls

| Bias | Typical leak | Control |
|---|---|---|
| Look-ahead | Final profile values used before session close | Reconstruct only values known at the timestamp |
| Survivorship | Testing only currently listed tokens | Use point-in-time symbol and delisting records |
| Selection | Saving memorable clean setups | Enumerate every eligible event from a frozen scan |
| Execution | Assuming a touch equals a fill | Model queue, spread, partial fills, and cancellation |
| Overlap | Counting correlated signals independently | Group by shared event or apply an exclusion window |
| Overfitting | Repeatedly tuning thresholds on the same history | Separate train, validation, and final holdout data |
| Multiple testing | Reporting only the best of many variants | Log every trial and adjust confidence claims |
| Regime leakage | Random split mixes one event across sets | Use chronological, embargoed splits |

Record every parameter tried, including discarded variants. The final model must be evaluated against the number of research choices that produced it, not as if it were the only hypothesis considered.

{% hint style="danger" %}
An out-of-sample set becomes in-sample immediately after its result influences a change. Create a new untouched set after any revision.
{% endhint %}
