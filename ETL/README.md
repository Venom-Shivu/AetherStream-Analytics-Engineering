# ETL — High-Scale Data Ingestion (Power Query)

This folder represents the **Extraction & Transformation layer** of the AetherStream Analytics Engineering pipeline.

All raw enterprise data enters the system here and is standardized using **Power Query (M Language)** before being loaded into the analytical model.

The objective of this layer is:

- Normalize inconsistent formats  
- Remove noise and malformed records  
- Enforce data types  
- Flatten semi-structured sources  
- Produce analysis-ready tables for the Data Model  

This mirrors real-world production ETL pipelines.

---

## 📂 Folder Structure

```

ETL/
│
├── CDN_logs/
│
└── device_json/

```

---

## 📁 CDN_logs

Multi-region CDN traffic exports used to simulate **high-volume log ingestion**.

### Typical Use Cases

- Folder-based ingestion (`Get Data → From Folder`)
- Automatic file consolidation
- Timestamp standardization (US / UK formats)
- Internal IP filtering
- Scientific notation cleanup
- Latency cleansing with error handling

### Represents

Enterprise telemetry pipelines such as:

- CDN traffic
- Server access logs
- Application performance metrics

These files are designed for:

✅ Folder combine logic  
✅ Type coercion  
✅ Sampling strategies  
✅ Large-scale Power Query transformations  

---

## 📁 device_json

Nested JSON files containing simulated user device metadata.

### Typical Use Cases

- Recursive folder ingestion
- JSON.Document parsing
- Record expansion
- Column flattening
- Schema normalization

### Represents

Semi-structured sources such as:

- Mobile device telemetry  
- IoT payloads  
- Support platform exports  

Used to practice:

✅ JSON flattening  
✅ Nested record expansion  
✅ Relational shaping  

---

## ⚙ ETL Design Principles

This layer follows professional standards:

- Raw data is never manually edited  
- All transformations are reproducible  
- Queries load as **Connection Only + Data Model**  
- No business logic is applied here (metrics belong in DAX)  
- Columns are trimmed early to reduce memory footprint  

Power Query acts as a **functional pipeline**, ensuring deterministic outputs and full data lineage.

---

## 🎯 Role in Overall Architecture

ETL feeds directly into:

```

ETL → Model → DAX → Predictive → Visualization

```

Bad ETL = broken analytics.

This folder exists to guarantee:

✔ Clean inputs  
✔ Stable schemas  
✔ Scalable modeling  

---

Author: **Shivansh Yadav**

