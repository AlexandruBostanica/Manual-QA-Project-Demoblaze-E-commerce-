# Exploratory Testing Notes – Demoblaze Manual QA Project

## 1. Purpose

This document captures the results of **exploratory testing sessions** performed on the *Demoblaze* e-commerce application. Exploratory testing was conducted to complement scripted test cases and identify **edge cases, usability issues, and hidden risks** that may not be evident through predefined scenarios.

The focus is on **risk discovery and quality insight**, not exhaustive defect enumeration.

---

## 2. Exploratory Testing Approach

Exploratory testing sessions were:

* **Time-boxed** (30–45 minutes per session)
* Conducted after execution of high-priority test cases
* Focused on areas with **higher business and technical risk**

Testing combined free exploration with lightweight charters to maintain direction while allowing flexibility.

---

## 3. Exploratory Test Charters

### Charter 1 – Cart State and Consistency

**Objective:** Explore cart behavior during rapid or unexpected user actions.

**Areas Explored:**

* Adding and removing products repeatedly
* Rapid navigation between catalog and cart
* Page refresh during cart manipulation

**Findings:**

* Temporary UI misalignment when multiple cart actions are performed quickly
* Duplicate products displayed without quantity indicators

**Risk Identified:**

* User confusion and potential pricing misunderstandings

---

### Charter 2 – Checkout Flow Robustness

**Objective:** Assess checkout behavior under incomplete or unusual user input.

**Areas Explored:**

* Closing checkout modal mid-process
* Submitting checkout with partial data
* Entering unexpected input formats

**Findings:**

* Checkout allows submission with incomplete mandatory data
* Limited input format validation across fields

**Risk Identified:**

* Data integrity issues and fulfillment problems

---

### Charter 3 – Session and Authentication Boundaries

**Objective:** Evaluate session handling during cart and checkout actions.

**Areas Explored:**

* Logging out during cart usage
* Attempting checkout without authentication
* Session continuation across navigation

**Findings:**

* Checkout accessible without enforced authentication

**Risk Identified:**

* Weak enforcement of business rules and access control

---

### Charter 4 – Security and Data Exposure Awareness

**Objective:** Observe handling of sensitive user data during checkout and confirmation.

**Areas Explored:**

* Visibility of payment-related information
* Confirmation dialogs and messages
* UI exposure of sensitive fields

**Findings:**

* Credit card number displayed in plain text in purchase confirmation

**Risk Identified:**

* Critical data privacy and security risk

---

## 4. General Observations

* Application behavior is inconsistent under non-linear user actions
* Validation is primarily superficial, focused on minimal flow completion
* UX feedback is limited in edge and error scenarios
  n

---

## 5. Exploratory Testing Value

Exploratory testing contributed to:

* Identification of **high-impact defects** not obvious in scripted testing
* Better understanding of **system behavior under stress and misuse**
* Validation of risk assumptions defined in the Test Plan

---

## 6. Recommendations

* Strengthen validation rules in checkout flow
* Improve cart state handling and visual feedback
* Mask or remove sensitive data from UI confirmation messages
* Continue exploratory testing after fixes to verify system robustness

---

