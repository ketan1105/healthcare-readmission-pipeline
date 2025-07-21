# 🏥 Healthcare Readmission Risk Pipeline

An industry-grade data engineering project using **PySpark DataFrame API** and **Google Cloud Platform (GCP)** to process real-world healthcare data and simulate readmission risk analytics. This project focusing purely on scalable ETL using native PySpark.

---

## 📌 Project Objective

To build a reliable data pipeline that processes electronic health record (EHR) data from hospitals using **PySpark's DataFrame API** for transformations and logic, and stores the processed data in BigQuery for analysis.

---

## 🧰 Tech Stack

| Layer            | Tool / Service                          |
|------------------|------------------------------------------|
| Language         | Python (PySpark)                         |
| Cloud Platform   | Google Cloud Platform (GCP)              |
| Storage          | Cloud Storage (GCS)                      |
| Data Processing  | PySpark DataFrame API (no Spark SQL)     |
| Data Warehouse   | BigQuery                                 |
| Dashboard        | Looker Studio (or BigQuery SQL)          |

---

## 📂 Project Structure


```
healthcare-readmission-pipeline/
├── data/ # Sample or test data (optional)
├── notebooks/ # Exploratory analysis (if any)
├── src/
│ ├── ingestion/
│ │ └── ingest_gcs.py # Read from Cloud Storage
│ ├── transformation/
│ │ ├── clean.py # Data cleaning and casting
│ │ └── feature_engineering.py # Add age groups, encounter flags, etc.
│ ├── prediction/
│ │ └── risk_scoring.py # Rule-based risk classification
│ └── pipeline_runner.py # Executes full pipeline
├── configs/ # GCP paths, schema definitions
├── bigquery/ # BQ schema files or queries
├── docs/ # Architecture diagrams
├── requirements.txt # Python dependencies
└── README.md # This file

```

---

## 📊 Dataset

**Source:** [UCI Diabetes Readmission Dataset](https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008)  
- 100,000+ patient records  
- CSV format  
- Includes demographics, diagnoses, hospital encounters, and readmission info

📁 Uploaded to:


gs://healthcare-readmission-pipeline-data/raw_data/diabetes_readmission.csv



---

## 🔄 Data Flow

Cloud Storage (CSV) → PySpark DataFrame API (ETL) → BigQuery


---

## 🔧 Core Transformation Example

```python
from pyspark.sql.functions import when, col

df = df.withColumn(
    "readmission_risk",
    when(col("number_inpatient") > 2, "HIGH")
    .when((col("number_emergency") > 1) & (col("age").like("70-80%")), "MEDIUM")
    .otherwise("LOW")
)
```

🧠 Key Steps in Pipeline
1. Ingestion
Load raw CSV from Cloud Storage into a Spark DataFrame

2. Cleaning
Drop nulls, cast column types, and standardize formats

3. Feature Engineering
Create new fields like age groups, encounter counts, etc.

4. Readmission Risk Logic
Apply conditional rules using withColumn() and when()

5. Output to BigQuery
Write final DataFrame into a BigQuery table

## 🚧 Work in Progress

| Phase | Description                     | Status        |
| ----- | ------------------------------- | ------------- |
| 1     | Setup GitHub repo and structure | ✅ Done        |
| 2     | Upload dataset to Cloud Storage | ⏳ In Progress |
| 3     | PySpark ingestion and cleaning  | ⏳ Upcoming    |
| 4     | Feature engineering             |               |
| 5     | Readmission scoring             |               |
| 6     | BigQuery output                 |               |
| 7     | Dashboarding                    |               |


---

## 📌 Author

**Ketan Jain**  
Data Engineer
[GitHub](https://github.com/ketan1105) • [LinkedIn](https://www.linkedin.com/in/ketan-jain-/)

---

## 📄 License

This project is licensed under the MIT License.
