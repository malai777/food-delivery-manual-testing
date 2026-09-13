# OmniPizza Food Delivery — Test Plan

## 1. Introduction

This document defines the testing approach for the OmniPizza food delivery web application.

The objective is to verify the application's core functionality, identify unexpected behavior, and validate important API workflows.

---

## 2. Objectives

The main testing objectives are:

* Verify user authentication
* Verify pizza browsing and selection
* Verify cart functionality
* Verify checkout functionality
* Verify order creation and order management
* Validate negative scenarios
* Perform exploratory testing
* Validate backend API behavior
* Test intentionally problematic user accounts
* Document test results and observations

---

## 3. Scope

### In Scope

* Login
* Authentication validation
* Pizza listing
* Pizza selection
* Cart management
* Quantity updates
* Cart item deletion
* Checkout
* Customer information
* Order creation
* Order retrieval
* Order cancellation
* API authentication
* API request/response validation
* Negative API testing
* Problem-user testing
* Exploratory testing

### Out of Scope

* Production deployment testing
* Performance/load testing
* Full security penetration testing
* Database-level validation
* Formal UAT
* Jira defect lifecycle management

---

## 4. Testing Types

The following testing types were performed:

### Functional Testing

Used to verify that the main application features work according to expected behavior.

### Negative Testing

Used to verify application behavior when invalid credentials, invalid inputs, or invalid requests are provided.

### Exploratory Testing

Used to investigate application behavior outside predefined test cases.

### API Testing

Used to validate backend endpoints, status codes, response data, authentication, cart operations, checkout, and order workflows.

### Problem-User Testing

Used to test OmniPizza's intentionally problematic user accounts and document their behavior.

---

## 5. Test Environment

**Application:** OmniPizza Food Delivery

**Browser:** Web browser

**API Testing Tool:** Postman

**API Documentation:** Swagger / OpenAPI

**Version Control:** Git / GitHub

---

## 6. Test Data

The following test accounts were used:

| Username                  | Purpose                         |
| ------------------------- | ------------------------------- |
| `standard_user`           | Normal application flow         |
| `locked_out_user`         | Locked account testing          |
| `problem_user`            | Problematic UI/pricing behavior |
| `performance_glitch_user` | Performance behavior            |
| `error_user`              | Checkout error behavior         |
| `a11y_glitch_user`        | Accessibility behavior          |
| `security_glitch_user`    | Security-related behavior       |

Password for the provided test accounts:

`pizza123`

---

## 7. Entry Criteria

Testing could begin when:

* The application was accessible
* Test accounts were available
* Required test data was prepared
* API endpoints were accessible
* Postman was available for API testing

---

## 8. Exit Criteria

Testing was considered complete when:

* Planned manual test cases were executed
* Exploratory scenarios were completed
* API test cases were executed
* Problem-user scenarios were tested
* Results were documented
* Screenshots/evidence were collected where applicable

---

## 9. Test Execution Summary

| Testing Area         | Planned/Executed |     Passed | Failed |
| -------------------- | ---------------: | ---------: | -----: |
| Manual Testing       |               20 |         20 |      0 |
| Exploratory Testing  |                3 |          3 |      0 |
| API Testing          |               20 |         20 |      0 |
| Problem-User Testing |      6 scenarios | Documented |      — |

### Standard Test Execution

**43 planned/executed checks**

**43 passed**

**0 failed**

**100% pass rate**

Problem-user testing is documented separately because several of the observed behaviors are intentionally seeded by the application.

---

## 10. Defect Handling

Unexpected defects identified during testing would be documented with:

* Defect ID
* Title
* Environment
* Preconditions
* Steps to reproduce
* Expected result
* Actual result
* Severity
* Priority
* Evidence
* Status

Intentionally seeded behavior associated with OmniPizza's special test accounts is documented as a known test scenario rather than automatically classified as an accidental defect.

---

## 11. Deliverables

The project contains:

* Test Plan
* Manual Test Cases
* Test Data
* Requirements Traceability Matrix
* Exploratory Testing Documentation
* Problem-User Testing Documentation
* API Test Plan
* API Test Cases
* API Test Data
* Screenshots
* Test Execution Results

---

## 12. Conclusion

The OmniPizza application was tested through manual functional testing, exploratory testing, API testing, negative testing, and problem-user testing.

The standard planned test execution achieved a **100% pass rate**, while the intentionally problematic user accounts were separately investigated and documented.
