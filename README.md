# Flight Analytics Data Warehouse

Snowflake-based analytical data warehouse project designed for flight performance analysis, dimensional modeling, and BI-ready reporting.

---

## 1. Objective

The objective of this project was to load a flight dataset into Snowflake, organize it into a dimensional structure, and prepare an analytical view suitable for downstream reporting and BI tools.

---

## 2. Data Loading

The source data was loaded into Snowflake using SQL-based ingestion workflows. Appropriate data types and transformations were applied during table creation to support analytical usage and reporting requirements.

---

## 3. Data Model

The dataset was organized into a dimensional structure including:

* FACT_FLIGHTS
* DIM_DATE
* DIM_AIRLINE
* DIM_AIRPORT
* DIM_BIN

This structure enables scalable querying and supports analytical workflows and BI reporting.

---

## 4. Transformations and Adjustments

Several transformations and derived analytical fields were implemented, including:

* DISTANCEGROUP binning in 100-mile ranges
* DEPDELAYGT15 indicator
* NEXTDAYARR indicator
* Cleaning and normalization of airline and airport names
* Standardization of time-related fields
* Timestamp generation for analytical reporting

Additional timestamp fields were included to improve usability for visualization and downstream analytics.

---

## 5. Analytical View

A final analytical view (`VW_FLIGHTS`) was created by joining the fact and dimension tables while exposing business-friendly analytical fields for reporting and visualization purposes.

---

## 6. Validation

Several validation and data quality checks were performed, including:

* Row count validation
* Null analysis
* Distance bin verification
* Derived KPI validation
* Join consistency checks

Approximately 1.19 million records were processed successfully.

---

## 7. Notes

The final structure was prepared with the intention of supporting BI tools such as Tableau and enabling efficient analytical querying and dashboard development.

---

## Technologies Used

* Snowflake
* SQL
* Snowpark Python
* Dimensional Modeling
* Data Warehouse Design
* BI-Oriented Data Modeling

---

## Repository Contents

| File             | Description                                   |
| ---------------- | --------------------------------------------- |
| notebook.ipynb   | Main implementation notebook                  |
| presentation.pdf | Business insights and analytical presentation |
| README.md        | Project documentation                         |

---

## Disclaimer

This repository contains sanitized and non-confidential analytical content prepared for educational and portfolio purposes.
