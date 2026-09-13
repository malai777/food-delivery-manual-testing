# OmniPizza Food Delivery — Test Scenarios

## 1. Purpose

This document contains the high-level test scenarios defined for testing the OmniPizza food delivery web application.

Test scenarios describe **what needs to be tested**, while the detailed test cases contain the specific steps, test data, expected results, and execution status.

---

# 2. Functional Test Scenarios

## TS-001 — User Login

**Objective:**
Verify that users can authenticate successfully and that invalid authentication attempts are handled correctly.

**Scenarios:**

* Login with valid credentials
* Login with invalid username
* Login with invalid password
* Login with empty username
* Login with empty password
* Verify locked-out user behavior

**Related Test Cases:** TC-001 to TC-005

**Result:** PASS

---

## TS-002 — Pizza Menu

**Objective:**
Verify that users can browse available pizzas and view pizza information.

**Scenarios:**

* View pizza menu
* Verify pizza information
* Open pizza customization/details
* Select a pizza

**Related Test Cases:** TC-006 to TC-007

**Result:** PASS

---

## TS-003 — Add Pizza to Cart

**Objective:**
Verify that users can add pizzas and customized pizzas to the shopping cart.

**Scenarios:**

* Add a pizza to cart
* Add pizza with toppings/customization
* Verify selected pizza appears in cart
* Verify selected customization appears correctly

**Related Test Cases:** TC-008 to TC-009

**Result:** PASS

---

## TS-004 — Cart Management

**Objective:**
Verify that users can view and manage items in the cart.

**Scenarios:**

* View cart
* Increase pizza quantity
* Decrease pizza quantity
* Remove pizza from cart
* Refresh cart
* Verify cart information remains consistent

**Related Test Cases:** TC-010 to TC-014

**Result:** PASS

---

## TS-005 — Checkout

**Objective:**
Verify that users can proceed through checkout using valid information.

**Scenarios:**

* Open checkout
* Enter customer information
* Select payment method
* Submit order
* Verify successful order creation

**Related Test Cases:** TC-015 to TC-018

**Result:** PASS

---

## TS-006 — Order Management

**Objective:**
Verify that users can view and validate order information after checkout.

**Scenarios:**

* Verify created order
* Verify order details
* Verify order status
* Navigate through order-related functionality

**Related Test Cases:** TC-019 to TC-020

**Result:** PASS

---

# 3. Negative Test Scenarios

## TS-007 — Invalid Login

**Objective:**
Verify that invalid authentication information is rejected.

**Scenarios:**

* Invalid username
* Invalid password
* Empty username
* Empty password
* Locked account

**Result:** PASS

---

## TS-008 — Invalid Checkout Data

**Objective:**
Verify that invalid checkout information is rejected by the application/API.

**Scenarios:**

* Invalid ZIP code
* Missing/invalid required checkout information

**Result:** PASS

---

## TS-009 — Invalid Order Request

**Objective:**
Verify that requests for non-existent orders are handled correctly.

**Scenario:**

* Request an invalid order ID

**Expected Behavior:**
Application/API should return an appropriate order-not-found response.

**Result:** PASS

---

# 4. Exploratory Test Scenarios

## TS-010 — Browser Refresh During Checkout

**Objective:**
Verify application behavior when the browser is refreshed during checkout.

**Scenario:**

* Refresh the browser while checkout information is entered.

**Observed:**
Application remained functional. Unsaved checkout information was cleared.

**Result:** PASS

---

## TS-011 — Browser Back During Checkout

**Objective:**
Verify application behavior when navigating backward from checkout.

**Scenario:**

* Use the browser Back button during checkout.
* Return to the checkout flow.
* Verify cart state.

**Observed:**
Application remained functional and cart information remained correct.

**Result:** PASS

---

## TS-012 — Multiple Browser Tabs

**Objective:**
Verify application behavior when the same account is opened in multiple browser tabs.

**Scenario:**

* Open the application in multiple tabs.
* Modify/view cart information.
* Refresh the tabs.
* Compare application state.

**Observed:**
Application remained functional and cart information remained consistent.

**Result:** PASS

---

# 5. Problem-User Test Scenarios

OmniPizza provides intentionally problematic test accounts for QA practice.

These scenarios were tested separately from the standard functional test cases.

## TS-013 — Problem User

**Test User:** `problem_user`

**Objective:**
Verify application behavior under the Problem User scenario.

**Areas Checked:**

* Pizza pricing
* Pizza images
* Cart behavior
* Ordering flow

**Observed:**
Abnormal pricing/image behavior was observed.

**Classification:**
Known / intentional test scenario.

