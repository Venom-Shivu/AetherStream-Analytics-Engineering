# DAX — Analytical Metrics & Business Logic

This folder represents the **Computational Layer** of the AetherStream Analytics Engineering architecture.

All business metrics are defined here using **DAX (Data Analysis Expressions)** on top of the semantic model.

This layer converts raw facts into decision-ready intelligence.

---

## 🎯 Purpose of the DAX Layer

- Define North Star metrics
- Handle filter context explicitly
- Implement churn, retention, and LTV logic
- Support dynamic ranking and benchmarking
- Enable currency switching
- Produce executive-grade calculations

No transformations happen here.

DAX consumes the model and returns meaning.

---

## 📊 Metrics Engineered

Typical measures include:

- Monthly Total Users (MTU)
- Retention cohorts
- Fiscal Year-over-Year growth
- Lapsed user identification
- Top-N country ranking
- Semi-additive cash balances
- Global benchmark variance
- Rolling averages
- Cumulative run rates
- Complex churn calculations

All measures are context-aware and slicer responsive.

---

## 🧠 Core DAX Concepts Used

- CALCULATE + filter modifiers  
- VAR for readability and performance  
- ALL / ALLEXCEPT for benchmarking  
- USERELATIONSHIP for role-playing dates  
- LASTNONBLANK for semi-additive logic  
- SELECTEDVALUE for parameter switching  
- RANKX for dynamic rankings  
- EXCEPT for churn detection  

This mirrors professional BI implementations.

---

## ⚠ Design Rules

- No calculated columns unless unavoidable  
- Measures only (preferred)  
- Business logic lives here, not in Power Query  
- Variables used for complex expressions  
- Defensive coding for divide-by-zero scenarios  

---

## 🧱 Architectural Position

```

ETL → Model → DAX → Predictive → Visualization

```

Bad DAX exposes bad models.

Good DAX assumes clean dimensional design.

---

## 🎯 Outcome

This layer enables:

✔ Accurate KPI reporting  
✔ Cohort analysis  
✔ Revenue attribution  
✔ Executive dashboards  
✔ Scenario modeling  

---

Author: **Shivansh Yadav**

---
