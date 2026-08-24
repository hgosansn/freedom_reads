---
description: Place stops where market evidence disproves the trade thesis and size exposure from that distance.
icon: ban
---

# Invalidation

Invalidation is the observable condition that makes the trade idea wrong. A stop is the order used to enforce it. Good risk design begins with invalidation, then derives size.

## Structural placement

Place invalidation beyond the point where the expected auction behavior no longer holds: renewed acceptance beyond a failed-auction extreme, return into an accepted breakout range, or break of the swing that defines a trend pullback.

Allow for normal noise, spread, and venue volatility. A stop exactly on a well-known high or low may trigger during a test without invalidating the idea. Arbitrarily widening it after entry, however, changes the trade.

## Position sizing

`position size = account risk / stop distance`

For linear USDT-settled contracts, if account risk is 100 USDT and entry-to-stop distance is 2%, notional size is approximately 5,000 USDT before fees and slippage. Contract specifications differ; verify inverse or coin-margined products separately.

Include trading fees, expected slippage, funding exposure, and correlation with open positions. Three altcoin longs may represent one concentrated crypto-beta risk.

{% hint style="warning" %}
Leverage changes margin usage and liquidation distance; it does not reduce the trade's underlying price risk. Keep liquidation comfortably beyond the planned stop.
{% endhint %}

**Drill:** Write the invalidation sentence before calculating size for every simulated trade. If it cannot be stated objectively, the trade is not ready.
