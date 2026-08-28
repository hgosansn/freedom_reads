---
description: Calculate quantity from account risk, structural invalidation, fees, and expected stop slippage.
icon: calculator
---

# Position sizing

Position size is the output of a risk decision. Define invalidation first,
estimate the loss per unit, then round quantity down to the venue's permitted
step.

## Linear spot and perpetual contracts

Let:

- `B` = maximum quote-currency loss budget
- `E` = expected average entry price
- `S` = expected average stop-fill price
- `f_entry` and `f_exit` = fee rates
- `s_stop` = expected adverse stop slippage per base unit

For a long position:

`loss_per_unit = (E - S) + (E × f_entry) + (S × f_exit) + s_stop`

`base_quantity = floor_to_size_step(B / loss_per_unit)`

`notional = base_quantity × E`

For a short, replace `(E - S)` with `(S - E)`. Use absolute loss terms so the
denominator remains positive.

### Example

Suppose `B = 100 USDT`, `E = 50,000`, expected stop fill `S = 49,500`, entry and
exit fees are each `0.05%`, and expected stop slippage is `25 USDT` per BTC.

- Price loss per BTC: `500`
- Entry fee per BTC: `25`
- Exit fee per BTC: `24.75`
- Stop slippage per BTC: `25`
- Total estimated loss per BTC: `574.75`
- Quantity before rounding: `100 / 574.75 = 0.17399 BTC`

Round down to the venue size step. Recalculate if the entry or stop changes.

## Percentage shortcut

When fees and slippage are temporarily excluded:

`notional = risk budget / absolute stop distance %`

If risk is `100 USDT` and stop distance is `2%`, notional is `5,000 USDT`.
This shortcut is a planning estimate, not a final order size.

## Contract-specific products

Inverse and coin-margined contracts have nonlinear quote-currency P&L and may
use contract multipliers. Calculate loss with the venue's published formula or
order preview, then solve for the largest whole contract count below `B`.

## Size constraints

Reduce the calculated quantity when:

- market depth cannot absorb the planned stop without excessive slippage;
- the position increases correlated cluster heat;
- funding or borrow cost is material to the holding period;
- collateral can lose value at the same time as the position;
- the account is under a drawdown throttle.

{% hint style="warning" %}
Never round quantity up. If the minimum order size exceeds the risk budget,
reject the trade.
{% endhint %}

CME educational guidance similarly begins with the stop location, dollar loss
per contract, and the account's permitted trade risk rather than maximum margin
availability ([CME position sizing](https://www.cmegroup.com/education/courses/trade-and-risk-management/proper-position-size.hideSubnav.educationIframe.html.html?hideAddThisExt=y&hideFooter=y&hideHeader=y&hideRightRail=y)).
