---
description: A precise library for selecting, pricing, managing, and testing limit-order entry models.
icon: crosshairs
---

# Entry Model Library

An entry model is a complete decision rule, not a chart shape. It defines the
market state, location, evidence required before entry, order price,
invalidation, cancellation conditions, and target path. If any field is
missing, the model is not executable or testable.

{% hint style="warning" %}
There is no universally correct limit price. A limit order controls the worst
price at which it may execute; it does not guarantee execution, a complete
fill, or a profitable trade. Calibrate every buffer and timing rule to the
instrument, venue, session, and timeframe with replay and live fill data.
{% endhint %}

## Model map

| Model | Regime | Directional idea | Default order deployment |
|---|---|---|---|
| [Balance-edge fade](balance-edge-fade.md) | Stable balance | Responsive trade back toward value | Resting limit allowed after balance qualification |
| [Failed Auction Reversal](failed-auction-reversal.md) | Failed discovery | Re-entry and rotation through the old auction | Limit only after reclaim or failed retest |
| [Breakout Acceptance](breakout-acceptance.md) | Balance to imbalance | Retest of a newly accepted area | Limit after acceptance; never before the break |
| [Trend Pullback](trend-pullback.md) | Directional auction | Corrective return to trend support or resistance | Limit at a planned zone or after a continuation trigger |
| [LVN rejection / reclaim](lvn-rejection-reclaim.md) | Distribution edge | Reject a low-volume corridor and return to distribution | Limit after rejection or reclaim |

Long examples are shown throughout. Invert price relationships and order sides
for shorts; do not invert the sequence of evidence.

## The model contract

Write these fields before placing an order:

1. **Regime:** balance, trend, or transition.
2. **Reference:** one exact price or a bounded zone derived before arrival.
3. **Setup:** what price must do at the reference.
4. **Trigger:** the observable event that authorizes exposure.
5. **Limit:** the price and order instructions sent to the venue.
6. **Invalidation:** the market event that disproves the thesis.
7. **Cancellation:** when an unfilled order is no longer valid.
8. **Targets:** the first opposing reference and any continuation objective.

Setup, trigger, and fill are different events. A setup can complete without a
retest; a valid limit can remain unfilled. Record both outcomes rather than
pretending every historical touch produced a fill.

## Limit-order placement protocol

Let `R` be the structural reference, `d` the tested entry offset, and `tick` the
venue tick size.

- Long support/retest: `L = floor_to_tick(R + d)`
- Short resistance/retest: `L = ceil_to_tick(R - d)`

`d` is signed toward the expected approach so the order can fill before the
exact reference when that behavior has been validated. Define it in ticks or as
a fixed fraction of the setup timeframe's ATR; do not change the method trade
by trade. A zero offset is valid when tests support it.

For a zone `[Z_low, Z_high]`, select one rule in advance: proximal edge,
midpoint, distal edge, or a fixed ladder. “Somewhere in the zone” is not a
rule. A ladder must assign size and invalidation to the whole position before
the first child order fills.

### Three deployment modes

**Resting limit:** placed before price reaches the reference. Use only when
location itself authorizes the trade, as in a qualified balance fade. It gains
queue priority but accepts the highest adverse-selection risk.

**Triggered passive limit:** placed only after confirmation, normally at the
retest price. This is the default for failed auctions, accepted breakouts, and
LVN reclaims. It can miss trades that do not retest.

**Marketable limit:** crosses the spread with a worst acceptable price. It
prioritizes immediacy while capping price, but can partially fill or not fill if
the book moves through the limit. It is not a substitute for a market order.

## Venue mechanics that change the result

Coinbase's official rules state that a limit order fills only at its specified
price or better. They also state that a non-post-only limit may act as maker,
taker, or both, while post-only instructions reject an order that would take
liquidity ([Coinbase Markets Trading
Rules](https://www.coinbase.com/legal/trading_rules)). Order matching uses
price-time priority, so an order at the correct chart price can remain behind
existing size in the queue ([Coinbase Exchange trading
concepts](https://docs.cdp.coinbase.com/exchange/concepts/trading)).

Queue position is not a detail. Research finds that orders deeper in a queue
have lower execution probability and greater adverse-selection exposure
([Yueshen, 2025](https://doi.org/10.1287/mnsc.2023.03371)). Crypto execution
research likewise treats unfilled limits as an opportunity cost, alongside
fees and price impact ([Bundi, Wei, and Khashanah,
2024](https://doi.org/10.1007/s42521-023-00103-y)).

For every order, record:

- venue, product, tick size, and minimum size;
- limit price, size, time in force, and post-only state;
- queue depth ahead if available;
- partial fills, average fill, maker/taker fees, and slippage;
- trigger-to-order latency and order-to-fill time;
- reason and timestamp for cancellation.

## Global cancellation rules

Cancel an unfilled limit when any of the following occurs:

- the model's invalidation condition prints before entry;
- the qualifying regime changes;
- price reaches the first target without filling the entry;
- the trigger expires under the model's time rule;
- scheduled event risk begins and the model excludes it;
- spread, depth, or correlated-market behavior violates the execution filter.

Never widen the entry or chase price merely because a valid order did not fill.
Non-fill is a model outcome, not permission to improvise.

## Validation standard

Backtests using candles cannot prove a passive fill when a bar merely touches
the limit. Use order-book or trade data where possible; otherwise classify
touches as **potential fills** and apply conservative queue and slippage
assumptions. Evaluate setup expectancy and execution expectancy separately.

The minimum journal schema is:

`model, regime, reference, trigger, limit, fill state, average fill, invalidation, MAE, MFE, target, fees, cancellation reason`

Keep parameters frozen for the in-sample set, then validate them on unseen data
and in forward simulation before risking capital.
