# OmniPizza Manual Testing - Test Cases

## Test Execution Summary

| Metric | Result |
|---|---:|
| Total Test Cases | 20 |
| Passed | 20 |
| Failed | 0 |
| Blocked | 0 |
| Pass Rate | 100% |

---

## Test Cases

| Test Case ID | Test Case | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| TC-001 | Login with valid credentials | User should log in successfully | User logged in successfully | PASS |
| TC-002 | Login with invalid password | Login should be rejected | "Invalid credentials" displayed | PASS |
| TC-003 | Login with invalid username | Login should be rejected | "Invalid credentials" displayed | PASS |
| TC-004 | Login with empty username | Login should be prevented | "Invalid credentials" displayed | PASS |
| TC-005 | Login with empty password | Login should be prevented | "Invalid credentials" displayed | PASS |
| TC-006 | Add pizza to cart | Selected pizza should appear in cart | Pizza added successfully | PASS |
| TC-007 | Increase pizza quantity | Quantity and price should update | Updated correctly | PASS |
| TC-008 | Decrease pizza quantity | Quantity and price should update | Updated correctly | PASS |
| TC-009 | Remove pizza from cart | Pizza should be removed | Pizza removed successfully | PASS |
| TC-010 | Enter invalid/short phone number | Validation message should appear | Invalid phone number was rejected | PASS |
| TC-011 | Leave required checkout field empty | Required-field validation should appear | "Please fill in this field" displayed | PASS |
| TC-012 | Enter invalid ZIP code | Invalid ZIP code should be rejected | ZIP code validation worked correctly | PASS |
| TC-013 | Test PayPal checkout flow | PayPal demo should connect and return to checkout | PayPal connected successfully | PASS |
| TC-014 | Complete PayPal demo login flow | PayPal demo should process the simulated login | Demo PayPal flow completed | PASS |
| TC-015 | Verify checkout total calculation | Total should equal subtotal + delivery fee + tax + tip | Calculation was correct | PASS |
| TC-016 | Verify tip calculation | Tip amount should calculate correctly | Tip calculated correctly | PASS |
| TC-017 | Change pizza quantity and verify checkout total | Subtotal, tax and total should update | Values updated correctly | PASS |
| TC-018 | Change tip and verify total | Total should update according to selected tip | Total updated correctly | PASS |
| TC-019 | Complete order successfully | Order confirmation should appear | Order placed successfully | PASS |
| TC-020 | Verify cart after successful order | Cart should be empty after successful order | Cart was empty | PASS |

---

## Test Environment

- Application: OmniPizza
- Testing Type: Manual Testing
- Testing Approach: Functional and Negative Testing
- Browser: Google Chrome
- Platform: Web Application
- Payment Method Tested: PayPal Demo
- Test Users: OmniPizza provided test accounts

---

## Testing Areas Covered

### Authentication
- Valid login
- Invalid username
- Invalid password
- Empty required login fields

### Cart
- Add pizza
- Increase quantity
- Decrease quantity
- Remove pizza
- Quantity and price updates

### Checkout
- Required-field validation
- Phone number validation
- ZIP code validation
- PayPal checkout flow
- Order confirmation
- Cart clearing after order

### Price Calculation
- Subtotal
- Delivery fee
- Tax
- Tip
- Final total
- Quantity changes
- Tip changes

---

## Test Result

All 20 executed test cases passed successfully.

No confirmed defects were identified during this test execution.

> Note: PayPal validation behavior was treated as part of the simulated PayPal demo flow and was not reported as an OmniPizza defect.