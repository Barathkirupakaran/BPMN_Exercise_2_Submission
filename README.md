# Camunda BPMN & DMN Homework

![Camunda](https://img.shields.io/badge/Camunda-BPMN%20%7C%20DMN-blue)
![BPMN](https://img.shields.io/badge/Workflow-BPMN%202.0-orange)
![DMN](https://img.shields.io/badge/Decision%20Modeling-DMN-green)

## 📌 Overview

This repository contains the implementation of **BPMN 2.0 workflows and DMN decision tables using Camunda Modeler**.

The assignment focuses on applying business rules and decision logic to real-world workflow scenarios through process orchestration and decision automation.

---

## 📚 Exercises

### 🔹 Exercise 1 — Loan Application Risk Routing

An automated loan approval workflow that evaluates an applicant's:

* Applicant Age
* Credit Score
* Loan Amount

A **DMN decision table** determines the applicant's risk tier and whether manual review is required. The BPMN process then routes the application accordingly.

**Possible outcomes:**

| Risk Condition | Action                   |
| -------------- | ------------------------ |
| 🟢 LOW         | Auto-Approve & Disburse  |
| 🟡 MEDIUM      | Underwriter Review       |
| 🔴 HIGH        | Auto-Reject Notification |

**DMN:** `evaluate-loan-risk`

**Hit Policy:** Unique (U) / First (F)

---

### 🔹 Exercise 2 — Multi-Item Order Discount & Fulfillment

A dynamic order-processing workflow that calculates discounts based on:

* Customer Tier
* Cart Value
* Promotional Code

Multiple discount rules can be applied simultaneously using the **Collect Sum (C+)** hit policy.

The final invoice amount is calculated as:

```text
finalAmount = cartValue × (1 - totalDiscount / 100)
```

Orders with a final amount of **1000 or more** require manager approval before being sent to the warehouse.

**DMN:** `calculate-discounts`

**Hit Policy:** Collect Sum (C+)

**Sample Input:**

```text
Customer Tier : PREMIUM
Cart Value    : 600
Promo Code    : FESTIVE10
```

**Expected Total Discount:** `25%`

---

## 🛠️ Technologies Used

* **Camunda Modeler**
* **BPMN 2.0**
* **DMN**
* **FEEL Expressions**
* **Business Rule Tasks**
* **Exclusive Gateways**
* **Service Tasks**
* **User Tasks**

---

## 🎯 Learning Objectives

Through these exercises, the implementation demonstrates:

* Designing **BPMN 2.0 process workflows**
* Creating and configuring **DMN decision tables**
* Integrating DMN decisions with BPMN processes
* Using **Business Rule Tasks**
* Implementing **FEEL unary tests and expressions**
* Configuring **Exclusive Gateways**
* Working with different DMN **hit policies**
* Mapping DMN decision results into BPMN process variables

---


## 👨‍💻 Author

**Barathkirupakaran**

> Academic assignment demonstrating BPMN workflow orchestration and DMN-based business decision automation using Camunda.
