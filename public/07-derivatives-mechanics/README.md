---
description: Understand the contract, price references, funding, margin, collateral, and liquidation before placing a derivatives order.
icon: file-contract
---

# Crypto Derivatives Mechanics

A precise entry price is useful only when the product mechanics are equally precise. Before trading, identify what is quoted, what settles P&L, which price triggers the stop, and which condition triggers liquidation.

{% hint style="danger" %}
Liquidation is not a substitute for a stop. Keep the planned stop reachable before liquidation under adverse mark-price movement, fees, funding, and maintenance-margin changes.
{% endhint %}

## Product specification card

Record these fields for every symbol and venue:

| Field | Required value |
|---|---|
| Product | Spot, linear perpetual, inverse perpetual, or dated future |
| Contract size | Base units or quote value per contract |
| Quote and settlement | Currency used for price, margin, fees, and P&L |
| Tick and quantity step | Smallest valid price and size increments |
| Index and mark | Construction method and current components |
| Stop trigger | Last, mark, or index price |
| Funding or expiry | Interval and formula, or settlement date and method |
| Margin mode | Isolated, cross, or portfolio |
| Initial and maintenance margin | Current tier and change conditions |
| Liquidation rule | Trigger, partial-liquidation process, and fees |

Continue with [Contract types](contract-types.md), [Price references and liquidation](price-liquidation.md), [Funding and basis](funding-basis.md), and [Margin and collateral](margin-collateral.md).
