# OmniPizza Food Delivery — Test Data

## 1. Purpose

This document contains the test data used during manual, exploratory, and problem-user testing of the OmniPizza food delivery application.

---

## 2. User Accounts

| Username                  | Password   | Purpose                        |
| ------------------------- | ---------- | ------------------------------ |
| `standard_user`           | `pizza123` | Normal functional testing      |
| `locked_out_user`         | `pizza123` | Locked account testing         |
| `problem_user`            | `pizza123` | Problematic UI/pricing testing |
| `performance_glitch_user` | `pizza123` | Performance behavior testing   |
| `error_user`              | `pizza123` | Checkout error testing         |
| `a11y_glitch_user`        | `pizza123` | Accessibility testing          |
| `security_glitch_user`    | `pizza123` | Security-related testing       |

> These are test accounts provided by the OmniPizza application.

---

## 3. Login Test Data

### Valid Login

```text
Username: standard_user
Password: pizza123
Expected: Successful login
```

### Invalid Password

```text
Username: standard_user
Password: wrongpassword
Expected: Login should be rejected
```

### Invalid Username

```text
Username: invalid_user
Password: pizza123
Expected: Login should be rejected
```

### Locked Account

```text
Username: locked_out_user
Password: pizza123
Expected: Login should be rejected because the account is locked
```

---

## 4. Cart Test Data

### Pizza Used

```text
Pizza ID: p01
Pizza: Margherita
Size: Small
Quantity: 1
Toppings: None
```

### Quantity Update

```text
Initial Quantity: 1
Updated Quantity: 2
Expected: Cart quantity should become 2
```

---

## 5. Checkout Test Data

### Customer Information

```text
Name: Test User
Address: 123 Test Street
Phone: 9876543210
ZIP Code: 40001
```

### Payment

```text
Payment Method: Card
Tip: 0%
```

### Expected Order Calculation

```text
Pizza Price: $12.99
Delivery Fee: $2.00
Tax: $1.04
Tip: $0.00

Expected Total: $16.03
```

---

## 6. Negative Test Data

| Scenario         | Test Data           | Expected Result      |
| ---------------- | ------------------- | -------------------- |
| Empty username   | `""`                | Validation error     |
| Empty password   | `""`                | Validation error     |
| Invalid username | `invalid_user`      | Authentication error |
| Invalid password | `wrongpassword`     | Authentication error |
| Invalid ZIP code | `400001`            | Validation error     |
| Invalid order ID | `INVALID-ORDER-999` | Order not found      |

---

## 7. Problem-User Test Data

| User                      | Testing Purpose    | Observed Scenario                       |
| ------------------------- | ------------------ | --------------------------------------- |
| `problem_user`            | UI/data validation | Abnormal pricing/image behavior         |
| `locked_out_user`         | Authentication     | Login rejected                          |
| `performance_glitch_user` | Performance        | Delayed application/API response        |
| `error_user`              | Error handling     | Checkout error behavior                 |
| `a11y_glitch_user`        | Accessibility      | Accessibility-related abnormal behavior |
| `security_glitch_user`    | Security           | Security-related abnormal behavior      |

---

## 8. API Test Data

### Authentication

```text
Username: standard_user
Password: pizza123
```

### Country Header

```text
X-Country-Code: US
```

### Pizza

```text
Pizza ID: p01
Pizza: Margherita
Size: small
Quantity: 1
Toppings: []
```

### Cart Item

```text
Item ID: item-002
Pizza ID: p01
Quantity: 1
Size: small
Toppings: []
```

### Order

```text
Order ID: ORDER-705A26F1
Initial Status: pending
Updated Status: cancelled
```

---

## 9. Test Data Notes

* Test data was used only for QA validation.
* No real customer information was used.
* The provided OmniPizza test accounts were used for special-user testing.
* API authentication tokens were generated during testing and were not included in project documentation.
