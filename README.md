# 🍕 OmniPizza Food Delivery — Manual & API Testing

A hands-on QA testing project for a food delivery web application. The project covers manual testing, exploratory testing, API testing, negative testing, and testing with intentionally problematic user accounts.

## 🔗 Application

**Application:** OmniPizza Food Delivery

**Test Environment:** Web application

**API:** OmniPizza Backend API

**API Documentation:** Swagger / OpenAPI

---

## 🎯 Testing Objectives

* Validate core food-ordering functionality
* Verify positive and negative scenarios
* Validate API endpoints and responses
* Perform exploratory testing
* Test application behavior with different user types
* Verify authentication, cart, checkout, and order workflows
* Document testing results and observations

---

## 🧪 Testing Performed

### Manual Testing

* Login
* Pizza browsing
* Pizza selection
* Cart functionality
* Quantity updates
* Removing items
* Checkout
* Customer information
* Order placement
* Order flow validation

**20 planned manual test cases executed**

**Result: 20/20 PASS**

---

### 🔍 Exploratory Testing

The following exploratory scenarios were performed:

* Refreshing the browser during checkout
* Using the browser Back button during checkout
* Opening the application in multiple browser tabs

**3/3 exploratory scenarios passed**

---

### 👤 Problem / Special User Testing

OmniPizza provides intentionally problematic test accounts to simulate different application conditions.

The following accounts were tested:

| User                      | Scenario Tested               |
| ------------------------- | ----------------------------- |
| `problem_user`            | Pricing and UI/image problems |
| `locked_out_user`         | Locked account login          |
| `performance_glitch_user` | Performance delays            |
| `error_user`              | Checkout errors               |
| `a11y_glitch_user`        | Accessibility issues          |
| `security_glitch_user`    | Security-related scenarios    |

These behaviors were documented as **known/intentional test scenarios** where applicable rather than incorrectly reporting seeded behavior as an accidental production defect.

Detailed results are available in:

`Bug-User/Bug-User-Testing.md`

---

## 🔌 API Testing

API testing was performed using **Postman** against the OmniPizza backend API.

### Areas Tested

* Authentication
* Invalid authentication
* Locked user authentication
* Input validation
* Pizza API
* Authentication headers
* Cart creation
* Cart retrieval
* Cart quantity update
* Cart item deletion
* Checkout
* Order retrieval
* Invalid order ID
* Order cancellation
* Post-cancellation order verification

**20 API test cases executed**

**Result: 20/20 PASS**

---

## 📊 Test Summary

| Testing Area        | Executed | Passed | Failed |
| ------------------- | -------: | -----: | -----: |
| Manual Testing      |       20 |     20 |      0 |
| Exploratory Testing |        3 |      3 |      0 |
| API Testing         |       20 |     20 |      0 |
| **Total**           |   **43** | **43** |  **0** |

### Overall Result

**43/43 executed checks passed**

**Pass Rate: 100%**

No accidental/confirmed production defects were identified in the executed standard test cases. Known behaviors of intentionally problematic users were documented separately.

---

## 📁 Project Structure

```text
food-delivery-manual-testing/
│
├── README.md
│
├── Test-Plan/
│   └── Test-Plan.md
│
├── Test-Cases/
│   └── Test-Cases.md
│
├── Test-Data/
│   └── Test-Data.md
│
├── Requirements-Traceability/
│   └── RTM.md
│
├── Exploratory-Testing/
│   └── Exploratory-Testing.md
│
├── Bug-User/
│   └── Bug-User-Testing.md
│
├── API-Testing/
│   ├── API-Test-Plan.md
│   ├── API-Test-Cases.md
│   └── API-Test-Data.md
│
└── Screenshots/
```

---

## 🛠️ Tools Used

* Postman
* Git
* GitHub
* Web Browser
* Swagger / OpenAPI

---

## 📚 QA Skills Demonstrated

* Manual testing
* Test case design
* Positive testing
* Negative testing
* Exploratory testing
* Boundary/input validation
* Authentication testing
* API testing
* HTTP status code validation
* JSON response validation
* Cart and checkout testing
* Order workflow testing
* Test documentation
* Test result reporting
* Problem-user/negative scenario testing

---

## 📌 Project Outcome

This project demonstrates a complete testing workflow for a food delivery application, covering both UI and API validation.

The project focuses on practical QA activities rather than only theoretical test cases, including exploratory testing, API validation, authentication testing, checkout testing, and testing of intentionally problematic user scenarios.
