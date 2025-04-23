# 📊 Sales Insight Dashboard – Power BI & SQL Project

This project demonstrates a **Sales Insight Dashboard** created using **Microsoft Power BI** and **SQL** for data analysis and cleaning. It analyzes multi-dimensional sales data to uncover patterns, trends, and high-value segments. The dashboard serves as a strategic tool for sales and business managers to make data-informed decisions.

## 🎯 Project Objective

- Analyze sales data to uncover insights related to performance across markets, products, customers, and time.
- Build a business-ready dashboard to present key KPIs and trends visually.
- Use SQL for data extraction, cleaning, and quick aggregations.

## ❓ Key Business Questions

1. Which markets generate the highest revenue and sales quantity?
2. What is the monthly/quarterly trend in sales revenue?
3. Who are the top 5 customers contributing to revenue?
4. Which products perform best by sales?
5. How do sales vary across different years or months?


## 📂 Datasets Used
- <a href="https://github.com/yadhukrishna361/sales-insight-dashboard-powerbi/blob/main/sales_data1.xlsx">Dataset</a>

## 🛠️ Data Preparation & Cleaning

- Used **SQL** to explore, filter, and clean the data prior to import.
- Performed joins between fact and dimension tables (e.g., transactions with date).
- Converted data types, handled currency inconsistencies, and identified null or duplicate records.

---

## 🔍 Data Analysis Using SQL

Some examples of SQL queries used during the initial data exploration phase:

```sql
-- 1. Show all customer records
SELECT * FROM customers;

-- 2. Count total number of customers
SELECT count(*) FROM customers;

-- 3. Transactions for Chennai (market code = 'Mark001')
SELECT * FROM transactions WHERE market_code = 'Mark001';

-- 4. Distinct product codes sold in Chennai
SELECT DISTINCT product_code FROM transactions WHERE market_code = 'Mark001';

-- 5. Transactions in US Dollars
SELECT * FROM transactions WHERE currency = 'USD';

-- 6. Transactions in 2020 (with Date join)
SELECT transactions.*, date.*
FROM transactions
INNER JOIN date ON transactions.order_date = date.date
WHERE date.year = 2020;

-- 7. Total revenue in 2020 (in INR or USD)
SELECT SUM(transactions.sales_amount)
FROM transactions
INNER JOIN date ON transactions.order_date = date.date
WHERE date.year = 2020 AND (transactions.currency = 'INR' OR transactions.currency = 'USD');

-- 8. Total revenue in Jan 2020
SELECT SUM(transactions.sales_amount)
FROM transactions
INNER JOIN date ON transactions.order_date = date.date
WHERE date.year = 2020 AND date.month_name = 'January'
AND (transactions.currency = 'INR' OR transactions.currency = 'USD');

-- 9. Total revenue in 2020 from Chennai
SELECT SUM(transactions.sales_amount)
FROM transactions
INNER JOIN date ON transactions.order_date = date.date
WHERE date.year = 2020 AND transactions.market_code = 'Mark001';
```

## 📊 Dashboard Features

- **Total Revenue and Sales Qty** KPIs
- **Revenue by Markets** (Bar chart)
- **Sales Qty by Markets** (Bar chart)
- **Revenue Trend Over Time** (Line chart)
- **Top 5 Customers** by revenue (Bar chart)
- **Top 5 Products** (Bar chart)

### 📸 Screenshot:
[Dashboard Screenshot]![sales dashboard](https://github.com/user-attachments/assets/849cb528-b9ec-4c6e-88ae-d751c2541de7)

## 🔍 Insights & Findings

- **Delhi** is the highest revenue-generating market (~520M).
- **Electricalsara Stores** is the top customer contributing over 400M in sales.
- A single unnamed product accounts for nearly 469M revenue (data cleaning opportunity).
- A downward revenue trend was noticed post-2019, needing further investigation.
- Several regions such as **Bangalore** and **Patna** show very low engagement, signaling potential areas for marketing focus.

## ✅ Conclusion

This project combines the power of **SQL for backend data cleaning and analysis** with **Power BI for compelling data visualization**. The dashboard helps business teams make strategic decisions based on sales performance, customer segmentation, and regional opportunities.
## 🛠️ Tools & Skills Used

- **Power BI Desktop**
- **Power Query Editor**
- **Data Modeling (Star Schema)**
- **DAX (Calculated Measures & KPIs)**
- **SQL for Data Cleaning & Querying**
- **Excel/CSV integration**
- **Data Cleaning & Transformation**
- **Business Analysis & Reporting**
