
# 🛒 E-Commerce Data Pipeline (No Kafka)

A near-real-time data engineering pipeline that simulates an e-commerce platform. It ingests, transforms, stores, and visualizes customer and sales data using modern data stack tools — **without using Kafka**.

---

## 📊 Project Overview

This project demonstrates an end-to-end data pipeline:

- 🔄 Simulates raw data (CSV) for orders, products, and users
- 📥 Ingests data into a database (PostgreSQL)
- 🔧 Transforms data using PySpark or dbt
- 🗃 Stores processed data in a warehouse (PostgreSQL / Parquet)
- 📈 Visualizes metrics using Apache Superset

---

## 🧱 Architecture

```

Simulated CSV Data
↓
Python Ingestion Scripts / Airflow DAGs
↓
Transformations (Spark or dbt)
↓
Storage (PostgreSQL + Parquet)
↓
Analytics Dashboard (Superset)

```

---

## 🛠️ Tech Stack

| Layer            | Tool                  |
|------------------|------------------------|
| Data Simulation   | Python                |
| Ingestion         | Python Scripts / Airflow |
| Processing        | PySpark or dbt        |
| Storage           | PostgreSQL, Parquet   |
| Orchestration     | Apache Airflow        |
| Visualization     | Apache Superset       |

---

## 📁 Project Structure

```

ecommerce-data-pipeline/
├── data/
│   ├── raw/
│   └── processed/
├── scripts/
│   ├── generate\_data.py
│   └── ingest\_to\_db.py
├── spark\_jobs/
│   └── transform\_orders.py
├── dags/
│   └── etl\_pipeline.py
├── dbt/
│   └── models/
├── dashboard/
│   └── screenshots/
└── README.md

````

---

## 🚀 Getting Started

### 1. Clone the Repo

```bash
git clone https://github.com/yourusername/ecommerce-data-pipeline.git
cd ecommerce-data-pipeline
````

### 2. Set Up the Environment

* Install Python 3.8+
* Install PostgreSQL (or use Docker)
* Install dependencies:

```bash
pip install -r requirements.txt
```

### 3. Run Data Simulation

```bash
python scripts/generate_data.py
```

This creates CSVs in `data/raw/`.

### 4. Ingest to PostgreSQL

```bash
python scripts/ingest_to_db.py
```

### 5. Run Transformations

**Using Spark:**

```bash
spark-submit spark_jobs/transform_orders.py
```

**Or using dbt:**

```bash
cd dbt
dbt run
```

### 6. Launch Dashboard

* Start Superset and connect to your PostgreSQL
* Build charts for:

  * Daily Revenue
  * Orders by Category
  * Top Customers

---

## 📷 Screenshots

Coming soon...

---

## 📌 Key Learnings

* Data ingestion with Python and PostgreSQL
* Transformation workflows with Spark/dbt
* Workflow automation using Airflow
* Real-time dashboarding with Superset

---

## 🧠 Future Enhancements

* Add Great Expectations for data quality checks
* Move storage to cloud (e.g., S3 + BigQuery)
* Automate end-to-end pipeline with Airflow

---

## 👨‍💻 Author

* [Hamza Bouali]([https://github.com/yourusername](https://github.com/Hamza-Bouali))
