# University Data Engineering Pipeline (Databricks)

## Project Overview

This project implements an end-to-end data engineering pipeline using Databricks with a Bronze-Silver-Gold architecture. Raw university student data was transformed into a clean analytics-ready dataset.

## Architecture

Bronze → Silver → Gold

## Bronze Layer

Raw CSV files were ingested into Databricks tables without transformations.

## Silver Layer

Data cleaning and transformations were performed:

* Aggregated student activity data
* Calculated weighted assessment scores
* Created dimension tables for students and courses
* Handled null values and duplicates
* Ensured correct data grain

## Gold Layer

Created final analytics-ready table: student_insights

Final table grain:
One row per student per course

The Gold table includes:

* Student demographics
* Course information
* Total clicks (engagement)
* Average score
* Weighted score
* Registration information

## Challenges Faced

* Join explosion after multiple joins
* Grain mismatch between tables
* Division by zero in weighted score calculation
* Handling null values
* Removing duplicate records

## Technologies Used

* Databricks
* SQL
* Delta Lake
* Data Modeling
* ETL Pipeline Design

## Final Output

The final Gold table can be used for analytics, dashboards, or machine learning models.
