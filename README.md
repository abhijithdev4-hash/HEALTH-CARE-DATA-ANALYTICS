# 🏥 Hospital Patient & Healthcare Analytics

A healthcare data analytics project exploring hospital admissions, patient demographics, department performance, billing, patient satisfaction, and readmission patterns using Python, SQL, MySQL, and data visualization.

## 📌 Project Overview

This project explores hospital admissions data to understand healthcare operations and identify useful patterns through data analysis.

The analysis focuses on patient demographics, admission trends, department performance, billing, patient satisfaction, and 30-day readmission patterns.

The dataset is synthetic and intended for educational and portfolio purposes.

## 🎯 Business Objectives

* Analyze hospital admission trends.
* Understand patient demographics.
* Compare department performance.
* Examine hospital billing patterns.
* Analyze length of stay.
* Explore patient satisfaction.
* Investigate 30-day readmission patterns.
* Present findings through visualizations and dashboards.

## 📊 Dataset Overview

The original project documentation describes a synthetic dataset containing 13,266 admission records and 14 fields covering January 2024 through December 2025.

These details and the reported metrics must be verified against the actual dataset before being treated as confirmed results.

### Dataset Fields

| Column                 | Description                  |
| ---------------------- | ---------------------------- |
| `admission_id`         | Admission identifier         |
| `patient_id`           | Patient identifier           |
| `admission_date`       | Admission date               |
| `department`           | Hospital department          |
| `diagnosis`            | Primary diagnosis            |
| `age`                  | Patient age                  |
| `gender`               | Patient gender               |
| `insurance_type`       | Insurance category           |
| `admission_type`       | Admission type               |
| `length_of_stay_days`  | Hospital stay duration       |
| `billing_amount`       | Billing amount               |
| `discharge_status`     | Discharge outcome            |
| `is_readmission_30d`   | 30-day readmission indicator |
| `patient_satisfaction` | Patient satisfaction score   |

## 🛠️ Tools and Technologies

### Python

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

### SQL and MySQL

* Data filtering and aggregation
* `GROUP BY` and `ORDER BY`
* Conditional logic
* Common Table Expressions (CTEs)
* Window functions
* Business KPI analysis

### Machine Learning

* Logistic Regression
* One-Hot Encoding
* StandardScaler
* Train/test splitting
* Model evaluation

### Power BI

* Interactive dashboards
* KPI cards
* Trend analysis
* Department performance
* Patient and financial analysis

*Tools and techniques listed above are described in the original project. Their implementation and results will be verified as the project develops.*

## 🔄 Project Workflow

1. Load the dataset.
2. Inspect data quality and structure.
3. Check missing values and duplicates.
4. Perform data preparation.
5. Conduct exploratory data analysis.
6. Analyze healthcare metrics using SQL.
7. Explore patient and department trends.
8. Review the readmission analysis.
9. Develop and validate a Power BI dashboard.
10. Document verified findings.

## 🧹 Data Cleaning and EDA

The analysis includes inspecting dataset dimensions, data types, missing values, duplicate records, numerical distributions, categorical variables, and admission dates.

Example Python code:

```python
import pandas as pd

df = pd.read_csv("data/hospital_admissions_data.csv")

print(df.head())
print(df.shape)
print(df.info())
print(df.isnull().sum())
print(df.duplicated().sum())
print(df.describe(include="all"))
```

## 🗄️ SQL Analysis

SQL is used to investigate hospital admission volume, billing, length of stay, department performance, and readmission patterns.

Example query:

```sql
SELECT
    department,
    COUNT(*) AS total_admissions,
    ROUND(AVG(length_of_stay_days), 2) AS avg_length_of_stay,
    ROUND(SUM(billing_amount), 2) AS total_billing
FROM admissions
GROUP BY department
ORDER BY total_admissions DESC;
```

SQL queries should be executed against the correctly configured MySQL database.

## 📈 Hospital KPIs

The project investigates the following metrics:

* Total admissions
* Unique patients
* Total billing
* Average billing amount
* Average length of stay
* 30-day readmission rate
* Average patient satisfaction

All reported KPI values must be recalculated and verified against the dataset before final conclusions are published.

## 💰 Financial Analysis

The financial analysis explores billing patterns across departments, diagnoses, insurance categories, and admission periods.

Billing amounts should not be interpreted as profit or collected revenue unless the dataset provides the necessary supporting information.

## 🏥 Department Analysis

Department-level analysis investigates admission volume, billing, average length of stay, patient satisfaction, and readmission patterns.

## 👥 Patient Analysis

The patient analysis explores age distribution, gender distribution, admission type, insurance category, diagnosis, length of stay, and discharge status.

## 🤖 Readmission Analysis

The original project includes a Logistic Regression workflow intended to explore 30-day readmission risk.

The original documentation reports a ROC-AUC of 0.812. This result has not yet been independently verified and should not be treated as a confirmed model result until the notebook has been reviewed and executed.

This educational model is not intended for clinical decisions or real-world patient care

## 📁 Project Structure

```text
HEALTH-CARE-DATA-ANALYTICS/
├── data/
├── notebooks/
├── sql/
├── screenshots/
├── outputs/
├── README.md
├── requirements.txt
└── .gitignore
```

The folders and files listed should be checked against the actual repository contents.

## 🚀 Installation and Setup

### Prerequisites

* Python 3
* Jupyter Notebook
* MySQL Server and MySQL Workbench, if using SQL
* Power BI Desktop, when a valid report is available



## 🔐 Security

Do not commit database passwords, API keys, private credentials, or sensitive information to GitHub.

## ⚠️ Limitations

* The dataset is synthetic.
* Original metrics and model results require verification.
* The analysis depends on the available dataset fields.
* Billing is not necessarily profit.
* The readmission model is educational and not clinically validated.
* The Power BI report still requires verification or development.


## 📌 Disclaimer

This project is intended for educational and portfolio purposes. The dataset is described as synthetic and should not be used to draw conclusions about real patients or hospitals.

The analysis and any machine-learning results are not intended for clinical diagnosis, treatment decisions, or patient care.




