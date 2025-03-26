# SQL-Project-Brazilian-E-Commerce-Public-Dataset-by-Olist
## 📌 Project Overview
This project analyzes an e-commerce dataset from Olist using advanced SQL to uncover insights on customer behavior, product performance, order trends, and reviews. The anonymized dataset includes 100K orders from 2016-2018 across multiple Brazilian marketplaces.
# Advanced SQL Project: E-Commerce Sales Analysis

## 📂 Dataset Information
The dataset used for this project is the **Brazilian E-Commerce Public Dataset by Olist** available on Kaggle:
[Download Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

### Dataset Tables
- **Customers**: Customer details (ID, name, email, country, signup date)
- **Products**: Product details (ID, name, category, price, stock)
- **Orders**: Order transactions (ID, customer ID, order date, total amount, status)
- **Order Details**: Products within each order (order ID, product ID, quantity, price)
- **Reviews**: Customer reviews (review ID, customer ID, product ID, rating, review text, date)

## 🛠️ SQL Scripts
The project includes the following SQL operations:

### 1️⃣ **Database Setup & Data Import**
- Create a database and define table schemas.
- Load CSV data into MySQL.

### 2️⃣ **Advanced SQL Queries**
- **Best-Selling Products**: Top 10 most sold products.
- **Top Customers**: Customers with the highest total spending.
- **Repeat Customers**: Customers with more than five orders.
- **Product Ratings**: Products with the highest average ratings (min 10 reviews).
- **Top Product Categories**: Most sold product categories.

## 🔍 Sample Query
```sql
-- Retrieve top 10 best-selling products
SELECT p.product_name, SUM(od.quantity) AS total_sold
FROM order_details od
JOIN products p ON od.product_id = p.product_id
GROUP BY p.product_name
ORDER BY total_sold DESC
LIMIT 10;
```

## 📌 How to Use This Project
1. **Import the Database:**
   - Create the `ecommerce_db` database.
   - Execute the SQL scripts to create tables and import data.
2. **Run Queries:**
   - Use MySQL Workbench.


