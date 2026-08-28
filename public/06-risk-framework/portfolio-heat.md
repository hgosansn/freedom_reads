---
description: Limit aggregate loss across open trades and correlated market scenarios.
icon: temperature-half
---

# Portfolio heat

Portfolio heat is the planned loss if every active position reaches its current
protective stop.

`raw heat = Σ planned stop loss for each open position`

Divide by current account equity to express heat as a percentage. Include
unrealized loss already incurred and fees expected at every stop.

## Correlated scenario heat

Raw heat understates risk when positions express the same underlying idea. BTC,
ETH, and several altcoin longs may all fail during one broad crypto selloff.

Group positions by shared failure scenario:

- broad crypto beta;
- one sector or token ecosystem;
- one collateral asset or stablecoin;
- one exchange or custodian;
- one macro event;
- one directional volatility exposure.

`cluster heat = Σ planned losses inside the shared scenario`

Use the greater of statistical correlation evidence and conservative scenario
judgment. Recent low correlation does not make two positions independent during
stress.

## Incremental risk test

Before adding a position, calculate:

1. current raw heat;
2. heat after the new trade;
3. current heat in the affected cluster;
4. cluster heat after the new trade;
5. venue and collateral concentration after the new trade.

Reject or reduce the trade if any policy limit is exceeded. Do not count a
correlated hedge at full value unless its behavior, liquidity, and execution
during stress have been validated.

## Example

An account has three planned losses:

| Position | Planned loss | Cluster |
|---|---:|---|
| BTC long | 100 USDT | Crypto beta |
| ETH long | 80 USDT | Crypto beta |
| SOL long | 60 USDT | Crypto beta |

Raw heat is `240 USDT`. Crypto-beta cluster heat is also `240 USDT`, not three
independent bets. A fourth altcoin long must be evaluated as additional exposure
to the same failure event.

{% hint style="danger" %}
Stops do not cap portfolio loss during gaps, liquidation cascades, exchange
failure, or unavailable liquidity. Policy limits need a separate catastrophe
allowance beyond ordinary stop estimates.
{% endhint %}
