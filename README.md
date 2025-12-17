# Demoblaze – Manual QA Project (Mid–Senior Level)

## 1. Project Overview

This repository contains a **manual QA testing project** for the *Demoblaze* demo e‑commerce application. The project simulates real-life QA activities performed during a manual testing phase within a product team, with a strong focus on **business-critical flows, risk-based testing, and quality reporting**.

The purpose of this project is not to exhaustively test every feature, but to demonstrate a **professional QA mindset**: prioritization, structured documentation, clear communication, and decision-making based on risk and business impact.

Target audience:

* QA Leads / Hiring Managers
* Recruiters evaluating mid–senior QA profiles
* QA Engineers looking for a realistic reference project

---

## 2. Application Under Test (AUT)

* **Name:** Demoblaze
* **Type:** Web-based e-commerce application
* **URL:** [https://www.demoblaze.com/](https://www.demoblaze.com/)

### Core Features:

* User authentication (Sign up / Log in)
* Product catalog browsing
* Product details view
* Cart management
* Order placement via checkout modal

The application is treated as a **black-box system**, similar to how a QA team would test a third-party or externally delivered product.

---

## 3. Testing Objectives

The main objectives of this testing effort are:

* Validate **core business flows** that directly impact user experience and conversion
* Identify **functional, usability, and data integrity issues**
* Assess **risk areas** such as cart persistence and checkout behavior
* Provide clear and actionable **bug reports and test documentation**

This project intentionally prioritizes **quality over quantity**.

---

## 4. Testing Scope

### In Scope:

* Authentication (Sign up / Log in / Log out)
* Product catalog and product details
* Add to cart / remove from cart
* Cart persistence during navigation
* Order placement (checkout form behavior)

### Out of Scope:

* Payment gateway validation (mocked behavior)
* Backend/database validation
* Performance and security testing
* UI automation (covered in a separate project)

Scope decisions are based on **time constraints and business impact**, mirroring a real project context.

---

## 5. Testing Approach

The testing approach follows **risk-based manual testing**, combining structured and exploratory techniques:

* **Smoke Testing** – to validate basic application stability
* **Functional Testing** – focused on core user journeys
* **Regression Testing** – applied to critical flows
* **Exploratory Testing** – used to uncover edge cases and hidden risks

Higher priority is given to flows that affect:

* Revenue (checkout, cart)
* User data integrity
* Session and state management

---

## 6. Test Artifacts

This repository contains the following QA deliverables:

* **Test Plan** – defines scope, risks, strategy, and entry/exit criteria
* **Test Scenarios** – business-oriented scenarios derived from user flows
* **Test Cases** – detailed positive, negative, and edge case validations
* **Bug Reports** – documented issues with clear reproduction steps and impact
* **Exploratory Testing Notes** – findings from unscripted testing sessions
* **Test Summary Report** – final quality assessment and release recommendation

Each artifact is stored in a dedicated directory for clarity and traceability.

---

## 7. Test Environment

* **Browsers:** Google Chrome (latest), Mozilla Firefox (latest)
* **Operating System:** Windows
* **Test Data:** Public demo data and manually created user accounts

No test data is persisted or reused beyond the scope of this project.

---

## 8. Assumptions and Constraints

* The application behavior may be unstable or inconsistent, as it is a demo environment
* No access to application logs, backend, or database
* Limited control over test data persistence

These constraints are treated as **real-world limitations**, similar to many QA projects.

---

## 9. Quality Criteria

Quality is evaluated based on:

* Correctness of core functionality
* Data consistency across user actions
* Usability and error handling
* Impact and severity of identified defects

A release recommendation is provided in the **Test Summary Report** based on these criteria.

---

## 10. How to Use This Repository

1. Start with the **Test Plan** to understand the strategy and scope
2. Review **Test Scenarios** to see business-level coverage
3. Dive into **Test Cases** for detailed validations
4. Analyze **Bug Reports** to assess defect quality and impact
5. Read **Exploratory Notes** for risk insights
6. Conclude with the **Test Summary Report** for final assessment

---

## 11. Author Notes

This project is designed to reflect how a **QA engineer** approaches manual testing in a professional environment:

* Focus on business value
* Clear prioritization
* Strong documentation and communication

The structure and content of this repository are intentionally kept stable throughout the project lifecycle to reflect disciplined QA practices.
