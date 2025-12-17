# Test Plan – Demoblaze Manual Testing

## 1. Introduction

This Test Plan describes the **manual testing strategy** applied to the *Demoblaze* e-commerce web application. The document outlines the scope, approach, risks, and quality criteria used to evaluate the application from a **business and user-impact perspective**.

The plan reflects a **realistic QA context**, with limited time, no backend access, and a focus on critical user journeys.

---

## 2. Objectives

The objectives of this testing effort are to:

* Validate **core e-commerce user flows** that impact conversion and user trust
* Identify **functional and usability defects** in high-risk areas
* Evaluate **data consistency and state management** (cart, session)
* Provide clear input for a **release decision** based on risk and defect severity

---

## 3. Application Overview

* **Application Name:** Demoblaze
* **Application Type:** Web-based e-commerce application
* **Testing Type:** Manual, black-box testing
* **Test Level:** System testing

---

## 4. Test Scope

### 4.1 In Scope

* User authentication (Sign up, Log in, Log out)
* Product catalog browsing and navigation
* Product details page behavior
* Cart management (add, remove, persistence)
* Order placement via checkout modal

### 4.2 Out of Scope

* Payment gateway validation (simulated behavior)
* Backend and database validation
* Performance, security, and accessibility testing
* Test automation activities

Scope decisions are driven by **business impact and testing priorities**, not by full feature coverage.

---

## 5. Test Approach

Testing will be conducted using a **risk-based approach**, combining scripted and exploratory testing techniques.

### 5.1 Test Types

* **Smoke Testing**
  Quick validation of application stability and availability of core features.

* **Functional Testing**
  Verification of expected behavior for core user flows and business rules.

* **Regression Testing**
  Re-validation of critical flows after identified issues or changes.

* **Exploratory Testing**
  Time-boxed sessions focused on high-risk areas to identify edge cases and unexpected behavior.

### 5.2 Prioritization Criteria

Testing priority is based on:

* Impact on checkout and revenue-related flows
* Risk of data loss or inconsistent state
* Frequency of user interaction

---

## 6. Risk Analysis

| Area            | Risk Description                             | Risk Level |
| --------------- | -------------------------------------------- | ---------- |
| Checkout flow   | Order placement with invalid or missing data | High       |
| Cart management | Cart data loss or inconsistent behavior      | High       |
| Authentication  | Session handling issues                      | Medium     |
| Product catalog | Incorrect product information                | Medium     |
| UI feedback     | Missing or unclear error messages            | Low        |

High-risk areas receive **deeper coverage and exploratory focus**.

---

## 7. Entry and Exit Criteria

### 7.1 Entry Criteria

* Application is accessible
* Core pages load without blocking errors
* Test environment is stable

### 7.2 Exit Criteria

* All planned test scenarios executed
* Critical and high-severity defects documented
* Test Summary Report completed
* Release recommendation provided

---

## 8. Test Deliverables

The following deliverables are produced during this testing effort:

* Test Scenarios
* Test Cases
* Bug Reports
* Exploratory Testing Notes
* Test Summary Report

All artifacts are stored in the project repository for traceability.

---

## 9. Test Environment

* **Browsers:** Google Chrome (latest), Mozilla Firefox (latest)
* **Operating System:** Windows
* **Test Data:** Public demo data and manually created user accounts

---

## 10. Roles and Responsibilities

* **QA Engineer:** Test design, execution, defect reporting, and test reporting

This project assumes a **single-QA ownership model**, common in small to mid-sized teams.

---

## 11. Assumptions and Constraints

* The application is a public demo and may behave inconsistently
* No access to source code, logs, or backend systems
* Limited control over test data persistence

These constraints are treated as part of the testing context.

---

## 12. Approval and Sign-off

This Test Plan is considered approved once test execution begins. Any scope changes or major deviations would be documented in the Test Summary Report.
