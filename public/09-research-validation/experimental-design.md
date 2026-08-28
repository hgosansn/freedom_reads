---
description: Pre-register hypotheses, observations, exclusions, and stopping rules before testing an entry model.
icon: diagram-project
---

# Experimental design

## Pre-registration card

| Field | Frozen definition |
|---|---|
| Population | Symbols, venues, sessions, dates, and regimes eligible for sampling |
| Unit | One break, touch, session, or independent trade opportunity |
| Predictor | Information available at the decision timestamp |
| Comparator | Baseline rule, random timing, or alternative model |
| Outcome | Fill rate, MAE, MFE, net return, or invalidation within a fixed horizon |
| Costs | Fees, spread, slippage, funding, borrow, and missed fills |
| Exclusions | Data defects and operational cases defined before outcomes |
| Dependence | Rule for overlapping signals and clustered market events |
| Stopping rule | Fixed observations or precision-based interval target |
| Decision rule | Minimum effect and uncertainty bound required for promotion |

Use chronological splits. Parameter selection belongs only in the training segment. Reserve the validation segment until every definition and transformation is frozen.

## Sample-size rule

Choose either:

- a fixed count justified by the minimum economically useful effect and desired uncertainty;
- a precision target, such as continuing until a confidence interval for fill rate or expectancy is narrower than a predeclared width.

If dependence is strong, count clusters or sessions rather than treating every signal as independent. Never stop because the equity curve looks good.
