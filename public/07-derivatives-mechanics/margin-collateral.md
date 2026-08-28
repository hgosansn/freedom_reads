---
description: Control isolated, cross, and portfolio margin plus collateral concentration.
icon: vault
---

# Margin and collateral

Initial margin opens a position. Maintenance margin is the minimum equity condition needed to avoid forced reduction. Both can depend on risk tiers, position size, other positions, open orders, and venue policy.

| Mode | Risk boundary | Main limitation |
|---|---|---|
| Isolated | Margin assigned to one position | Added margin increases the amount exposed |
| Cross | Eligible account equity supports positions together | One loss can consume collateral supporting other trades |
| Portfolio | Scenario model offsets selected risks | Model, correlation, and eligibility can change under stress |

## Collateral haircut

If collateral amount is `Q`, market price is `P`, and venue collateral ratio is `h`:

`recognized collateral value = Q × P × h`

Stress both `P` and `h`. A stablecoin or token can lose market value while the venue reduces its collateral ratio.

## Pre-entry margin test

- Model the stop loss in account currency, not displayed margin return.
- Keep liquidation beyond the stop after mark-price stress and costs.
- Include other positions and open orders in cross-margin consumption.
- Record current maintenance tier and the next tier boundary.
- Reject a trade whose safety depends on adding emergency margin.

Margin rules are venue-specific and mutable. Recheck the live contract specification before every deployment or parameter change.
