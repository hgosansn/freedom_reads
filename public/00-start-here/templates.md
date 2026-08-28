---
description: Copy consistent pre-market, order, and review records for simulation and live use.
icon: clipboard
---

# Planning and Journal Templates

## Pre-market plan

```text
Date/session/timezone:
Venue/symbol/product:
Data and venue checks:
External regime and invalidation:
Value, balance, HVN/LVN, and liquidity references:
Scheduled event windows:
Allowed model versions:
If/then branches:
Session and portfolio risk available:
```

## Order ticket

```text
Decision timestamp:
Model/version/variant:
Context and location evidence:
Authorization trigger:
Entry formula and final price:
Order type/TIF/post-only/trigger source:
Structural invalidation and stop order:
Expected stop fill and loss per unit:
Risk budget/calculated quantity/final quantity:
Targets and management transitions:
Cancellation and partial-fill rules:
```

## Post-trade or non-fill record

```text
Order lifecycle and timestamps:
Average fill, fees, funding, and slippage:
Exit reason and net R:
MAE/MFE and holding time:
Rule adherence: yes/no with evidence
Data or operational defects:
Valid opportunity but no fill: yes/no
Screenshot/data snapshot locations:
One process correction, owner, and due date:
Model change proposed: yes/no (new version required)
```
