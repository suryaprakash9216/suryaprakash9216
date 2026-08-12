# Retail Revenue Performance & Customer Intelligence System | SQL Server & Power BI

## Project Overview

This project investigates a real-world revenue and customer activity decline using a live 1M+ row transactional dataset. It follows a complete BI lifecycle — data acquisition, SQL Server data engineering, data quality investigation, dimensional modelling, root-cause analysis, and interactive Power BI dashboard development — to answer a genuine business question rather than simply visualise data.

The project simulates a real business engagement: management observes revenue and customer activity decline and requests an investigation into the cause, along with a recommended course of action.

---

## Business Objectives

* Investigate the drivers behind a period of revenue decline.
* Determine whether the cause was pricing, cancellations, data quality, or customer behaviour.
* Identify which customers, products, and countries were most affected.
* Quantify the revenue impact tied to customer churn.
* Develop an executive-ready Power BI report with role-based security and automated alerting.

---

## Dataset Summary

The UCI Online Retail II dataset (official UCI Machine Learning Repository) contains:

* 1,067,371 transaction line items
* December 2009 – December 2011
* Real UK-based online giftware retailer
* Order, product, customer, and country-level detail
* Genuine data quality issues (missing customer IDs, cancellations, duplicates, invalid records)

---

## Tools & Technologies

* SQL Server / T-SQL
* Power BI
* DAX
* Power Query
* Power BI Service
* Row-Level Security
* Power BI Data Alerts
* Data Modelling
* ETL

---

## Project Workflow

### 1. Data Acquisition & Staging

Loaded raw data into SQL Server without transformation, preserving a fully auditable source layer.

### 2. Data Profiling & Quality Investigation

Systematically profiled missing values, duplicates, cancellations, and invalid records, with every issue documented and a handling decision recorded.

### 3. Data Cleaning & Transformation

Built repeatable SQL logic to flag (never silently delete) cancellations, invalid prices, non-product codes, and duplicate records.

### 4. Dimensional Modelling

Designed and built a star schema (fact and dimension tables) for analytical performance.

### 5. SQL Root-Cause Investigation

Ran seven sequential diagnostic queries — testing and ruling out pricing, cancellations, and data-completeness issues — before reaching an evidenced conclusion.

### 6. KPI Framework

Defined every metric's exact formula and assumptions before building any visual.

### 7. Power BI Development

Built a three-page executive report with a custom DAX measure library and visual design.

### 8. Deployment & Security

Published to Power BI Service with row-level security by region and a live, threshold-based KPI alert.

### 9. Testing & Validation

Logged UAT test scenarios and results against the finished report.

---

## Key Finding

Revenue declined for three consecutive months (February–April 2011) despite steady growth through the prior year. The investigation ruled out pricing, cancellations, and data-completeness issues, and identified two evidenced, compounding causes:

* A genuine decline in customer purchase frequency — 1,055 lower-value customers did not return, representing €595,135 in prior-year revenue.
* A concentrated product-level effect — the top 20 declining products accounted for 53.4% of the total decline.

---

## Key KPIs

* Total Revenue
* Total Orders
* Active Customers
* Average Order Value (AOV)
* Cancellation Rate %
* Year-over-Year Growth %
* Revenue Variance Contribution %
* Customers Churned

---

## Dashboard Screenshots

### Executive Overview

![Executive Overview](Screenshot%202026-08-12%20020252.png)

### Root Cause Analysis

![Root Cause Analysis](Screenshot%202026-08-12%20020313.png)

### Action Tracker

![Action Tracker](Screenshot%202026-08-12%20020338.png)

### Row-Level Security — UK Manager

![RLS UK Manager](Screenshot%202026-08-12%20030513.png)

### Row-Level Security — Non-UK Manager

![RLS Non-UK Manager](Screenshot%202026-08-12%20030530.png)

---

## Repository Structure

### SQL Scripts

* 02_staging_tables.sql
* 03_data_profiling.sql
* 04_data_cleaning.sql
* 05_star_schema.sql
* 06_business_analysis.sql

### Power BI Dashboard

* Retail_Revenue_Performance_Customer_Intelligence.pbix

### Documentation

* business_brief.md
* data_quality_report.md
* findings_log.md
* kpi_dictionary.md
* UAT_testing.md
* phase10_power_automate_status.md

---

## Business Value

* Identified the true root cause of a revenue decline using systematic SQL investigation rather than assumption.
* Quantified real revenue-at-risk (€595,135) tied to specific customer churn.
* Isolated a concentrated product-level effect responsible for over half the total decline.
* Ruled out pricing and cancellations as contributing factors with direct evidence.
* Delivered a production-style Power BI deployment with row-level security and live alerting, not just a static dashboard.

---

## Skills Demonstrated

SQL Server | T-SQL | Power BI | DAX | Power Query | Data Modelling | Star Schema Design | Data Quality Investigation | ETL | Row-Level Security | Power BI Service | KPI Alerting | Root-Cause Analysis | Business Intelligence | Dashboard Development
