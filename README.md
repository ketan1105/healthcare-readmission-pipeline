# 🏥 Healthcare Readmission Risk Pipeline

An industry-grade data engineering project using **PySpark** and **Google Cloud Platform (GCP)** to process real-world healthcare data and simulate readmission risk analytics. This project focuses on scalable **ETL with PySpark**, **Cloud Storage**, and **BigQuery**.

---

## 📌 Project Objective

To build a reliable data pipeline that processes electronic health record (EHR) data from hospitals to predict and analyze patient **readmission risk** based on demographic and clinical features.

---

## 🧰 Tech Stack

| Layer            | Tool / Service                     |
|------------------|-------------------------------------|
| Language         | Python (PySpark)                    |
| Cloud Platform   | Google Cloud Platform               |
| Storage          | Cloud Storage (GCS)                 |
| Data Processing  | PySpark (on Dataproc or locally)    |
| Data Warehouse   | BigQuery                            |
| Dashboard        | Looker Studio (or BigQuery SQLs)    |

---

## 📂 Project Structure

```
healthcare-readmission-pipeline/
├── data/ # Sample or test data (optional)
├── notebooks/ # Exploratory analysis (if any)
├── src/
│ ├── ingestion/ # PySpark scripts to read GCS data
│ ├── transformation/ # PySpark scripts for data cleaning
│ └── prediction/ # Logic for risk prediction
├── configs/ # Schema files, GCP paths
├── docs/ # Architecture diagrams, references
├── bigquery/ # SQL queries, table DDLs
├── requirements.txt # Python dependencies
└── README.md # This file

```


---

## 📊 Dataset

**Source:** [UCI Diabetes Readmission Dataset](https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008)  
- 100,000+ patient records  
- Includes demographics, diagnoses, medications, readmission info  
- Format: CSV

Uploaded to:

gs://<your-bucket-name>/raw_data/diabetes_readmission.csv


---

## 🔄 Data Flow Overview

1. **Raw Data Ingestion**  
   → From Cloud Storage to PySpark  

2. **Data Cleaning & Transformation**  
   → Null handling, feature engineering, value standardization  

3. **Risk Logic Inference**  
   → Rule-based logic (e.g. age + number of inpatient visits)  

4. **Data Sink**  
   → Write final output to **BigQuery**  

5. **Analysis & Reporting**  
   → Run SQL queries or build Looker dashboards

---

## 🚧 Work in Progress

| Phase | Description                             | Status     |
|-------|-----------------------------------------|------------|
| 1     | Setup GitHub repo and choose dataset    | ✅ Done     |
| 2     | Upload data to GCS                      | ⏳ In Progress |
| 3     | Write PySpark ingestion job             | ⏳ Next     |
| 4     | Data cleaning and transformation        |            |
| 5     | Add prediction logic                    |            |
| 6     | Write to BigQuery                       |            |
| 7     | Dashboarding with Looker Studio         |            |

---

## 📌 Author

**Ketan Jain**  
Data Engineer
[GitHub](https://github.com/ketan1105) • [LinkedIn](https://www.linkedin.com/in/ketan-jain-/)

---

## 📄 License

This project is licensed under the MIT License.
