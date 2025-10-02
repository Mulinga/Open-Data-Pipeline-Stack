# Open Data Pipeline Stack

An **open-source data engineering workflow** inspired by Twiga's analytics stack.  
This repository documents an end-to-end data pipeline architecture using **Apache + open-source tools** for scalable, reliable, and real-time analytics.

---

## 📊 Architecture Overview

The pipeline follows the **Data Engineering Lifecycle**:

1. **Change Data Capture (CDC)** → [Debezium](https://debezium.io/)  
2. **Data Streaming** → [Apache Kafka](https://kafka.apache.org/)  
3. **Data Storage** → [Apache Iceberg](https://iceberg.apache.org/) + [Google Cloud Storage](https://cloud.google.com/storage)  
4. **Data Transformation** → [DBT](https://www.getdbt.com/)  
5. **Data Querying** → [Apache Trino](https://trino.io/)  
6. **Data Reporting** → [Apache Superset](https://superset.apache.org/) + [Apache OpenWhisk](https://openwhisk.apache.org/)  
7. **Data Orchestration** → [Apache Airflow](https://airflow.apache.org/)

---

## 🛠️ Tools & Responsibilities

| Stage                | Tool(s) Used                     | Responsibilities |
|-----------------------|----------------------------------|------------------|
| **Data Capture**      | Debezium + PostgreSQL            | Real-time CDC (insert, update, delete) |
| **Data Streaming**    | Kafka                           | Event distribution to downstream systems |
| **Data Storage**      | Apache Iceberg + GCP            | Scalable, schema-evolving storage |
| **Transformation**    | DBT                             | SQL-based transformations, layered models |
| **Querying**          | Trino                           | Distributed SQL across data sources |
| **Reporting**         | OpenWhisk + Superset            | Automated reports, dashboards |
| **Orchestration**     | Airflow                         | Workflow scheduling, monitoring |

---

## 📐 Workflow Diagram

![Data Engineering Workflow](images/stack.png)

---

## 🚀 Getting Started

### Prerequisites
- [Docker](https://www.docker.com/) or Kubernetes for deployments
- Basic knowledge of **SQL** & **Python**
- A cloud provider (Google Cloud recommended) for storage

### Setup
```bash
# Clone this repository
git clone https://github.com/your-username/open-data-pipeline-stack.git
cd open-data-pipeline-stack
