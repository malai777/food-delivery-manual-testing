# Bug User Testing

## BUG-USER-001 — Problem User

### Test User
`problem_user`

### Test Objective
Verify application behavior using the Problem User account.

### Steps to Reproduce
1. Open the OmniPizza application.
2. Login with:
   - Username: `problem_user`
   - Password: `pizza123`
3. Browse the pizza menu.
4. Add a pizza to the cart.
5. Open the cart.
6. Continue through the ordering flow.

### Expected Result
Pizza prices, images, cart information, and order information should be displayed correctly.

### Actual Result
The Problem User account displayed abnormal pricing/behavior, including pizza prices appearing as `$0`.

### Severity
Medium

### Priority
Medium

### Status
Known / Intentional Test Scenario

### Evidence
Screenshot: `Screenshots/problem-user.png`

---

## BUG-USER-002 — Error User Checkout

### Test User
`error_user`

### Test Objective
Verify checkout behavior using the Error User account.

### Steps to Reproduce
1. Open the OmniPizza application.
2. Login with:
   - Username: `error_user`
   - Password: `pizza123`
3. Add a pizza to the cart.
4. Proceed to checkout.
5. Enter valid checkout information.
6. Submit the order.

### Expected Result
The order should be processed successfully and an order confirmation should be displayed.

### Actual Result
Checkout failed with an error instead of completing the order.

### Severity
High

### Priority
High

### Status
Known / Intentional Test Scenario

### Evidence
Screenshot: `Screenshots/error-user.png`

---

## BUG-USER-003 — Locked Out User

### Test User
`locked_out_user`

### Test Objective
Verify that a locked account cannot access the application.

### Steps to Reproduce
1. Open the OmniPizza application.
2. Enter:
   - Username: `locked_out_user`
   - Password: `pizza123`
3. Click Login.

### Expected Result
The user should not be allowed to log in and an appropriate error message should be displayed.

### Actual Result
Login was rejected with a locked-out user message.

### Severity
N/A

### Priority
N/A

### Status
Expected / Intentional Test Scenario

---

## BUG-USER-004 — Performance Glitch User

### Test User
`performance_glitch_user`

### Test Objective
Check application responsiveness using the Performance Glitch User.

### Steps to Reproduce
1. Login using `performance_glitch_user`.
2. Navigate through the application.
3. Observe the response time of application actions.

### Expected Result
Application actions should respond within an acceptable time.

### Actual Result
Noticeable delay was observed during application/API operations.

### Severity
Medium

### Priority
Medium

### Status
Known / Intentional Test Scenario

---

## BUG-USER-005 — Accessibility Glitch User

### Test User
`a11y_glitch_user`

### Test Objective
Check the application for accessibility-related issues.

### Steps to Reproduce
1. Login using `a11y_glitch_user`.
2. Navigate through the main application screens.
3. Interact with available controls and elements.
4. Observe accessibility behavior.

### Expected Result
UI elements should be accessible and usable according to expected accessibility standards.

### Actual Result
Accessibility-related abnormal behavior was observed during testing.

### Severity
Medium

### Priority
Medium

### Status
Known / Intentional Test Scenario

---

## BUG-USER-006 — Security Glitch User

### Test User
`security_glitch_user`

### Test Objective
Check the application for intentionally introduced security-related issues.

### Steps to Reproduce
1. Login using `security_glitch_user`.
2. Navigate through the application.
3. Test access to application data and functionality.
4. Observe whether unauthorized information or functionality is exposed.

### Expected Result
Users should only be able to access information and functionality they are authorized to access.

### Actual Result
Security-related abnormal behavior was observed during testing.

### Severity
High

### Priority
High

### Status
Known / Intentional Test Scenario