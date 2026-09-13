# Food Delivery Manual Testing Project

A manual QA testing project for **OmniPizza**, a test-friendly food ordering web application.

This project demonstrates practical manual testing skills including test planning, test case design, functional testing, negative testing, exploratory testing, checkout validation, test data management, requirements traceability, and defect reporting.

---

## Project Overview

**Application:** OmniPizza  
**Testing Type:** Manual Testing  
**Tester:** Malaika  
**Project Status:** Completed

The objective of this project was to test the core food-ordering workflow from login through cart management and checkout.

---

## Testing Objectives

The main objectives were to verify:

- User authentication
- Login validation
- Pizza selection and cart functionality
- Pizza quantity management
- Cart item removal
- Checkout field validation
- Phone number validation
- ZIP code validation
- Required field validation
- Payment flow
- Tip calculation
- Checkout total calculation
- Order confirmation
- Cart behavior after successful order
- Browser navigation behavior
- Multiple browser tab behavior

---

## Scope of Testing

### In Scope

- Login
- Authentication validation
- Product selection
- Cart functionality
- Quantity management
- Checkout
- Form validation
- Payment flow
- Tip calculation
- Tax and delivery fee calculation
- Order placement
- Order confirmation
- Exploratory testing
- Browser navigation
- Multiple browser tabs

### Out of Scope

- Performance/load testing
- Security penetration testing
- Database testing
- API automation
- Mobile application testing
- Production payment processing
- Real customer data

---

## Testing Types

The following testing techniques were used:

- Functional Testing
- Positive Testing
- Negative Testing
- Boundary/Validation Testing
- UI Testing
- End-to-End Testing
- Exploratory Testing
- Regression Checks

---

## Test Environment

| Item | Details |
|---|---|
| Application | OmniPizza |
| Testing Type | Manual |
| Browser | Google Chrome |
| Platform | macOS |
| Test Data | Dummy/Test Data |
| Payment | Demo/Simulated Payment Flow |

No real payment credentials or sensitive personal information were used.

---

# Test Execution Summary

## Planned Test Cases

**Total Test Cases:** 20  
**Passed:** 20  
**Failed:** 0  
**Pass Rate:** 100%

All planned test cases passed during execution.

---

## Exploratory Testing

Additional exploratory testing was performed after completing the planned test cases.

| Test | Area | Result |
|---|---|---|
| ET-001 | Refresh during checkout | PASS |
| ET-002 | Browser Back navigation | PASS |
| ET-003 | Multiple browser tabs | PASS |

**Exploratory Tests:** 3  
**Passed:** 3  
**Failed:** 0

### Exploratory Testing Areas

- Browser refresh during checkout
- Browser Back navigation
- Cart persistence during navigation
- Multiple browser tabs
- Cart quantity synchronization

No confirmed defects were identified during exploratory testing.

---

# Overall Test Result

| Metric | Result |
|---|---:|
| Planned Test Cases | 20 |
| Planned Tests Passed | 20 |
| Exploratory Tests | 3 |
| Exploratory Tests Passed | 3 |
| Total Tests Executed | 23 |
| Total Passed | 23 |
| Total Failed | 0 |
| Confirmed Bugs | 0 |
| Overall Pass Rate | 100% |

---

# Test Documentation

### Test Plan

Contains:

- Testing objectives
- Scope
- Testing types
- Test environment
- Entry criteria
- Exit criteria
- Test scenarios
- Test execution summary

[View Test Plan](Test-Plan/Test-Plan.md)

---

### Test Cases

Contains 20 manually designed test cases covering:

- Login
- Cart functionality
- Checkout
- Validation
- Payment
- Calculations
- Order confirmation

[View Test Cases](Test-Cases/Test-Cases.md)

---

### Test Data

Contains the dummy data used during testing, including:

- Login credentials
- Checkout data
- Cart data
- Negative test data
- Payment test data

[View Test Data](Test-Data/Test-Data.md)

---

### Requirements Traceability Matrix

The RTM maps requirements to test cases and helps verify test coverage.

**Requirements Covered:** 17  
**Test Cases Mapped:** 20  
**Coverage:** 100%

[View RTM](Requirements-Traceability/RTM.md)

---

### Exploratory Testing

Contains the exploratory testing performed after the planned test cases.

Areas covered:

- Checkout refresh
- Browser Back navigation
- Multiple browser tabs

[View Exploratory Testing](Exploratory-Testing/Exploratory-Testing.md)

---

### Bug Reports

No confirmed reproducible defects were identified during the testing performed.

Only confirmed defects would be documented as bug reports.

[View Bug Reports](Bug-Reports/README.md)

---

# Screenshots

Screenshots were captured as evidence for selected test scenarios.

Examples include:

- Successful login
- Invalid login
- Cart functionality
- Phone validation
- Checkout calculation
- Successful order

Screenshots are available in the `Screenshots/` folder.

---

# Project Structure

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
├── Bug-Reports/
│   └── README.md
│
└── Screenshots/
```

---

# Key QA Skills Demonstrated

This project demonstrates practical experience with:

- Manual test case creation
- Test planning
- Functional testing
- Positive and negative testing
- Form validation
- Boundary testing
- End-to-end testing
- Exploratory testing
- Requirements traceability
- Test data preparation
- Defect identification
- Defect reporting principles
- Test execution
- Evidence collection
- Regression checks
- Browser-based testing

---

# Testing Approach

Testing was performed using a combination of predefined test cases and exploratory testing.

The testing approach focused on verifying expected behavior while also checking common user actions that could produce unexpected results.

Observed behavior was not reported as a defect unless it was reproducible and could be confirmed as a violation of the expected requirements.

This helped avoid false-positive bug reports.

---

# Conclusion

The OmniPizza food ordering application was tested across its core user journey, including authentication, product selection, cart management, checkout, payment simulation, calculations, and order completion.

Additional exploratory testing was performed to verify browser navigation, refresh behavior, and multi-tab usage.

### Final Result

**23 tests executed → 23 passed → 0 failed → 0 confirmed bugs**

The project demonstrates a structured manual QA workflow from **test planning → test case design → execution → exploratory testing → evidence collection → reporting → final test summary**.