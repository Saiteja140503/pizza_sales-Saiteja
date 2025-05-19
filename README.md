🍕 Pizza Sales Analysis using MySQL

📊 Project Overview

This project is a comprehensive SQL portfolio project focused on analyzing sales data from a fictional pizza restaurant. Using MySQL, we explore key business metrics like revenue, order volume, popular products, and customer preferences to derive actionable insights for decision-making.

📁 Dataset Description
The dataset includes the following CSV files:

orders.csv: Contains order IDs and timestamps.

order_details.csv: Contains order line items with quantity and pizza ID.

pizzas.csv: Contains pizza ID, size, and price.

pizza_types.csv: Descriptive metadata like category and ingredients for each pizza.

🛠️ Tech Stack
Database: MySQL

Tools Used: MySQL Workbench / phpMyAdmin / VS Code

Language: SQL

🧠 Key Business Questions Answered
📅 What are the peak order hours and busiest days?

💰 What is the total revenue and average order value?

🍕 Which pizza types and sizes are the most popular?

🗂️ What are the top 5 best-selling and least-selling pizzas?

📈 What are monthly trends in sales volume and revenue?

📌 Sample Queries
sql
Copy
Edit
-- Total Revenue
SELECT ROUND(SUM(od.quantity * p.price), 2) AS total_revenue
FROM order_details od
JOIN pizzas p ON od.pizza_id = p.pizza_id;

-- Busiest Days
SELECT DAYNAME(o.date) AS day, COUNT(*) AS total_orders
FROM orders o
GROUP BY day
ORDER BY total_orders DESC;
📊 Insights & Recommendations
Most orders are placed on weekends, especially during evenings.

Large-sized pizzas dominate sales, contributing to higher revenue.

Classic and Supreme categories are consistently popular.

Consider running promotions on slow days to increase traffic.# pizza_sales-Saiteja
