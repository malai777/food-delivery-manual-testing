# OmniPizza Food Delivery — API Test Cases

## Test Execution Summary

**Total API Test Cases:** 20
**Executed:** 20
**Passed:** 20
**Failed:** 0
**Pass Rate:** 100%

---

## Authentication API

### API-001 — Valid Login

**Method:** POST
**Endpoint:** `/api/auth/login`

**Test Data:**

```text
username: standard_user
password: pizza123
```

**Expected Result:**

* HTTP status should be `200`
* Response should contain an authentication token

**Actual Result:** Authentication token returned successfully.

**Status:** PASS

---

### API-002 — Invalid Password

**Method:** POST
**Endpoint:** `/api/auth/login`

**Test Data:**

```text
username: standard_user
password: wrongpassword
```

**Expected Result:**

* HTTP status should be `401`
* Appropriate authentication error should be returned

**Actual Result:** `401` returned with invalid username/password error.

**Status:** PASS

---

### API-003 — Locked User

**Method:** POST
**Endpoint:** `/api/auth/login`

**Test Data:**

```text
username: locked_out_user
password: pizza123
```

**Expected Result:**

* HTTP status should be `403`
* Locked-user error should be returned

**Actual Result:** `403` returned with locked-user error.

**Status:** PASS

---

### API-004 — Empty Username

**Method:** POST
**Endpoint:** `/api/auth/login`

**Test Data:**

```text
username: ""
password: pizza123
```

**Expected Result:**

* Request should be rejected
* Validation error should be returned

**Actual Result:** Validation error returned for username length.

**Status:** PASS

---

### API-005 — Empty Password

**Method:** POST
**Endpoint:** `/api/auth/login`

**Test Data:**

```text
username: standard_user
password: ""
```

**Expected Result:**

* Request should be rejected
* Validation error should be returned

**Actual Result:** Validation error returned for password length.

**Status:** PASS

---

### API-006 — Invalid Username

**Method:** POST
**Endpoint:** `/api/auth/login`

**Test Data:**

```text
username: invalid_user
password: pizza123
```

**Expected Result:**

* HTTP status should be `401`
* Authentication should fail

**Actual Result:** `401` returned with invalid username/password error.

**Status:** PASS

---

## Pizza API

### API-007 — Get Pizzas With Authentication

**Method:** GET
**Endpoint:** `/api/pizzas`

**Headers:**

```text
Authorization: Bearer <valid_token>
X-Country-Code: US
```

**Expected Result:**

* HTTP status should be `200`
* Pizza data should be returned
* Country and currency information should be available

**Actual Result:** `200` returned with pizza data and US/USD information.

**Status:** PASS

---

### API-008 — Get Pizzas Without Authentication

**Method:** GET
**Endpoint:** `/api/pizzas`

**Header:**

```text
X-Country-Code: US
```

**Expected Result:**

* Request should be rejected because authentication is required

**Actual Result:** `403 Not authenticated` returned.

**Status:** PASS

---

## Cart API

### API-009 — Create Cart

**Method:** POST
**Endpoint:** `/api/cart`

**Request Body:**

```json
{
  "items": [
    {
      "pizza_id": "p01",
      "quantity": 1,
      "size": "small",
      "toppings": [],
      "item_id": "item-001"
    }
  ]
}
```

**Expected Result:**
Cart should be created/updated with the selected pizza.

**Actual Result:** Cart item was successfully created.

**Status:** PASS

---

### API-010 — Get Cart

**Method:** GET
**Endpoint:** `/api/cart`

**Expected Result:**

* HTTP status should be `200`
* Cart should contain the previously added pizza
* Pizza name, quantity, price and currency should be returned

**Actual Result:** Cart returned successfully with Margherita, quantity 1 and USD price.

**Status:** PASS

---

### API-011 — Update Cart Quantity

**Method:** PUT
**Endpoint:** `/api/cart/items/item-001`

**Request Body:**

```json
{
  "pizza_id": "p01",
  "quantity": 2,
  "size": "small",
  "toppings": [],
  "item_id": "item-001"
}
```

**Expected Result:**
Cart quantity should be updated from 1 to 2.

**Actual Result:** Quantity updated successfully.

**Status:** PASS

---

### API-012 — Verify Updated Cart

**Method:** GET
**Endpoint:** `/api/cart`

**Expected Result:**
Cart should show quantity `2` for the selected item.

**Actual Result:** Quantity returned as `2`.

**Status:** PASS

---

### API-013 — Delete Cart Item

**Method:** DELETE
**Endpoint:** `/api/cart/items/item-001`

**Expected Result:**
Selected item should be removed from the cart.

**Actual Result:** Cart item was successfully removed.

**Status:** PASS

---

### API-014 — Verify Empty Cart

**Method:** GET
**Endpoint:** `/api/cart`

**Expected Result:**
Cart should contain no items after deletion.

**Actual Result:** Empty cart returned successfully.

**Status:** PASS

---

## Checkout & Order API

### API-015 — Checkout With Valid Information

**Method:** POST
**Endpoint:** `/api/checkout`

**Test Data:**

```text
Name: Test User
Address: 123 Test Street
Phone: 9876543210
ZIP Code: 40001
Payment Method: card
Tip: 0
```

**Expected Result:**

* Checkout should succeed
* Order ID should be generated
* Order status should be returned
* Total should be calculated correctly

**Actual Result:**
Order was successfully created with status `pending`.

Expected calculation:

```text
Subtotal:      $12.99
Delivery Fee:  $2.00
Tax:           $1.04
Tip:           $0.00
---------------------
Total:         $16.03
```

Returned total: `$16.03`

**Status:** PASS

---

### API-016 — Verify Checkout Total

**Expected Calculation:**

```text
12.99 + 2.00 + 1.04 + 0.00 = 16.03
```

**Expected Result:**
API total should equal `$16.03`.

**Actual Result:** Returned total was `$16.03`.

**Status:** PASS

---

### API-017 — Get Orders

**Method:** GET
**Endpoint:** `/api/orders`

**Expected Result:**
Previously created order should be returned with its order details.

**Actual Result:** Order `ORDER-705A26F1` was returned successfully.

**Status:** PASS

---

### API-018 — Get Specific Order

**Method:** GET
**Endpoint:** `/api/orders/ORDER-705A26F1`

**Expected Result:**
Specific order details should be returned.

**Actual Result:** Order details were returned successfully.

**Status:** PASS

---

### API-019 — Invalid Order ID

**Method:** GET
**Endpoint:** `/api/orders/INVALID-ORDER-999`

**Expected Result:**

* HTTP status should be `404`
* Order-not-found error should be returned

**Actual Result:** `404` returned with order-not-found error.

**Status:** PASS

---

### API-020 — Cancel Order

**Method:** PATCH
**Endpoint:** `/api/orders/ORDER-705A26F1`

**Request Body:**

```json
{
  "status": "cancelled"
}
```

**Expected Result:**
Order status should change from `pending` to `cancelled`.

**Actual Result:** Order status successfully changed to `cancelled`.

**Status:** PASS

---

# API Test Results

| ID Range          | Area              | Result         |
| ----------------- | ----------------- | -------------- |
| API-001 – API-006 | Authentication    | 6/6 PASS       |
| API-007 – API-008 | Pizza API         | 2/2 PASS       |
| API-009 – API-014 | Cart API          | 6/6 PASS       |
| API-015 – API-020 | Checkout & Orders | 6/6 PASS       |
| **Total**         | **All API Tests** | **20/20 PASS** |

## Final Result

**20/20 API test cases passed.**

**Pass Rate: 100%**

No unexpected API defects were confirmed during the executed API test cases.
