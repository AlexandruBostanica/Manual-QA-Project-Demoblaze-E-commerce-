# Bug Reports – Demoblaze Manual Testing

## 1. Purpose

This document contains the **defects identified during manual testing** of the Demoblaze application, based on the defined Test Plan, Test Scenarios, and Test Cases.

The reported bugs focus on **functional correctness, data integrity, usability, and business impact**, rather than cosmetic issues. Each defect is documented in a **clear, reproducible, and business-oriented manner**, reflecting real-world QA reporting standards.

---

## 2. Bug Report Format

Each bug includes:

* **Bug ID**
* **Title**
* **Related Test Scenario / Test Case**
* **Severity**
* **Priority**
* **Environment**
* **Steps to Reproduce**
* **Expected Result**
* **Actual Result**
* **Business Impact**

---

## 3. Reported Bugs

### BUG-01 – Checkout allows order placement without validating cart total

**Related Scenario:** TS-11
**Related Test Case:** TC-06

**Severity:** High
**Priority:** High

**Environment:** Chrome (latest), Windows

**Steps to Reproduce:**

1. Log in to the application
2. Add a product to the cart
3. Open Cart page
4. Click "Place Order"
5. Modify checkout fields minimally and complete purchase

**Expected Result:**

* Order total is validated against cart contents

**Actual Result:**

* Order is placed without clear validation of cart total consistency

**Business Impact:**
Risk of incorrect order values, affecting billing accuracy and trust.

---

### BUG-02 – Order can be placed with only Name and Credit Card fields filled

**Related Scenario:** TS-11
**Related Test Case:** TC-06

**Severity:** High
**Priority:** High

**Environment:** Chrome (latest), Windows

**Steps to Reproduce:**

1. Log in to the application
2. Add product(s) to the cart
3. Open checkout modal
4. Fill only the Name and Credit Card fields
5. Click "Purchase"

**Expected Result:**

* Checkout should enforce completion of all mandatory fields, including address, city, and country

**Actual Result:**

* Order is successfully placed without completing other required fields

**Business Impact:**
Allows incomplete order submissions, causing potential shipping and fulfillment errors, and undermining data integrity.

---

### BUG-03 – Cart allows duplicate identical products without quantity indication

**Related Scenario:** TS-08
**Related Test Case:** TC-02

**Severity:** Medium
**Priority:** High

**Environment:** Chrome (latest), Windows

**Steps to Reproduce:**

1. Log in
2. Add the same product multiple times
3. Open Cart page

**Expected Result:**

* Quantity is displayed or duplicates are clearly managed

**Actual Result:**

* Identical products appear as separate entries without quantity context

**Business Impact:**
Creates confusion around pricing and order composition.

---

### BUG-04 – Credit card number is displayed in plain text in purchase confirmation

**Related Scenario:** TS-11
**Related Test Case:** TC-06

**Severity:** Critical
**Priority:** High

**Environment:** Chrome (latest), Windows

**Steps to Reproduce:**

1. Log in to the application
2. Add a product to the cart
3. Open Cart page
4. Click "Place Order"
5. Fill in the checkout form, including the Credit Card field
6. Complete the purchase

**Expected Result:**

* Sensitive payment data (credit card number) should be masked or not displayed at all in confirmation messages

**Actual Result:**

* Credit card number is displayed in plain text in the purchase confirmation window

**Business Impact:**
Critical security and data privacy issue. Exposes sensitive payment information to shoulder surfing, screenshots, or logging, potentially violating data protection standards and severely impacting user trust.

---

### BUG-05 – Checkout is accessible for non-authenticated users

**Related Scenario:** TS-14
**Related Test Case:** TC-09

**Severity:** High
**Priority:** Medium

**Environment:** Chrome (latest), Windows

**Steps to Reproduce:**

1. Do not log in
2. Add a product to the cart
3. Open Cart page
4. Click "Place Order"

**Expected Result:**

* User is prompted to log in or checkout is restricted

**Actual Result:**

* Checkout modal is accessible without authentication

**Business Impact:**
Breaks expected business rules and may lead to anonymous or untraceable orders.

---

### BUG-06 – Checkout modal does not enforce input format consistency

**Related Scenario:** TS-13
**Related Test Case:** TC-08

**Severity:** Medium
**Priority:** Medium

**Environment:** Chrome (latest), Windows

**Steps to Reproduce:**

1. Log in
2. Add product to cart
3. Open checkout modal
4. Enter numeric values in name or country fields
5. Complete purchase

**Expected Result:**

* Input format validation should be enforced

**Actual Result:**

* Order is accepted with clearly invalid field formats

**Business Impact:**
Leads to poor data quality and downstream processing issues.

---

### BUG-07 – User can initiate checkout with empty cart after cart manipulation

**Related Scenario:** TS-11
**Related Test Case:** TC-10

**Severity:** Medium
**Priority:** Medium

**Environment:** Chrome (latest), Windows

**Steps to Reproduce:**

1. Log in
2. Add product to cart
3. Remove product from cart
4. Click "Place Order"

**Expected Result:**

* Checkout should be disabled for empty cart

**Actual Result:**

* Checkout modal can still be opened

**Business Impact:**
Confusing user experience and unnecessary order attempts.

---

## 4. Notes

* All defects were identified through manual testing
* Severity reflects **impact on system and data integrity**
* Priority reflects **business urgency**

---