**Result:** DOCUMENTED

---

## TS-014 — Locked Out User

**Test User:** `locked_out_user`

**Objective:**
Verify that a locked account cannot authenticate.

**Expected:**
Login should be rejected.

**Observed:**
Login was rejected with a locked-user message.

**Classification:**
Expected / intentional test scenario.

**Result:** PASS

---

## TS-015 — Performance Glitch User

**Test User:** `performance_glitch_user`

**Objective:**
Observe application responsiveness using the performance test account.

**Areas Checked:**

* Page response
* Application/API response behavior
* Delays during interaction

**Observed:**
Noticeable delays were observed.

**Classification:**
Known / intentional test scenario.

**Result:** DOCUMENTED

---

## TS-016 — Error User

**Test User:** `error_user`

**Objective:**
Verify application behavior when checkout errors are intentionally triggered.

**Areas Checked:**

* Cart
* Checkout
* Order submission

**Observed:**
Checkout error behavior was observed.

**Classification:**
Known / intentional test scenario.

**Result:** DOCUMENTED

---

## TS-017 — Accessibility Glitch User

**Test User:** `a11y_glitch_user`

**Objective:**
Check application behavior for intentionally introduced accessibility issues.

**Areas Checked:**

* UI interaction
* Accessibility-related behavior
* Application controls

**Observed:**
Accessibility-related abnormal behavior was observed during testing.

**Classification:**
Known / intentional test scenario.

**Result:** DOCUMENTED

---

## TS-018 — Security Glitch User

**Test User:** `security_glitch_user`

**Objective:**
Check application behavior under the intentionally provided security test scenario.

**Areas Checked:**

* Access control
* Application data exposure
* Security-related behavior

**Observed:**
Security-related abnormal behavior was investigated.

**Classification:**
Known / intentional test scenario.

**Result:** DOCUMENTED

---

# 6. API Test Scenarios

## TS-019 — API Authentication

**Objective:**
Verify authentication API behavior.

**Scenarios:**

* Valid login
* Invalid password
* Invalid username
* Locked user
* Empty username
* Empty password

**API Test Cases:** API-001 to API-006

**Result:** PASS

---

## TS-020 — Pizza API

**Objective:**
Verify pizza API authentication and data retrieval.

**Scenarios:**

* Retrieve pizzas with valid authentication
* Verify country header requirement
* Verify unauthenticated request behavior

**API Test Cases:** API-007 to API-008

**Result:** PASS

---

## TS-021 — Cart API

**Objective:**
Verify backend cart operations.

**Scenarios:**

* Create/update cart
* Retrieve cart
* Update item quantity
* Verify updated quantity
* Delete cart item
* Verify empty cart

**API Test Cases:** API-009 to API-014

**Result:** PASS

---

## TS-022 — Checkout API

**Objective:**
Verify backend checkout processing and order creation.

**Scenarios:**

* Submit valid checkout information
* Create an order
* Verify order ID
* Verify order status
* Verify subtotal
* Verify delivery fee
* Verify tax
* Verify tip
* Verify final total

**API Test Cases:** API-015 to API-016

**Result:** PASS

---

## TS-023 — Order API

**Objective:**
Verify order retrieval and order status management.

**Scenarios:**

* Retrieve all orders
* Retrieve a specific order
* Request an invalid order
* Cancel an order
* Verify cancelled order status

**API Test Cases:** API-017 to API-020

**Result:** PASS

---

# 7. Overall Scenario Summary

| Category             | Scenario IDs    | Result     |
| -------------------- | --------------- | ---------- |
| Functional Testing   | TS-001 – TS-006 | PASS       |
| Negative Testing     | TS-007 – TS-009 | PASS       |
| Exploratory Testing  | TS-010 – TS-012 | PASS       |
| Problem-User Testing | TS-013 – TS-018 | DOCUMENTED |
| API Testing          | TS-019 – TS-023 | PASS       |

---

# 8. Overall Testing Result

### Standard Testing

* Manual test cases: **20/20 PASS**
* Exploratory scenarios: **3/3 PASS**
* API test cases: **20/20 PASS**

### Problem-User Testing

* **6 special-user scenarios tested and documented**

The problem-user scenarios are maintained separately because the abnormal behaviors are intentionally provided by the application for testing purposes.

---

## 9. Conclusion

The test scenarios covered the major functional areas of the OmniPizza food delivery application, including authentication, pizza selection, cart management, checkout, orders, negative scenarios, exploratory testing, API testing, and intentionally problematic user scenarios.

Detailed execution information is maintained in the corresponding test case, exploratory testing, API testing, and problem-user testing documentation.
