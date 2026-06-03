# 📉 Sales-Data-Analysis-using-sql-power-bi

## Overview

This project focuses on analyzing sales performance using SQL and Power BI to uncover business insights, identify trends, and support data-driven decision-making. The project involves data extraction, transformation, analysis, and visualization to provide a comprehensive view of sales operations.

---

## Business Problem

Organizations generate large volumes of sales data, but transforming that data into actionable insights can be challenging. This project aims to analyze sales performance, customer behavior, and product trends to help stakeholders make informed business decisions.

---

## Tools & Technologies

### SQL

* Data Extraction
* Data Cleaning
* Data Validation
* Aggregation Queries
* Business KPI Analysis
* Trend Analysis

### Power BI

* Data Modeling
* DAX Measures
* Interactive Dashboard Creation
* KPI Visualization
* Drill-Down Analysis
* Business Reporting

---

## Project Workflow

### 1. Data Collection

* Imported raw sales data from source files.
* Verified data quality and completeness.

### 2. Data Cleaning

* Removed duplicates.
* Handled missing values.
* Standardized data formats.
* Corrected inconsistent records.

---
  
### 3. SQL Analysis

Performed SQL queries to analyze:

1.Show all customer records

SELECT * FROM customers;

2.Show total number of customers

SELECT count(*) FROM customers;

3.Show transactions for Chennai market (market code for chennai is Mark001

SELECT * FROM transactions where market_code='Mark001';

4.Show distrinct product codes that were sold in chennai

SELECT distinct product_code FROM transactions where market_code='Mark001';

5.Show transactions where currency is US dollars

SELECT * from transactions where currency="USD"

6.Show transactions in 2020 join by date table

SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

7.Show total revenue in year 2020,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

8.Show total revenue in year 2020, January Month,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

9.Show total revenue in year 2020 in Chennai

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";

---

### 4. Data Modeling in Power BI

* Established table relationships.
* Created calculated columns.
* Built DAX measures for KPIs.

---

Power BI Dashboard Preview
<img width="1003" height="627" alt="image" src="https://github.com/user-attachments/assets/33510e1b-ffbb-4dff-aa21-97f55c991f33" />

<img width="1007" height="637" alt="image" src="https://github.com/user-attachments/assets/ef621446-4a13-4a8c-9676-382bc3f89a74" />

<img width="1005" height="635" alt="image" src="https://github.com/user-attachments/assets/331efcfc-276b-4a0f-9a7a-c611eaec1b81" />

---

## Key KPIs

* Total Revenue =₹142M
* Sales Qty = 350K
* Total Profit Margin = ₹2.1M
* Top Customers = Electricalsara Stores, Excel Stores, Premium Stores, Electricalslytical, Info Stores
 
---

## Key Insights

* Identified high-performing products and categories.
* Analyzed sales trends over time.
* Evaluated customer purchasing behavior.
* Measured profitability across regions.
* Highlighted opportunities for business growth.

---

## Business Impact

The dashboard enables stakeholders to:

* Monitor business performance in real time.
* Identify profitable products and customers.
* Improve sales strategies.
* Make data-driven decisions.
* Optimize resource allocation.

---

## Conclusion

This project demonstrates an end-to-end data analytics workflow using SQL and Power BI. By combining data analysis, business intelligence, and interactive visualization techniques, the solution transforms raw sales data into meaningful business insights that support strategic decision-making.

---


