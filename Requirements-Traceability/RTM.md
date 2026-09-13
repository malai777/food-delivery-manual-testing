# OmniPizza Food Delivery — Requirements Traceability Matrix

## 1. Purpose

The Requirements Traceability Matrix (RTM) maps application requirements to the corresponding manual test cases and confirms that the main functional areas were covered during testing.

---

## 2. RTM

| Requirement ID | Requirement                                              | Test Case IDs  | Status |
| -------------- | -------------------------------------------------------- | -------------- | ------ |
| REQ-001        | User should be able to log in with valid credentials     | TC-001         | PASS   |
| REQ-002        | Invalid username/password should be rejected             | TC-002, TC-003 | PASS   |
| REQ-003        | Required login fields should be validated                | TC-004, TC-005 | PASS   |
| REQ-004        | Users should be able to view available pizzas            | TC-006         | PASS   |
| REQ-005        | Users should be able to view pizza details/customization | TC-007         | PASS   |
| REQ-006        | Users should be able to add pizzas to the cart           | TC-008, TC-009 | PASS   |
| REQ-007        | Users should be able to view cart contents               | TC-010         | PASS   |
| REQ-008        | Users should be able to change item quantity             | TC-011, TC-012 | PASS   |
| REQ-009        | Users should be able to remove cart items                | TC-013         | PASS   |
| REQ-010        | Cart information should remain consistent after refresh  | TC-014         | PASS   |
| REQ-011        | Users should be able to proceed to checkout              | TC-015         | PASS   |
| REQ-012        | Checkout should accept valid customer information        | TC-016         | PASS   |
| REQ-013        | Users should be able to select a payment method          | TC-017         | PASS   |
| REQ-014        | Users should be able to place an order                   | TC-018         | PASS   |
| REQ-015        | Users should be able to verify order information/status  | TC-019         | PASS   |
| REQ-016        | Application navigation should work correctly             | TC-020         | PASS   |

---

## 3. Coverage Summary

| Metric                    | Result |
| ------------------------- | -----: |
| Requirements Identified   |     16 |
| Requirements Covered      |     16 |
| Requirements Not Covered  |      0 |
| Coverage                  |   100% |
| Related Manual Test Cases |     20 |
| Passed Test Cases         |     20 |
| Failed Test Cases         |      0 |

---

## 4. Additional Testing Coverage

In addition to the requirements mapped above, the project also included:

* Exploratory testing
* Negative testing
* API testing
* Authentication testing
* Problem-user testing
* Checkout validation
* Order lifecycle validation

These activities are documented separately in the project.

---

## 5. Conclusion

All identified functional requirements were mapped to one or more manual test cases.

The RTM shows **100% requirement-to-test-case coverage** for the requirements defined within the scope of this project.
