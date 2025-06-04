# Sales-Trend-Analysis-Using-Aggreg# 📊 Sales Trend Analysis (SQL Project)

## 🎯 Objective
Analyze monthly revenue and order volume using aggregation functions in SQL.

## 🛠 Tools
- SQL  MySQL
- Table: `online_sales` with columns:
  - `order_id`
  - `order_date`
  - `amount`
  - `product_id`

## 📈 SQL Highlights
- Used `EXTRACT(YEAR/MONTH FROM order_date)` for time-based grouping
- Used `SUM()` to calculate total revenue
- Used `COUNT(DISTINCT order_id)` to count unique orders
- Results ordered by year and month

## 📂 Output 
| Year | Month | Revenue | Orders |
|------|-------|---------|--------|
| 2024 | 1     | 650.00  | 2      |



Coding in sample wasy: use this code way.

sqls,,,,,,
SELECT 
    EXTRACT(YEAR FROM order_date) AS order_year,
    EXTRACT(MONTH FROM order_date) AS order_month,
    SUM(amount) AS total_revenue,
    COUNT(DISTINCT order_id) AS total_orders
FROM 
    online_sales
GROUP BY 
    EXTRACT(YEAR FROM order_date),
    EXTRACT(MONTH FROM order_date)
ORDER BY 
    order_year,
    order_month;

