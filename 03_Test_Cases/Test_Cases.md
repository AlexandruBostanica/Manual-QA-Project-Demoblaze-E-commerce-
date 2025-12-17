# Test Cases – Demoblaze Manual Testing

## 1. Purpose

This document contains **detailed manual test cases** derived from the highest‑risk test scenarios defined in the *Test Scenarios* document. The focus is on **negative paths, edge cases, and state-related behavior**, while still validating essential positive flows.

The goal is to ensure **depth of coverage** for business‑critical functionality rather than exhaustive validation of all scenarios.

---

## 2. Scope of Test Cases

Test cases are created for the following scenarios:

* TS‑07 – TS‑10 (Cart Management)
* TS‑11 – TS‑15 (Checkout & Order Placement)

Lower‑risk scenarios are covered through exploratory testing and are not expanded into scripted test cases.

---

## 3. Test Case Format

Each test case includes:

* **ID**
* **Related Scenario**
* **Description**
* **Preconditions**
* **Test Steps**
* **Expected Result**
* **Priority**

---

## 4. Cart Management Test Cases

### TC‑01 – Add product to cart (positive flow)

**Scenario:** TS‑07
**Description:** Verify that a product is successfully added to the cart.

**Preconditions:** User is logged in.

**Steps:**

1. Navigate to product catalog
2. Select a product
3. Click "Add to cart"
4. Open Cart page

**Expected Result:**

* Product is displayed in the cart with correct name and price

**Priority:** High

---

### TC‑02 – Add same product multiple times

**Scenario:** TS‑08
**Description:** Verify cart behavior when the same product is added repeatedly.

**Preconditions:** User is logged in.

**Steps:**

1. Navigate to a product details page
2. Click "Add to cart" multiple times
3. Open Cart page

**Expected Result:**

* Cart reflects consistent behavior (either multiple entries or quantity handling)
* No incorrect pricing or duplicated inconsistencies

**Priority:** High

---

### TC‑03 – Rapid multiple clicks on "Add to cart" button

**Scenario:** TS‑08
**Description:** Verify system stability during rapid user interaction.

**Preconditions:** User is logged in.

**Steps:**

1. Navigate to a product details page
2. Rapidly click "Add to cart" multiple times
3. Open Cart page

**Expected Result:**

* Cart does not enter an inconsistent state
* No application errors occur

**Priority:** High

---

### TC‑04 – Remove product from cart

**Scenario:** TS‑09
**Description:** Verify that a product can be removed from the cart.

**Preconditions:** Cart contains at least one product.

**Steps:**

1. Open Cart page
2. Click "Delete" for a product

**Expected Result:**

* Product is removed
* Cart total is updated correctly

**Priority:** High

---

### TC‑05 – Cart persistence after page refresh

**Scenario:** TS‑10
**Description:** Verify that cart contents persist after browser refresh.

**Preconditions:** Cart contains at least one product.

**Steps:**

1. Open Cart page
2. Refresh browser

**Expected Result:**

* Cart contents remain unchanged

**Priority:** High

---

## 5. Checkout and Order Placement Test Cases

### TC‑06 – Successful order placement (positive flow)

**Scenario:** TS‑11
**Description:** Verify that a logged‑in user can place an order with valid data.

**Preconditions:** User is logged in and cart contains products.

**Steps:**

1. Open Cart page
2. Click "Place Order"
3. Fill all mandatory fields with valid data
4. Confirm order

**Expected Result:**

* Order confirmation message is displayed

**Priority:** High

---

### TC‑07 – Attempt checkout with empty mandatory fields

**Scenario:** TS‑12
**Description:** Verify validation when required checkout fields are empty.

**Preconditions:** User is logged in and cart contains products.

**Steps:**

1. Open checkout modal
2. Leave mandatory fields empty
3. Click "Purchase"

**Expected Result:**

* User receives validation feedback
* Order is not placed

**Priority:** High

---

### TC‑08 – Checkout with invalid input data

**Scenario:** TS‑13
**Description:** Verify behavior when invalid data is entered in checkout form.

**Preconditions:** User is logged in and cart contains products.

**Steps:**

1. Open checkout modal
2. Enter special characters or excessively long strings
3. Click "Purchase"

**Expected Result:**

* Invalid input is rejected or handled gracefully
* No application crash

**Priority:** High

---

### TC‑09 – Checkout attempt by non‑authenticated user

**Scenario:** TS‑14
**Description:** Verify system behavior when a non‑logged‑in user attempts checkout.

**Preconditions:** User is not logged in and cart contains products.

**Steps:**

1. Open Cart page
2. Click "Place Order"

**Expected Result:**

* System restricts checkout or prompts authentication

**Priority:** High

---

### TC‑10 – Interrupt checkout process

**Scenario:** TS‑15
**Description:** Verify system behavior when checkout is interrupted.

**Preconditions:** User is logged in and cart contains products.

**Steps:**

1. Open checkout modal
2. Close modal or refresh page before confirming order
3. Reopen Cart page

**Expected Result:**

* Cart remains in a consistent state
* No partial or unintended order is created

**Priority:** High

---

## 6. Notes

* Expected results describe **intended behavior**, not necessarily current system behavior
* Any deviation is documented as a bug
* Additional edge cases are covered during exploratory testing

---

