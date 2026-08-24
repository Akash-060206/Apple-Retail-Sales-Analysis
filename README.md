# 🍎 Apple Retail Sales Analysis

<div align="center">

### Advanced SQL Analysis of 1M+ Apple Retail Sales Records

![SQL](https://img.shields.io/badge/SQL-PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![Dataset](https://img.shields.io/badge/Dataset-1M%2B%20Rows-6C63FF?style=for-the-badge)
![Performance](https://img.shields.io/badge/Performance-136ms%20%E2%86%92%206ms-00A67E?style=for-the-badge)

</div>

---

## 📌 Project Overview

**Apple Retail Sales Analysis** is an advanced SQL project built on **1+ million retail sales records**. The project focuses on solving real-world business problems related to **store performance, product trends, sales growth, geographic analysis, and warranty claims**.

It also demonstrates SQL query optimization using **indexes and `EXPLAIN ANALYZE`**.

---

## 🗃️ Database Schema

The database contains five main tables:

| Table | Description |
|---|---|
| `stores` | Store information such as name, city and country |
| `category` | Product category details |
| `products` | Product name, category, launch date and price |
| `sales` | Sales transactions, dates, stores, products and quantities |
| `warranty` | Warranty claims and repair status |

```text
category ──► products ──► sales ◄── stores
                         │
                         ▼
                      warranty
```

---

## 🧠 Skills Demonstrated

- Advanced SQL
- Complex Joins
- Aggregations
- CTEs
- Subqueries
- Window Functions
- `RANK()` and `LAG()`
- Running Totals
- Year-over-Year Analysis
- Date & Time Functions
- Conditional Logic with `CASE`
- Indexing
- Query Performance Optimization
- `EXPLAIN ANALYZE`

---

## 📊 Business Questions Solved

### 🏪 Store & Sales Analysis

1. How many stores exist in each country?
2. How many units has each store sold?
3. How many sales occurred in December 2023?
4. Which store sold the highest number of units in the last year?
5. Which countries have the highest sales volume?

### 📦 Product Analysis

6. What is the average product price in each category?
7. How many unique products were sold during the last year?
8. What is the least-selling product in each country?
9. Which product categories have the most warranty claims?
10. Which recently launched products received warranty claims?

### 🛡️ Warranty Analysis

11. How many stores have never had a warranty claim?
12. What percentage of warranty claims were rejected?
13. How many warranty claims were filed in 2024?
14. How many claims were filed within 180 days of purchase?
15. Which store has the highest percentage of completed warranty claims?

### 📈 Advanced Time-Series Analysis

16. What is the year-over-year growth ratio for each store?
17. What is the monthly running total of sales for each store?
18. Which months exceeded 5,000 units sold in the US?
19. How do warranty claims vary across product price segments?
20. Which products perform poorly across different countries?

---

## ⚡ Query Performance Optimization

A key part of this project was improving query performance.

### Before Optimization

**136.423 ms**

### After Optimization

**6.324 ms**

### 🚀 Result

**~95% reduction in execution time**

Indexes were created on frequently queried columns:

```sql
CREATE INDEX sales_product_id
ON sales(product_id);

CREATE INDEX sales_store_id
ON sales(store_id);

CREATE INDEX sales_quantity
ON sales(quantity);

CREATE INDEX sale_date
ON sales(sale_date);

CREATE INDEX sales_product_id_store_id
ON sales(product_id, store_id);
```

Performance was measured using:

```sql
EXPLAIN ANALYZE
```

---

## 🔍 Key Analytical Areas

### 🏪 Store Performance
Identify top-performing stores, sales volume, growth and warranty completion rates.

### 📦 Product & Category Trends
Analyze product demand, pricing, categories and low-performing products.

### 🌎 Geographic Analysis
Compare sales and warranty activity across countries.

### 🛡️ Warranty Analysis
Analyze rejected claims, completed claims, claim timing and claim rates.

### 📈 Time-Series Analysis
Perform monthly analysis, running totals and YoY growth calculations.

---

## 📁 Project Structure

```text
Apple-Retail-Sales-Analysis/
│
├── schema.sql
├── SQL_QUERIES.sql
└── README.md
```

- **`schema.sql`** → Database and table definitions
- **`SQL_QUERIES.sql`** → Analysis, business questions and optimization queries
- **`README.md`** → Project documentation

---

## 🚀 Key Takeaways

This project demonstrates the ability to:

**Explore → Analyze → Solve → Optimize**

It combines **business problem-solving, advanced SQL, analytical thinking, and query optimization** to extract actionable insights from a large retail dataset.

---

## 👤 Author

### **Akash Srivastava**

⭐ If you found this project useful, consider giving the repository a star!

