# Hybrid Sales Anomaly Detection & Alerting System

An end-to-end data analytics and machine learning project that detects unusual sales transactions using a combination of business rules, statistical methods, and Isolation Forest.

The project is designed to simulate a real-world business monitoring system where suspicious sales, extreme discounts, abnormal quantities, and severe profit losses are automatically identified before they become larger operational problems.

---

## Project Overview

Businesses often identify abnormal sales behaviour only after periodic reporting or manual review.

This project solves that problem by building an automated anomaly detection pipeline that:

- cleans messy retail transaction data
- performs feature engineering
- detects anomalies using business rules
- applies statistical methods such as IQR and Z-score
- uses Isolation Forest for unsupervised anomaly detection
- combines multiple signals into a hybrid risk score
- assigns anomaly severity
- explains why each transaction was flagged
- recommends an appropriate business action
- displays results in an interactive Streamlit dashboard
- evaluates model performance using known synthetic anomaly labels

---

## Business Problem

Sales datasets may contain unusual patterns such as:

- extremely high or low sales
- excessive discounts
- large negative profits
- unusually high quantities
- suspicious combinations of high sales and large discounts
- abnormal transactions compared with typical business behaviour

If these anomalies are not detected quickly, they may indicate:

- pricing errors
- incorrect discounts
- operational mistakes
- unusual customer activity
- margin leakage
- data-quality problems
- potential fraud or transaction issues

The objective of this project is to automatically identify these patterns and prioritize them for review.

---

## Solution Architecture

```text
Raw Sales CSV
      |
      v
Data Cleaning
      |
      v
Feature Engineering
      |
      v
Business Rules
      |
      +------------------+
      |                  |
      v                  v
     IQR               Z-Score
      |                  |
      +--------+---------+
               |
               v
        Isolation Forest
               |
               v
        Hybrid Risk Score
               |
               v
     Severity Classification
               |
               v
       Anomaly Explanation
               |
               v
      Recommended Action
               |
               v
      Streamlit Dashboard
