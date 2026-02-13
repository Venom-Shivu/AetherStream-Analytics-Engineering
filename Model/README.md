
# Model — Enterprise Relational Data Modeling (Power Pivot)

This folder represents the **Semantic Modeling Layer** of the AetherStream Analytics Engineering system.

All cleaned outputs from ETL are shaped here into a **Star Schema** and loaded into the **Power Pivot Data Model (VertiPaq)** to create a single source of truth.

This layer defines how the business is mathematically represented.

---

## 🎯 Primary Objectives

- Build dimensional models for analytics
- Separate Facts from Dimensions
- Enforce relationship directionality
- Optimize memory footprint
- Enable high-performance DAX calculations

This mirrors how enterprise BI systems are designed.

---

## 📐 Modeling Strategy

The model follows a classic **Star Schema**:

### Fact Tables
Contain measurable business events:

- Streaming sessions  
- Sales transactions  
- Hardware purchases  

Typical columns:

- Date  
- User_ID  
- Product_ID  
- Revenue  
- Quantity  

Facts remain narrow and numeric.

---

### Dimension Tables

Provide descriptive context:

- Dim_Date  
- Dim_User  
- Dim_Product  
- Dim_Region  

Dimensions contain:

- Human-readable attributes  
- Hierarchies  
- Sort keys  

Surrogate keys are hidden from report consumers.

---

## 🔗 Relationship Architecture

- Single-direction filters (Dimensions → Facts)
- Role-playing dates via inactive relationships
- Bridge tables for many-to-many scenarios
- Month-Year keys for mixed-granularity facts

No bi-directional chaos.

No circular dependencies.

---

## ⚡ Performance Optimization

This layer enforces:

- Column pruning before load
- Removal of unused attributes
- Binary workbook format (.xlsb)
- Numeric encoding where possible
- Minimal cardinality dimensions

The goal is:

✔ Sub-second Pivot refresh  
✔ Low VertiPaq memory usage  
✔ Stable DAX behavior  

---

## 🧠 Why This Layer Matters

DAX does not fix bad models.

Visuals do not fix bad models.

Everything downstream depends on this structure.

A correct model enables:

- Accurate churn metrics  
- Proper cohort analysis  
- Reliable forecasting  
- Scalable dashboards  

---

## 🧱 Architectural Position

```

ETL → Model → DAX → Predictive → Visualization

```

The Model layer is the analytical foundation.

---

Author: **Shivansh Yadav**

---

