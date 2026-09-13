# OmniPizza Food Delivery — Exploratory Testing

## 1. Objective

Exploratory testing was performed to investigate application behavior outside the predefined manual test cases.

The focus was on navigation, browser behavior, session state, cart consistency, and checkout behavior.

---

## 2. Exploratory Test Summary

| ID     | Scenario                     | Result |
| ------ | ---------------------------- | ------ |
| ET-001 | Refresh during checkout      | PASS   |
| ET-002 | Browser Back during checkout | PASS   |
| ET-003 | Multiple browser tabs        | PASS   |

**Total:** 3
**Passed:** 3
**Failed:** 0

---

## ET-001 — Refresh During Checkout

### Objective

Verify application behavior when the browser is refreshed during checkout.

### Steps

1. Login with a valid user.
2. Add a pizza to the cart.
3. Proceed to checkout.
4. Enter checkout information.
5. Refresh the browser.

### Expected Result

The application should handle the refresh without crashing or corrupting the cart/order state.

### Actual Result

The application remained functional. Unsaved checkout information was cleared after refresh.

### Result

**PASS**

### Observation

Checkout information was not retained after refresh. This was recorded as an observation and not confirmed as a defect.

---

## ET-002 — Browser Back During Checkout

### Objective

Verify application behavior when using the browser Back button during checkout.

### Steps

1. Login with a valid user.
2. Add a pizza to the cart.
3. Proceed to checkout.
4. Use the browser Back button.
5. Navigate forward again and verify the cart.

### Expected Result

The application should navigate correctly without crashing or corrupting cart information.

### Actual Result

The application remained functional and the cart quantity/information remained correct.

Checkout information was not retained after navigating away.

### Result

**PASS**

### Observation

Checkout information was cleared after navigation. No confirmed functional defect was identified.

---

## ET-003 — Multiple Browser Tabs

### Objective

Verify whether application state remains consistent when the same account is opened in multiple browser tabs.

### Steps

1. Login using a valid account.
2. Open the application in another browser tab.
3. Add or modify cart items.
4. Refresh the tabs.
5. Compare the cart state.

### Expected Result

The application should remain stable and should not produce unexpected errors or corrupted cart data.

### Actual Result

The application remained functional. Cart quantity and information remained consistent after refreshing.

### Result

**PASS**

---

## 3. Exploratory Testing Conclusion

The exploratory testing scenarios completed during this project did not identify any confirmed unexpected functional defects.

Two observations were recorded regarding checkout information being cleared after browser refresh/navigation.

These observations were not classified as defects because the expected requirement for retaining unsaved checkout information was not established.
