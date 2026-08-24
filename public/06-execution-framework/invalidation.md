---
description: Place stops where market evidence disproves the trade thesis and size exposure from that distance.
icon: ban
---

# Invalidation

Invalidation is the observable condition that makes the trade idea wrong. A stop is the order used to enforce it. Good risk design begins with invalidation, then derives size.

## Structural placement

Place invalidation beyond the point where the expected auction behavior no longer holds: renewed acceptance beyond a failed-auction extreme, return into an accepted breakout range, or break of the swing that defines a trend pullback.

Add a tested execution buffer for spread, tick size, and venue volatility beyond structural invalidation. Placing the stop directly on a public extreme exposes it to an ordinary test. Widening after entry creates an unplanned risk profile.

## Position sizing

`position size = account risk / stop distance`

For linear USDT-settled contracts, if account risk is 100 USDT and entry-to-stop distance is 2%, notional size is approximately 5,000 USDT before fees and slippage. Contract specifications differ; verify inverse or coin-margined products separately.

Include trading fees, expected slippage, funding exposure, and correlation with open positions. Treat several altcoin longs driven by the same BTC beta as one concentrated factor exposure.

{% hint style="warning" %}
Leverage changes margin usage and liquidation distance; it does not reduce the trade's underlying price risk. Keep liquidation comfortably beyond the planned stop.
{% endhint %}

**Control:** Write the invalidation condition before calculating size. Reject the order if the condition cannot be classified from observable price, profile, or flow data.
