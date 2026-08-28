---
description: Plan for exchange, custody, collateral, data, connectivity, and protective-order failure.
icon: building-shield
---

# Operational and counterparty risk

A correct market thesis can still lose through venue or infrastructure failure.
Treat these risks as part of total exposure rather than rare exceptions.

## Failure map

| Risk | Example | Control |
|---|---|---|
| Venue | Insolvency, withdrawal halt, matching pause | Venue capital cap; withdrawal test; multiple routes |
| Custody | Compromised credentials or device | Hardware security keys; withdrawal allowlist; separate storage |
| Collateral | Stablecoin depeg or token haircut | Collateral diversification; conservative collateral value |
| Data | Frozen chart, missing trades, bad CVD | Independent reference feed; stale-data alarm |
| Connectivity | Local internet or API outage | Backup connection; server-side protection; manual venue access |
| Order state | Rejected, canceled, or partially filled stop | Order acknowledgment monitoring; fill reconciliation |
| Liquidation | Stop fails before maintenance margin | Liquidation kept beyond stop under stress assumptions |

## Venue exposure policy

Define the maximum account equity held on one venue. Keep only the collateral
and operational buffer needed for the approved strategy when withdrawal and
custody conditions permit.

Venue diversification is not complete when several venues depend on the same
stablecoin, custodian, cloud region, or banking route. Record shared dependencies.

## Protective-order checklist

- Confirm trigger source: mark, index, or last price.
- Confirm stop-market versus stop-limit behavior.
- Confirm reduce-only, position side, and margin mode.
- Confirm the order is acknowledged by the venue.
- Confirm partial fills leave the correct remaining protection.
- Test the emergency close path before it is needed.
- Define who or what acts when monitoring is unavailable.

## Stress reserve

Ordinary position sizing estimates expected stop execution. Maintain additional
capital and policy headroom for gaps, slippage, funding, collateral haircuts,
and positions that cannot be closed immediately.

{% hint style="danger" %}
An order visible in a local interface is not necessarily live at the venue.
Reconcile open positions and protective orders against the venue's confirmed
state.
{% endhint %}
