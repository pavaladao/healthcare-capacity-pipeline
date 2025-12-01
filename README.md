````markdown
# 🏥 Healthcare Hospital Capacity Data Pipeline

This project implements an end-to-end data pipeline to collect, clean, model, and visualize U.S. hospital capacity metrics using real open government data. The final deliverable is an interactive dashboard enabling analysis of bed utilization over time to support public health decision-making.

> This repository is part of a broader data engineering & analytics portfolio focused on real-world datasets and modern data stack practices.

---

## 🎯 Objective

Build a scalable data pipeline capable of:

1. **Ingesting** raw hospital capacity data directly from U.S. open data APIs  
2. **Transforming and validating** the data using optimized analytical formats  
3. **Modeling** dimensions and fact tables for efficient reporting  
4. **Visualizing** key indicators through an interactive dashboard

---

## 🧱 Architecture Overview

The project follows a **Bronze → Silver** data architecture:

```mermaid
graph TD
    A[HealthData.gov API] -->|Ingestion| B[Bronze Layer - Parquet]
    B -->|Transform/Clean| C[Silver Layer - DuckDB]
    C -->|Analytics| D[Streamlit Dashboard]
````

---

## 📊 Dataset

* **Source:** U.S. Department of Health & Human Services — HealthData.gov
* **Theme:** Weekly reported hospital patient impact & bed capacity
* **Fields examples:**

  * Staffed beds
  * Beds occupied
  * ICU beds
  * COVID-19 patient impact
  * Hospital geolocation (State, County, Facility ID)

The dataset is updated continuously from official U.S. hospital reporting.

🔗 Final dataset/API link will be added upon pipeline configuration.

---

## 🛠️ Tech Stack

| Component                  | Technology             |
| -------------------------- | ---------------------- |
| Language                   | Python                 |
| Orchestration              | Prefect                |
| Data Lake                  | Parquet + partitioning |
| Data Warehouse (Analytics) | DuckDB                 |
| Dashboard                  | Streamlit + Plotly     |
| Version Control            | Git & GitHub           |

---

## 🔍 Key Features

✔ Automated ingestion pipeline
✔ Incremental and structured data storage
✔ Fact/dimension modeling for analytical queries
✔ Interactive insights for U.S. public health monitoring
✔ Fully reproducible environment

---

## 📈 KPIs (MVP)

* Bed occupancy (%) per state/hospital
* ICU stress evolution over time
* Top hospitals by average utilization
* U.S. heatmap by capacity indicators *(coming soon)*

---

## 🚀 How to Run Locally

```bash
# Install dependencies
pip install -r requirements.txt

# Run ingestion pipeline
python -m flows.ingest

# Build the analytical warehouse
python -m flows.build_warehouse

# Launch dashboard
streamlit run dashboards/app.py
```

---

## 📁 Repository Structure

```text
│
├── data/
│   ├── raw/
│   ├── bronze/
│   └── warehouse.duckdb
│
├── flows/
├── src/
│   ├── ingestion/
│   ├── transforms/
│   └── utils/
│
├── dashboards/
└── notebooks/
```

---

## 📌 Roadmap

| Status | Milestone                       |
| ------ | ------------------------------- |
| 🟡     | API ingestion + Bronze Parquet  |
| ⚪      | Silver warehouse in DuckDB      |
| ⚪      | Streamlit dashboard             |
| ⚪      | Cloud deployment                |
| ⚪      | Additional U.S./Brazil datasets |

---

## 🎓 Skills Demonstrated

* Data engineering and orchestration
* Data modeling (Dimensional / Star schema)
* Public health data analysis
* Visualization and product thinking
* Modern data stack technologies

---

## 🤝 Contributions

Suggestions and improvements are welcome!
Future enhancements include:

* Validation with Pandera or Great Expectations
* Monitoring and CI/CD automation
* Geospatial analytics
* Comparison between U.S. and Brazil hospital systems

---

## 👤 Author

**Pedro Valadão**
M.S. Computer Science Candidate — U.S. (2026)
Focus: Data Engineering • Applied Data Science • AI Automation

```

Me confirma: quer que eu já **crie os primeiros arquivos do projeto** e te entregue?
```
