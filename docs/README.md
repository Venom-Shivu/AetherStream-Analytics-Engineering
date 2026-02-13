# Capstone Architecture — AetherStream Analytics Engineering

This document describes the **end-to-end system architecture** of the AetherStream Analytics Engineering framework.

The project is designed to simulate how real organizations build analytics platforms — from raw data ingestion to executive decision support.

---

## 🧭 System Overview

The architecture follows a layered analytical pipeline:



Raw Sources
↓
ETL (Power Query)
↓
Semantic Model (Power Pivot / Star Schema)
↓
DAX Metrics Engine
↓
Predictive Analytics
↓
Executive Dashboards

```

Each layer has a single responsibility.

No shortcuts.

---

## 📐 Architectural Layers

### 1. ETL Layer

Responsible for:

- Folder-based ingestion (CDN logs)
- JSON parsing (device metadata, support tickets)
- Type enforcement
- Data cleansing
- Schema normalization

All transformations are reproducible and automated.

---

### 2. Modeling Layer

Implements:

- Star schema design
- Fact / Dimension separation
- Surrogate keys
- Role-playing dates
- Bridge tables for many-to-many relationships

This layer establishes the **Single Source of Truth**.

---

### 3. DAX Layer

Defines all business logic:

- Churn
- Retention
- LTV
- Fiscal YoY growth
- MTU
- Top-N rankings
- Benchmark variance
- Semi-additive balances

Metrics are context-aware and slicer responsive.

---

### 4. Predictive Layer

Introduces statistical intelligence:

- Regression modeling
- Monte Carlo simulations
- Forecasting
- SPC control charts
- Outlier detection
- Optimization via Solver

This layer supports forward-looking decision making.

---

### 5. Visualization Layer

Final delivery includes:

- Executive KPI dashboards
- Scenario toggles
- Sparklines
- Drill-through reports
- Accessibility-aware color palettes
- Automated PDF exports

Design follows high data-ink ratio principles.

---

## 🎯 Design Principles

- Separation of concerns
- Reproducible transformations
- Dimensional modeling over flat tables
- Measures over calculated columns
- Predictive transparency (no black boxes)
- Performance-first mindset

---

## 🚀 Outcome

This architecture enables:

✔ Scalable analytics  
✔ Accurate business metrics  
✔ Predictive insight  
✔ Executive-grade reporting  

It mirrors professional Analytics Engineering systems used in industry.

---

Author: **Shivansh Yadav**

---

