# Test Scenarios – Demoblaze Manual Testing

## 1. Purpose

This document defines the **high-value test scenarios** selected for detailed validation through test cases. The scenarios are derived directly from the **Test Plan** and focus on **business-critical user flows and high-risk areas**.

Only scenarios that justify deeper coverage (positive, negative, and edge cases) are included. Lower-risk behaviors are intentionally excluded to maintain focus and efficiency.

---

## 2. Scenario Selection Criteria

Scenarios included in this document meet one or more of the following criteria:

* Direct impact on **checkout or revenue-related flows**
* Risk of **data loss or inconsistent state**
* High frequency of user interaction
* History of instability or unclear behavior in demo environments

---

## 3. Authentication Scenarios

### TS-01 – User successfully creates a new account

**Description:** Verify that a new user can create an account using valid credentials.
**Business Risk:** Medium – entry point for user engagement.

---

### TS-02 – User attempts to sign up with invalid or duplicate credentials

**Description:** Verify system behavior when invalid data or an existing username is used during sign-up.
**Business Risk:** Medium – data integrity and user feedback.

---

### TS-03 – User logs in with valid credentials

**Description:** Verify that a registered user can successfully authenticate and access user-specific functionality.
**Business Risk:** Medium – access to cart and checkout flows.

---

### TS-04 – User logs out and session is properly terminated

**Description:** Verify that user session is ended after logout and restricted actions are no longer available.
**Business Risk:** Medium – session management and security perception.

---

## 4. Product Catalog and Product Details Scenarios

### TS-05 – User browses product categories and views product details

**Description:** Verify that products are displayed correctly and product details pages load expected information.
**Business Risk:** Medium – product discoverability and trust.

---

### TS-06 – User navigates between products and categories without data corruption

**Description:** Verify application stability during navigation across multiple categories and products.
**Business Risk:** Low – general usability.

---

## 5. Cart Management Scenarios (High Priority)

### TS-07 – User adds a product to the cart

**Description:** Verify that selected products are correctly added to the cart.
**Business Risk:** High – core e-commerce functionality.

---

### TS-08 – User adds the same product multiple times

**Description:** Verify cart behavior when the same product is added repeatedly.
**Business Risk:** High – pricing accuracy and cart consistency.

---

### TS-09 – User removes a product from the cart

**Description:** Verify that products can be removed and cart totals update correctly.
**Business Risk:** High – cart accuracy.

---

### TS-10 – Cart data persists during navigation and page refresh

**Description:** Verify that cart contents are preserved when navigating between pages or refreshing the browser.
**Business Risk:** High – risk of data loss and user frustration.

---

## 6. Checkout and Order Placement Scenarios (Critical)

### TS-11 – Logged-in user successfully places an order

**Description:** Verify that a logged-in user can complete the checkout process with valid order details.
**Business Risk:** High – revenue and conversion.

---

### TS-12 – User attempts to place an order with missing mandatory fields

**Description:** Verify system validation and error handling when required checkout fields are empty.
**Business Risk:** High – data integrity and order quality.

---

### TS-13 – User places an order with invalid input data

**Description:** Verify checkout behavior when invalid or unexpected input is provided (special characters, long strings).
**Business Risk:** High – system robustness and data quality.

---

### TS-14 – Unauthorized user attempts to place an order

**Description:** Verify application behavior when a non-authenticated user initiates checkout.
**Business Risk:** High – business rules and access control.

---

### TS-15 – User interrupts checkout process

**Description:** Verify system behavior when checkout is interrupted (modal closed, page refreshed).
**Business Risk:** High – state management and usability.

---

## 7. Post-Order and Data Integrity Scenarios

### TS-16 – Order confirmation feedback is displayed to the user

**Description:** Verify that the user receives clear feedback after placing an order.
**Business Risk:** Medium – user trust and transparency.

---

### TS-17 – Cart state after successful order placement

**Description:** Verify cart behavior after order completion.
**Business Risk:** Medium – prevention of duplicate or incorrect orders.

---

## 8. Scenario Coverage Notes

* Not all scenarios are expanded into test cases; focus is placed on **high-risk and high-impact flows**.
* Exploratory testing is used alongside these scenarios to identify additional risks.
* Scenario outcomes are summarized in the **Test Summary Report**.

---

