
# Support_API — Paginated JSON Ingestion

This folder represents the **External Data Integration Layer** of the AetherStream Analytics Engineering system.

It simulates ingestion from a paginated support platform API using JSON files.

The goal is to practice recursive data retrieval and flattening of semi-structured sources using Power Query.

---

## 🎯 Purpose

- Simulate enterprise REST API consumption
- Practice recursive pagination
- Handle semi-structured JSON payloads
- Normalize ticket data into relational tables

This mirrors real-world ingestion from platforms such as:

- Customer support systems  
- SaaS applications  
- Operational APIs  

---

## 📦 Contents

Multiple paginated JSON files:

```

tickets_page_1.json
tickets_page_2.json
...
tickets_page_100.json

```

Each file contains:

- Ticket ID  
- User ID  
- Region  
- Sentiment indicator  
- Creation timestamp  

These files are treated as API responses.

---

## ⚙ Power Query Techniques Practiced

- `Json.Document`
- Recursive pagination using `List.Generate`
- Record expansion
- Table normalization
- Error handling with `try...otherwise`

The objective is to produce a single unified **Fact_SupportTickets** table.

---

## 🧠 Analytical Use Cases

After ingestion, ticket data supports:

- Sentiment scoring
- Regional support load analysis
- Churn risk indicators
- Operational KPI reporting

This data ultimately feeds the DAX and Predictive layers.

---

## 🧱 Architectural Position

```

ETL → Model → DAX → Predictive → Visualization

```

External APIs enter at this stage and become structured facts.

---

Author: **Shivansh Yadav**

---

