# University Data Engineering Pipeline (Databricks)

## 📌 Project Overview

This project implements an end-to-end data engineering pipeline using Databricks and SQL with a Bronze-Silver-Gold architecture. The goal of the project was to transform raw university student data into a clean, analytics-ready dataset that can be used for reporting, dashboards, or machine learning.

---

## 🏗️ Architecture

Bronze → Silver → Gold

### Bronze Layer

* Raw CSV files were ingested into Databricks tables.
* No transformations were applied in this layer.
* This layer acts as the raw data storage layer.

### Silver Layer

In the Silver layer, data cleaning and transformations were performed:

* Aggregated student activity data (VLE clicks)
* Calculated average and weighted assessment scores
* Created dimension tables for students and courses
* Handled null values and duplicates
* Ensured correct data grain before joining tables

### Gold Layer

Created final analytics-ready table: **student_insights**

**Final table grain:**
One row per student per course

The Gold table includes:

* Student demographics
* Course information
* Total clicks (engagement)
* Average score
* Weighted score
* Registration information
* Final result

This table can be directly used for analytics, dashboards, or machine learning models.

---
##  Architecture Diagram

<p>
  <img src="./mermaid-diagram (1).png" alt="Data Pipeline Architecture" width="1000" height='600'>
</p>

---
## ⚠️ Challenges Faced

During this project, several real-world data engineering problems were solved:

* Join explosion after joining multiple tables
* Grain mismatch between tables
* Division by zero in weighted score calculation
* Handling null values in engagement and assessment data
* Removing duplicate records
* Ensuring one row per student per course in Gold layer

---

## 🛠️ Technologies Used

* Databricks
* SQL
* Delta Lake
* Data Modeling
* ETL Pipeline Design
* Bronze-Silver-Gold Architecture

---

## 📊 Final Output

Final Gold table: **student_insights**

This dataset combines student, course, engagement, and performance data into a single analytics-ready dataset.

---

## 🚀 Learning Outcomes

Through this project, I learned:

* Data pipeline architecture (Bronze, Silver, Gold)
* Data modeling and grain definition
* Handling duplicates and null values
* Aggregation and join strategies
* Debugging join explosion issues
* Building analytics-ready datasets
