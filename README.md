# 🏥 Healthcare Analytics Pipeline using PySpark on GCP

## 📌 Project Overview

This project is designed to showcase **end-to-end data engineering capabilities** using **PySpark on Google Cloud Platform (GCP)** in the **healthcare domain**. It focuses on the scalable transformation and analysis of electronic health record (EHR) data to derive meaningful insights for healthcare stakeholders.

All transformations, analytics, and data processing are handled using the **PySpark DataFrame API** 
---

## 📊 Dataset

- **Source**: UCI Machine Learning Repository
- **Dataset**: Diabetes 130-US hospitals for years 1999–2008
- **Format**: CSV
- **File Size**: ~50 MB
- **Bucket Path**: `gs://healthcare-readmission-pipeline-data/raw_data/diabetes.csv`

This dataset includes over 100,000 de-identified patient records with information on demographics, diagnoses, procedures, medications, and readmission outcomes.

---

## ⚙️ Cloud Services Used

- **Google Cloud Storage (GCS)** – Raw data ingestion
- **Google BigQuery** – Final output storage for BI consumption
- **Looker Studio** – Visualization of KPIs and insights

---

## 🔍 Key Features

- Ingestion of raw healthcare data from GCS
- Multi-step data cleaning and schema standardization
- Advanced feature engineering using PySpark
- 30+ real-world healthcare analytics including:
  - Readmission analysis
  - Risk profiling
  - Utilization trends
  - Medication summaries
  - Comorbidity detection
- Data quality validation and audit reports
- BigQuery table creation for each analytical output
- Visual dashboard in Looker Studio based on analytical KPIs

---

## 🧱 Project Architecture

             ┌──────────────────────────┐
             │ Google Cloud Storage (GCS)│
             └────────────┬─────────────┘
                          │
                     PySpark Ingestion
                          │
            ┌────────────▼─────────────┐
            │ Data Cleaning & Enrichment│
            └────────────┬─────────────┘
                          │
          30+ Analytical Modules in PySpark
                          │
               ┌─────────▼────────┐
               │ Google BigQuery  │
               └─────────┬────────┘
                          │
               ┌─────────▼────────────┐
               │ Looker Studio Report │
               └──────────────────────┘


---

## 📁 Folder Structure

```

healthcare-pyspark-project/
├── data/
├── src/
│ ├── ingestion/
│ │ └── ingest_gcs.py
│ ├── transformation/
│ │ ├── clean.py
│ │ ├── feature_engineering.py
│ │ └── advanced_features.py
│ ├── analytics/
│ │ ├── demographics.py
│ │ ├── utilization.py
│ │ ├── diagnostics.py
│ │ ├── medications.py
│ │ ├── outcomes.py
│ │ ├── quality_checks.py
│ │ ├── advanced_flags.py
│ │ └── summary.py
│ ├── prediction/
│ │ └── risk_scoring.py
│ └── pipeline_runner.py
├── requirements.txt
├── README.md
└── .gitignore

```


---

## 📊 Analytical Highlights (30+ Metrics & Flags)

### Demographics
- Patient count by age group, gender, and race
- Readmission rate by gender and age
- Chronic condition prevalence by demographic

### Utilization
- Inpatient, outpatient, and emergency visit distribution
- High-utilizer detection
- Avg. visits per patient

### Diagnostics
- Most common primary diagnosis codes
- Comorbidity clusters (e.g., diabetes + hypertension)
- Diagnosis category flags

### Medications
- Drug prescription frequency
- Drug change detection
- Readmission association with specific drugs

### Outcomes & Risk
- Readmission within 30 days
- Length of stay analysis
- Risk classification (HIGH, MEDIUM, LOW) using rules

### Quality Checks
- Null and invalid value reporting
- Data quality scoring
- Record rejection tracking

### Summary Tables
- Aggregated KPIs per demographic group
- Risk flags distribution
- Diagnostic category performance

---

## 📈 Visualization

A Looker Studio dashboard is integrated with the BigQuery output to visualize key healthcare KPIs. This includes:

- Readmission trends by demographics
- Risk distribution heatmaps
- Utilization over time
- Diagnosis summary charts
- Summary scorecards and filters

_👉 Dashboard preview screenshots coming soon_

---


## 🧠 Skills Demonstrated

- Scalable data pipeline development with **PySpark**
- Modular data engineering codebase
- Healthcare domain modeling and flag creation
- Real-world transformation use cases
- GCP-native integration for storage, processing, and reporting
- Visualization with real business value

---

## 📌 Purpose

This project was created by a Data Engineer to demonstrate **deep practical knowledge of PySpark**, **hands-on cloud data engineering skills**, and the ability to deliver **realistic business intelligence pipelines** in the healthcare domain .

---

## 📌 Author

**Your Name**  
Data Engineer | PySpark & GCP Specialist  
[GitHub](https://github.com/ketan1105) • [LinkedIn](https://www.linkedin.com/in/ketan-jain-/)
