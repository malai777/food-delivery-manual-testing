# OmniPizza Food Delivery — Manual Test Cases

## Test Case Summary

**Total Test Cases:** 20
**Executed:** 20
**Passed:** 20
**Failed:** 0
**Pass Rate:** 100%

---

## Authentication & Login

| ID     | Test Case                              | Expected Result                             | Status |
| ------ | -------------------------------------- | ------------------------------------------- | ------ |
| TC-001 | Login with valid username and password | User should successfully log in             | PASS   |
| TC-002 | Login with invalid username            | Appropriate login error should be displayed | PASS   |
| TC-003 | Login with invalid password            | Appropriate login error should be displayed | PASS   |
| TC-004 | Login with empty username              | Validation/error should be displayed        | PASS   |
| TC-005 | Login with empty password              | Validation/error should be displayed        | PASS   |

---

## Pizza & Menu

| ID     | Test Case                             | Expected Result                                             | Status |
| ------ | ------------------------------------- | ----------------------------------------------------------- | ------ |
| TC-006 | View pizza menu                       | Available pizzas should be displayed correctly              | PASS   |
| TC-007 | Open pizza details/customization      | Pizza information and available options should be displayed | PASS   |
| TC-008 | Add pizza to cart                     | Selected pizza should be added to the cart                  | PASS   |
| TC-009 | Add pizza with toppings/customization | Selected customization should be reflected in the cart      | PASS   |

---

## Cart

| ID     | Test Case              | Expected Result                              | Status |
| ------ | ---------------------- | -------------------------------------------- | ------ |
| TC-010 | View cart              | Cart should display selected items correctly | PASS   |
| TC-011 | Increase item quantity | Quantity and total should update correctly   | PASS   |
| TC-012 | Decrease item quantity | Quantity and total should update correctly   | PASS   |
| TC-013 | Remove item from cart  | Selected item should be removed              | PASS   |
| TC-014 | Refresh cart page      | Cart data should remain consistent           | PASS   |

---

## Checkout

| ID     | Test Case                           | Expected Result                            | Status |
| ------ | ----------------------------------- | ------------------------------------------ | ------ |
| TC-015 | Proceed to checkout with valid cart | Checkout page should open successfully     | PASS   |
| TC-016 | Enter valid customer information    | Information should be accepted             | PASS   |
| TC-017 | Select payment method               | Selected payment method should be accepted | PASS   |
| TC-018 | Place order with valid information  | Order should be created successfully       | PASS   |

---

## Order & Navigation

| ID     | Test Case                              | Expected Result                                               | Status |
| ------ | -------------------------------------- | ------------------------------------------------------------- | ------ |
| TC-019 | Verify order after successful checkout | Order details/status should be displayed correctly            | PASS   |
| TC-020 | Navigate between application pages     | Navigation should work without crashes or unexpected behavior | PASS   |

---

# Test Execution Result

| Metric           | Result |
| ---------------- | -----: |
| Total Test Cases |     20 |
| Passed           |     20 |
| Failed           |      0 |
| Blocked          |      0 |
| Not Executed     |      0 |
| Pass Rate        |   100% |

## Conclusion

All 20 planned manual functional test cases were executed successfully.

No unexpected functional defects were confirmed during the standard manual test execution.

Additional exploratory testing and intentionally problematic user testing were performed separately and are documented in their respective project folders.
