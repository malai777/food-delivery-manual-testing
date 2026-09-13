# OmniPizza Manual Testing - Test Plan

## 1. Project Overview

OmniPizza is a web-based food ordering application used as a testing sandbox.

The purpose of this project is to perform manual functional testing of the application's login, pizza selection, cart, checkout, payment and order confirmation functionality.

---

## 2. Testing Objective

The main objectives of testing are:

- Verify that users can log in successfully.
- Verify that invalid login information is handled correctly.
- Verify that pizzas can be added and removed from the cart.
- Verify that cart quantities and prices are updated correctly.
- Verify checkout field validation.
- Verify ZIP code and phone number validation.
- Verify the PayPal demo checkout flow.
- Verify tax, delivery fee, tip and total calculations.
- Verify successful order placement.
- Verify that the cart is cleared after a successful order.

---

## 3. Scope of Testing

### In Scope

The following features were tested:

- User Login
- Invalid Login Scenarios
- Pizza Selection
- Shopping Cart
- Quantity Management
- Cart Removal
- Checkout Form
- Phone Number Validation
- ZIP Code Validation
- PayPal Demo Payment Flow
- Price Calculation
- Tip Calculation
- Order Placement
- Order Confirmation
- Cart Clearing

### Out of Scope

The following areas were not covered in this test cycle:

- Backend/API testing
- Database testing
- Performance testing
- Security penetration testing
- Mobile application testing
- Accessibility testing
- Real payment processing

---

## 4. Test Type

The following manual testing techniques were used:

- Functional Testing
- Negative Testing
- Boundary Testing
- Validation Testing
- End-to-End Testing
- Exploratory Testing

---

## 5. Test Environment

| Item | Details |
|---|---|
| Application | OmniPizza |
| Application Type | Web Application |
| Testing Type | Manual Testing |
| Browser | Google Chrome |
| Platform | Web |
| Payment Method | PayPal Demo |
| Test Data | Application-provided test data |

---

## 6. Test Scenarios

### Authentication

- Verify login with valid credentials.
- Verify login with invalid username.
- Verify login with invalid password.
- Verify login with empty username.
- Verify login with empty password.

### Shopping Cart

- Verify adding a pizza to the cart.
- Verify increasing pizza quantity.
- Verify decreasing pizza quantity.
- Verify removing a pizza from the cart.
- Verify cart price updates.

### Checkout

- Verify required checkout fields.
- Verify invalid phone number validation.
- Verify ZIP code validation.
- Verify PayPal demo checkout.
- Verify successful order placement.
- Verify order confirmation.
- Verify cart clearing after order.

### Price Calculation

- Verify subtotal calculation.
- Verify delivery fee.
- Verify tax calculation.
- Verify tip calculation.
- Verify final total.
- Verify total updates when quantity changes.
- Verify total updates when tip changes.

---

## 7. Entry Criteria

Testing can begin when:

- The application is accessible.
- Test users are available.
- The required test environment is ready.
- The application features under test are functional.

---

## 8. Exit Criteria

Testing can be completed when:

- Planned test cases have been executed.
- Test results have been recorded.
- Failed test cases, if any, have been investigated.
- Confirmed defects have been documented.
- Test results have been summarized.

---

## 9. Test Execution Summary

| Metric | Result |
|---|---:|
| Total Test Cases | 20 |
| Passed | 20 |
| Failed | 0 |
| Blocked | 0 |
| Pass Rate | 100% |

---

## 10. Test Result

All 20 executed test cases passed successfully.

No confirmed defects were identified during this test execution.

The PayPal demo was treated as a simulated payment environment. Validation behavior observed within the PayPal demo was not reported as an OmniPizza application defect.

---

## 11. Conclusion

The tested OmniPizza functionality performed as expected during the manual test execution.

Login, cart operations, checkout validation, price calculations, PayPal demo flow, order placement and post-order cart behavior were successfully verified.