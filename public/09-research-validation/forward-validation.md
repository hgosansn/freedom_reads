---
description: Promote, monitor, pause, and retire models with explicit evidence gates.
icon: arrow-trend-up
---

# Forward validation

Forward simulation must reproduce the information, latency, order types, and decision deadlines of live execution. Log signals at their decision time, including valid orders that never fill.

## Event record

- timestamp, venue, symbol, product, and session;
- frozen model version and parameter hash;
- regime, location, trigger, invalidation, entry, stop, and targets;
- visible data snapshot and unavailable inputs;
- order lifecycle, partial fills, fees, funding, and slippage;
- MAE, MFE, exit reason, rule adherence, and operational defects.

## Promotion gate

Promote only when the untouched and forward samples both meet the predeclared minimum effect, cost, drawdown, and uncertainty requirements. Begin with reduced risk and a maximum exposure cap.

Pause automatically when data integrity fails, live costs exceed the validated band, classification agreement degrades, drawdown crosses policy, or the model's rolling outcome distribution breaches its monitoring threshold.

Version every rule change. Do not combine results across versions unless the change was declared immaterial before viewing outcomes.
