# SauceDemo — Manual QA Functional Testing

## Project overview
Manual functional testing of the [SauceDemo](https://www.saucedemo.com/) demonstration e-commerce application using Google Chrome.

**Scope:** Login validation, cart operations, required checkout fields, pricing consistency, and end-to-end purchase confirmation.

## Test approach
Executed positive and negative scenarios using `standard_user` and the demonstration locked-out account. Compared observed results with expected application behavior and documented reproducibility where applicable.

## Key verified scenarios
- Valid user can sign in; invalid or missing credentials are rejected with relevant messages.
- Adding three distinct products updates the cart badge sequentially to 1, 2, and 3.
- Removing one item leaves the two expected products at quantity 1 each and updates the badge to 2.
- Checkout blocks progress without a first name and displays `Error: First Name is required`.
- Checkout overview shows Sauce Labs Bike Light and Sauce Labs Bolt T-Shirt at quantity 1 each; subtotal $25.98 + tax $2.08 = total $28.06.
- Completing the order displays `Thank you for your order!`.

## Files
- [Test-Cases.xlsx](Test-Cases.xlsx) — Scenario-level cases, execution observations, and outcomes.
- [Test-Execution-Report.md](Test-Execution-Report.md) — Scope, results, limitations, and release recommendation.
- [Defect-Log.md](Defect-Log.md) — Unexpected behavior and retest history; no confirmed reproducible defects.

## Limitations
This is a focused manual test sample, not exhaustive product certification. Cross-browser, accessibility, performance, security, and broad edge-case coverage were not performed. Some earlier observations were not fully documented and are identified accordingly.
