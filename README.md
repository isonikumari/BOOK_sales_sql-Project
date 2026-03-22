sales_sql_project
comprehensive books sales database management and analysis using SQL schemas and queries.

📊 Sales SQL Analysis
📌 Project Overview
This project explores a Sales dataset to extract actionable business insights. I focused on customer segmentation, revenue trends, and craze.

🏗️ Data Architecture (The Schema)
I built a normalized database consisting of three primary tables. This structure ensures data integrity and mimics real-world backend systems

The goal was to transition from raw data creation to high-level business intelligence reporting using MySQL.

1. customers Table
Contains user demographics and unique identifiers.

2. orders Table
Tracks financial transactions, linking to customers via customerid.

🛠️ SQL Skills Demonstrated
In this project, I applied the following advanced SQL concepts:

Joins: Using LEFT JOIN to identify "Ghost Customers" (users with zero orders).
Subqueries: Implementing multi-level subqueries to filter orders against database maximums.
Aggregations: Leveraging GROUP BY, SUM(), and COUNT() for monthly revenue reports.
Window Functions: Ranking products and orders using DENSE_RANK().
Data Validation: Identifying schema errors (e.g., correcting column naming conventions).
💡 Business Questions & Solutions
🛒 Sales Performance
Question: Which customers are high-value (orders > $200)?

SELECT customername, amount 
FROM customers c 
JOIN orders o ON c.customerid = o.customerid 
WHERE amount > 200;
