---
description: Include perpetual funding and futures basis in trade selection and holding-period risk.
icon: percent
---

# Funding and basis

`basis = derivative price - reference spot price`

`annualized basis ≈ (basis / spot price) × (365 / days to expiry)`

Positive basis is commonly called contango and negative basis backwardation. For dated futures, basis normally converges toward zero at settlement, but the path can be volatile.

Perpetuals use periodic funding to encourage alignment with spot. A common cash-flow form is:

`funding cash flow = position value × funding rate`

The venue determines the rate, sign, position-value reference, interval, caps, and timestamp eligibility. Bybit states that funding is exchanged between position holders and only applies to positions held at the funding time ([funding calculation](https://www.bybit.com/en/help-center/article/Funding-fee-calculation)).

## Order-planning rule

Estimate all funding events inside the maximum holding window. Record the current rate, a stressed rate, next timestamp, and sign. Funding can change after entry, so it is a scenario cost, not a fixed fee.

Do not enter solely because funding is extreme. Extreme funding can persist, and the price loss required to realize convergence can exceed the payment received.
