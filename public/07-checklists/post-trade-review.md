---
description: Review decisions separately from outcomes and convert trades into reliable performance data.
icon: magnifying-glass-chart
---

# Post-trade review

Review the decision process before judging the profit or loss. Outcome bias rewards bad trades that win and rejects good trades that lose.

## Capture

- [ ] Save screenshots from before entry, at entry, during management, and after exit.
- [ ] Record instrument, venue, timestamps, direction, size, leverage, fees, funding, slippage, and realized P&L in R.
- [ ] Tag regime, location, setup, entry model, and market session.
- [ ] Record maximum favorable excursion (MFE) and maximum adverse excursion (MAE).

## Grade the process

Score each dimension independently from 0 to 2:

| Dimension | 0 | 1 | 2 |
|---|---|---|---|
| Context | Misread/ignored | Ambiguous | Correct and explicit |
| Setup | Not present | Partial | All criteria met |
| Risk | Violated | Minor deviation | Fully planned |
| Execution | Impulsive | Imperfect | Rule-compliant |
| Management | Emotion-led | Mixed | Model followed |

Then classify the trade: **good win, good loss, bad win, or bad loss**. Process quality determines the first word; financial outcome determines the second.

## Learn without overfitting

- [ ] What information was available at the decision point?
- [ ] What did price do that confirmed or contradicted the thesis?
- [ ] Was the mistake analytical, executional, or behavioral?
- [ ] Is it a repeated pattern or a single event?
- [ ] What one behavior will change next time?

{% hint style="info" %}
Change an entry-model rule only after the predefined sample closes. A single
loss has no authority to rewrite the model.
{% endhint %}

## Weekly review

Aggregate results by setup and regime. Track expectancy, win rate, average win/loss, MFE/MAE, rule adherence, fees, and time of day. Retire or modify a setup based on process-clean samples, not blended results from discretionary exceptions.
