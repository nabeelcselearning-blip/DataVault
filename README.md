# DataVault

**DataVault** is a Python-based ETL pipeline designed to process transaction data from CSV files and transform raw records into clean, validated, and analysis-ready datasets.

The project demonstrates core **Data Engineering concepts** including data ingestion, schema validation, data cleaning, duplicate detection, transformation, error handling, aggregation, and automated reporting.

## 🚀 Features

- **Data Ingestion** — Reads raw transaction data from CSV files.
- **Schema & Record Validation** — Checks incoming records against defined validation rules.
- **Data Cleaning** — Handles invalid, inconsistent, and incomplete records.
- **Duplicate Detection** — Identifies and handles duplicate transaction records.
- **Data Transformation** — Converts validated raw data into a structured format suitable for downstream use.
- **Error Handling** — Separates invalid records for controlled inspection instead of allowing them to affect the processed dataset.
- **Data Aggregation** — Generates customer- and product-level metrics.
- **Automated Reporting** — Produces summary reports from processed transaction data.

## 🔄 ETL Pipeline

```text
Raw CSV Data
     │
     ▼
┌───────────────┐
│   Ingestion    │
└───────┬───────┘
        ▼
┌───────────────┐
│  Validation    │
│ Schema + Data  │
└───────┬───────┘
        ▼
┌───────────────┐
│ Data Cleaning  │
│ & Deduplication│
└───────┬───────┘
        ▼
┌───────────────┐
│ Transformation │
└───────┬───────┘
        ▼
┌────────────────┐
│ Processed Data │
└────────┬───────┘
         ▼
┌────────────────┐
│  Aggregation & │
│    Reporting   │
└────────────────┘

Invalid Records ──► Error / Rejected Records
```

## 📊 Generated Insights

The pipeline produces aggregated metrics that can be used for downstream analysis, including:

- Total revenue
- Average transaction value
- Customer-level transaction summaries
- Product-level transaction summaries
- Processed and rejected record counts

## 🛠️ Tech Stack

- **Python**
- **Pandas**
- **CSV**
- **Git & GitHub**

## 📁 Project Structure

```text
DataVault/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── src/
│   ├── ingestion.py
│   ├── validation.py
│   ├── cleaning.py
│   ├── transformation.py
│   └── reporting.py
│
├── output/
│
├── requirements.txt
├── README.md
└── main.py
```

> The project structure may vary depending on the current implementation.

## ⚙️ How to Run

### 1. Clone the repository

```bash
git clone https://github.com/nabeelcselearning-blip/DataVault.git
cd DataVault
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it:

**Windows**

```bash
venv\Scripts\activate
```

**macOS / Linux**

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the pipeline

```bash
python main.py
```

The pipeline will process the input transaction data and generate the corresponding processed datasets and reports.

## 🎯 Project Objectives

DataVault was built to demonstrate practical understanding of the fundamental stages involved in a data pipeline:

1. Ingest raw data.
2. Validate incoming records.
3. Identify and handle data-quality issues.
4. Clean and transform valid data.
5. Separate rejected records for controlled error handling.
6. Generate aggregated datasets and reports.

## 🔮 Future Improvements

Potential extensions to the project include:

- Replace CSV ingestion with a relational database.
- Add SQL-based transformations and analytics.
- Introduce Apache Airflow for workflow orchestration.
- Add automated data-quality tests.
- Containerize the pipeline using Docker.
- Add cloud-based storage and processing.
- Implement structured logging and pipeline monitoring.
- Add CI/CD using GitHub Actions.

## 👨‍💻 Author

**Nabeel Islam**

B.Tech — Computer Science & Engineering

GitHub: [nabeelcselearning-blip](https://github.com/nabeelcselearning-blip)

---

> **DataVault** is an educational Data Engineering project focused on building a reliable and structured ETL workflow for transaction data.
