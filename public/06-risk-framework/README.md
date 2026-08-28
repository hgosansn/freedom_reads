---
description: Define trade, portfolio, drawdown, and operational risk before selecting position size.
icon: shield-halved
---

# Risk Framework

Risk management decides how much uncertainty the account can survive. It begins
before position sizing and remains separate from confidence in any individual
trade.

{% hint style="danger" %}
Margin available is not risk capacity. An exchange may permit a position that
is much larger than the account can survive through normal volatility.
{% endhint %}

## Risk hierarchy

Apply limits from the account downward:

1. **Capital at risk:** funds that may be exposed to trading and venue failure.
2. **Drawdown limits:** thresholds that reduce or stop new exposure.
3. **Portfolio heat:** total loss if every active trade reaches its planned
   stop, adjusted for correlated scenarios.
4. **Session budget:** maximum realized and open loss allowed in one trading
   session.
5. **Trade budget:** maximum planned loss for one idea.
6. **Position size:** quantity derived from the trade budget and structural
   stop distance.

A lower layer cannot override a higher one. A valid entry is rejected when the
portfolio or session has no remaining risk capacity.

## Required policy

Write these values as account policy, not during a trade:

| Control | Definition |
|---|---|
| Trading capital | Capital segregated from living expenses and emergency funds |
| Base trade risk | Normal risk budget for one independent idea |
| Maximum trade risk | Hard cap including fees and stop slippage |
| Maximum portfolio heat | Aggregate planned loss across open positions |
| Maximum cluster heat | Aggregate planned loss for one correlated scenario |
| Session loss limit | Realized loss plus remaining open risk that halts entries |
| Drawdown thresholds | Equity declines that reduce size or stop trading |
| Venue exposure cap | Maximum capital held at one custodian or exchange |

Do not copy another trader's percentages. Set limits from personal loss
tolerance, strategy drawdown evidence, liquidity, and the possibility that a
stop or venue fails.

## Module pages

- [Position sizing](position-sizing.md) converts structural invalidation into
  quantity.
- [Portfolio heat](portfolio-heat.md) controls simultaneous and correlated
  exposure.
- [Drawdown controls](drawdown-controls.md) defines automatic size reduction
  and trading halts.
- [Operational and counterparty risk](operational-counterparty-risk.md) covers
  failures outside the chart.

The CFTC warns that leverage amplifies crypto futures gains and losses and can
produce losses beyond initial funds. It also highlights theft and limited
recourse as material risks ([CFTC customer
advisory](https://www.cftc.gov/LearnAndProtect/AdvisoriesAndArticles/understand_risks_of_virtual_currency.html)).
