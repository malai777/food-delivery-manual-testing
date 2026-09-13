# OmniPizza Food Delivery — API Test Data

## 1. Purpose

This document contains the test data used during API testing of the OmniPizza food delivery application.

---

## 2. Authentication Data

### Valid Credentials

```text
Username: standard_user
Password: pizza123
```

### Invalid Password

```text
Username: standard_user
Password: wrongpassword
```

### Invalid Username

```text
Username: invalid_user
Password: pizza123
```

### Locked User

```text
Username: locked_out_user
Password: pizza123
```

---

## 3. Authentication Negative Data

| Scenario         | Username          | Password        |  Expected Status |
| ---------------- | ----------------- | --------------- | ---------------: |
| Valid login      | `standard_user`   | `pizza123`      |              200 |
| Invalid password | `standard_user`   | `wrongpassword` |              401 |
| Locked account   | `locked_out_user` | `pizza123`      |              403 |
| Empty username   | Empty             | `pizza123`      | Validation error |
| Empty password   | `standard_user`   | Empty           | Validation error |
| Invalid username | `invalid_user`    | `pizza123`      |              401 |

---

## 4. API Headers

### Authentication

```text
Authorization: Bearer <valid_access_token>
```

### Country

```text
X-Country-Code: US
```

### Content Type

```text
Content-Type: application/json
```

### Accept

```text
Accept: application/json
```

> Authentication tokens were generated during testing and are not stored in this repository.

---

## 5. Pizza API Data

### Pizza Used for Testing

```text
Pizza ID: p01
Pizza Name: Margherita
Country: US
Currency: USD
Size: small
Quantity: 1
Toppings: []
```

### Expected Price

```text
Base Price: $12.99
```

---

## 6. Cart API Data

### Create Cart Request

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

### Quantity Update

```text
Item ID: item-001
Original Quantity: 1
Updated Quantity: 2
```

### Cart Verification

Expected:

```text
Pizza: Margherita
Quantity: 2
Price: $12.99
Currency: USD
```

---

## 7. Checkout API Data

### Customer Information

```text
Name: Test User
Address: 123 Test Street
Phone: 9876543210
ZIP Code: 40001
```

### Order Information

```text
Pizza ID: p01
Quantity: 1
Size: small
Toppings: []
Payment Method: card
Tip: 0
Country: US
```

---

## 8. Checkout Calculation

```text
Subtotal:      $12.99
Delivery Fee:  $2.00
Tax Rate:      8%
Tax:           $1.04
Tip:           $0.00
---------------------
Expected Total: $16.03
```

### Validation

```text
$12.99 + $2.00 + $1.04 + $0.00 = $16.03
```

Returned API total:

```text
$16.03
```

---

## 9. Order Data

### Created Order

```text
Order ID: ORDER-705A26F1
Initial Status: pending
Final Status: cancelled
```

### Invalid Order

```text
Order ID: INVALID-ORDER-999
Expected Status: 404
```

---

## 10. Invalid Input Data

### Invalid ZIP Code

```text
ZIP Code: 400001
```

Expected:

```text
Validation error
```

The API rejected the six-digit ZIP code because the tested US ZIP code validation required five digits.

---

## 11. API Test Data Summary

| Data Category          | Used |
| ---------------------- | ---- |
| Valid authentication   | Yes  |
| Invalid authentication | Yes  |
| Locked account         | Yes  |
| Empty required fields  | Yes  |
| Country header         | Yes  |
| Pizza data             | Yes  |
| Cart data              | Yes  |
| Checkout data          | Yes  |
| Order data             | Yes  |
| Invalid order ID       | Yes  |
| Invalid ZIP code       | Yes  |

---

## 12. Security Note

No real customer information, payment-card information, or authentication tokens are included in this project.

All data used for testing was dummy/test data.
