---
description: Distinguish spot, linear, inverse, perpetual, and dated contracts by their cash flows.
icon: arrows-left-right-to-line
---

# Contract types

| Product | Position unit | P&L and settlement | Carry or expiry |
|---|---|---|---|
| Spot | Base asset | Base asset against quote asset | No funding; borrow cost if margined |
| Linear perpetual | Usually base quantity | Linear in quote or stablecoin collateral | Funding; no expiry |
| Inverse perpetual | Usually quote-value contracts | Nonlinear P&L paid in the base asset | Funding; no expiry |
| Dated future | Venue-specific contracts | Venue-specific settlement asset | Expires and settles; basis converges toward spot |

For a linear long with base quantity `q`, entry `E`, and exit `X`, gross quote P&L is `q × (X - E)`. For an inverse USD contract with contract value `C`, gross base-asset P&L is commonly `C × (1/E - 1/X)` for a long. Verify the venue formula and sign convention before sizing.

## Selection rule

Choose the product whose loss can be calculated in the account's risk currency. Coin collateral creates wrong-way risk when a long position loses while its collateral also falls in value. A nominally equal position can therefore have a different account-level loss across contract types.

{% hint style="warning" %}
Never transfer a quantity from a linear contract to an inverse contract without recalculating contract value, P&L, fees, and liquidation.
{% endhint %}
