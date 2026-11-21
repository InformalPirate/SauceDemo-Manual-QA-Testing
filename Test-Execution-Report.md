# Test Execution Report — SauceDemo

**Application:** https://www.saucedemo.com/  
**Environment:** Google Chrome (manual browser testing)  
**Testing type:** Functional, negative validation, regression-style retest, and end-to-end checkout

## Scope
Login authentication and required-field errors; product addition and removal; cart badge and item quantities; checkout first-name validation; checkout calculations; order confirmation.

## Execution summary
The documented scenarios generally met their expected results. Positive login and invalid-credential/required-field checks behaved as expected. A three-product cart showed badges 1, 2, and 3, with all products at quantity 1. Removing the backpack left Bike Light and Bolt T-Shirt at quantity 1 each and badge 2. Missing first name prevented checkout progression and produced `Error: First Name is required`.

The completed purchase included:

| Checkout detail | Observed |
|---|---:|
| Sauce Labs Bike Light | Qty 1 |
| Sauce Labs Bolt T-Shirt | Qty 1 |
| Item subtotal | $25.98 |
| Tax | $2.08 |
| Total | $28.06 |

**Calculation check:** $25.98 + $2.08 = $28.06. The final screen displayed `Thank you for your order!`.

## Unexpected behavior / retest
An initial locked-out account test reportedly showed a generic credential mismatch. Two subsequent tests in Chrome Incognito returned the expected locked-out message. The initial observation was not reproducible; it is tracked as an observation rather than a confirmed defect.

## Release assessment
The tested workflows support a **limited release recommendation for the tested scope**, subject to the team's broader quality gates. This work alone does not establish readiness for an unrestricted production release.

## Limitations
Only a subset of user journeys was covered. Cross-browser, accessibility, security, performance, mobile/responsive behavior, and comprehensive boundary testing were outside scope. Results are based on recorded manual observations rather than independent automated evidence.
