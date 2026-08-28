---
description: Demonstrate classification, calculation, execution, and review competence before deployment.
icon: graduation-cap
---

# Assessment Rubric

Score each competency from `0` to `3`:

- `0`: absent or retrospective;
- `1`: partially defined and inconsistently reproducible;
- `2`: correct with minor omissions that do not change the decision;
- `3`: complete, timestamped, reproducible, and correctly calculated.

| Competency | Evidence |
|---|---|
| Context | Classifies regime and external structure without future data |
| Location | Constructs profile and liquidity references from frozen anchors |
| Behavior | Distinguishes acceptance, rejection, absorption, and exhaustion |
| Model | Completes every Frozen Model Specification field |
| Order | Prices and rounds entry, stop, targets, and quantity correctly |
| Risk | Applies trade, cluster, session, drawdown, and venue limits |
| Research | Uses chronological splits, costs, uncertainty, and bias controls |
| Review | Logs fills, non-fills, errors, MAE, MFE, and version changes |

## Graduation gate

Require at least `2` in every category and `3` in Order and Risk. Then pass a forward-simulation block with no critical rule breach. A critical breach includes exceeding risk, moving invalidation to avoid a stop, entering an unauthorized model, or omitting protective-order verification.

Any critical breach resets the relevant simulation block after corrective review. Profit does not offset a process breach.
