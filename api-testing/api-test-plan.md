# OmniPizza Food Delivery — API Test Plan

## 1. Introduction

This document defines the API testing approach used to validate the OmniPizza backend API.

API testing was performed using Postman against the application's REST API.

---

## 2. Objectives

The objectives of API testing were to:

* Verify API authentication
* Validate successful and unsuccessful login requests
* Validate required input fields
* Verify authentication requirements
* Validate pizza data retrieval
* Verify cart operations
* Validate checkout processing
* Verify order retrieval
* Verify order cancellation
* Validate HTTP status codes
* Validate JSON response structures and values

---

## 3. API Scope

### Authentication

* Valid login
* Invalid credentials
* Locked user
* Empty username
* Empty password
* Invalid username

### Pizza API

* Retrieve pizzas with authentication
* Verify country header requirement
* Verify authentication requirement

### Cart API

* Create/update cart
* Retrieve cart
* Update cart quantity
* Verify updated cart
* Delete cart item
* Verify empty cart

### Checkout & Orders

* Checkout with valid information
* Retrieve orders
* Retrieve a specific order
* Invalid order ID
* Cancel an order
* Verify cancelled order

---

## 4. Testing Tool

**Tool:** Postman

**API Base URL:**

`https://omnipizza-backend.onrender.com`

**API Documentation:** Swagger / OpenAPI

---

## 5. Test Environment

* API accessed through HTTPS
* Requests executed using Postman
* Authentication performed using Bearer tokens
* `X-Country-Code` header used where required
* JSON request and response bodies validated

---

## 6. Testing Approach

Each API request was validated using:

* HTTP status code
* Response body
* Required response fields
* Expected values
* Authentication behavior
* Input validation
* Business logic
* Cart/order state changes

Postman test scripts were also used for selected authentication validations.

---

## 7. Test Data

Primary test account:

```text
Username: standard_user
Password: pizza123
```

Additional accounts were used for negative/problem-user testing.

Country header:

```text
X-Country-Code: US
```

Pizza:

```text
Pizza ID: p01
Pizza: Margherita
Size: small
Quantity: 1
```

---

## 8. Execution Summary

| Metric                | Result |
| --------------------- | -----: |
| API Test Cases        |     20 |
| Passed                |     20 |
| Failed                |      0 |
| Pass Rate             |   100% |
| Setup Activities      |      1 |
| Confirmed API Defects |      0 |

---

## 9. API Endpoints Tested

| Method | Endpoint                    | Purpose                 |
| ------ | --------------------------- | ----------------------- |
| POST   | `/api/auth/login`           | User authentication     |
| GET    | `/api/pizzas`               | Retrieve pizza data     |
| POST   | `/api/cart`                 | Create/update cart      |
| GET    | `/api/cart`                 | Retrieve cart           |
| PUT    | `/api/cart/items/{item_id}` | Update cart item        |
| DELETE | `/api/cart/items/{item_id}` | Delete cart item        |
| POST   | `/api/checkout`             | Create order            |
| GET    | `/api/orders`               | Retrieve orders         |
| GET    | `/api/orders/{order_id}`    | Retrieve specific order |
| PATCH  | `/api/orders/{order_id}`    | Update order status     |

---

## 10. Exit Criteria

API testing was considered complete after:

* All planned API test cases were executed
* Authentication scenarios were validated
* Cart operations were validated
* Checkout was validated
* Order operations were validated
* Negative scenarios were executed
* Response data was verified
* Test results were documented

---

## 11. Conclusion

A total of **20 API test cases** were executed using Postman.

All 20 test cases passed, resulting in a **100% pass rate** for the planned API test suite.

No unexpected API defects were confirmed during the executed test cases.
