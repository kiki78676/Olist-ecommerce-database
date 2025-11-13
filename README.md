📦 Olist E-Commerce Relational Database System
End-to-End Data Engineering • Database Design • SQL Modeling • ETL Pipeline








🌟 Overview

This project delivers a full end-to-end relational database system built using the Brazilian Olist E-Commerce Dataset.
It involves:

📐 Database Modeling (Crow’s Foot ERD)

🧽 Data Cleaning & Transformation (Python + Pandas)

🗄️ SQL Database Creation (SQLite with proper PK/FK constraints)

🔌 ETL Pipeline converting raw CSV files → clean tables

📊 Analytical SQL Queries & Reporting

🧾 Complete Data Dictionary & Documentation

This project demonstrates real industry-level data engineering & database design skills.

🚀 Project Objectives

To build a complete analytical database capable of answering questions about:

👥 Customer behavior

🛍️ Order lifecycle

🏪 Seller performance

🛒 Product categories & inventory info

🚚 Shipping & fulfillment efficiency

💳 Payment method usage

⭐ Customer review behavior

The dataset includes:

100k+ orders

70k+ products

100k+ payments

100k+ customer reviews

3k+ sellers

🗺️ ERD — Entity Relationship Diagram

The Olist system was modeled into 8 fully normalized tables with correct PK/FK relationships.

This ERD was created using Draw.io and follows proper Crow’s Foot notation.

📌 Entities include:

Customers

Orders

Order_Items

Products

Product_Category

Sellers

Payments

Reviews

Full ERD image is included below ↓

<img width="960" height="593" alt="d9c09be2375c48f0a9018fe95d4f13fa" src="https://github.com/user-attachments/assets/60fb0f01-a868-4880-99ab-3a41f02bbb3a" />


🧹 Data Cleaning & Transformation

All raw CSV files were cleaned using Python + Pandas:

✔ Standardization

Removed leading/trailing spaces

Unified casing (lowercase categories, uppercase states, title-case cities)

Converted text timestamps → SQL YYYY-MM-DD HH:MM:SS

✔ Type Conversion

Numeric columns converted to Int64 or float

IDs converted to string

Handled None, NaN, and missing values consistently

✔ Integrity Checking

Removed duplicate primary keys

Enforced foreign-key relationships

Ensured no orphan customer_id, seller_id, or order_id

✔ Final Output

Each cleaned dataframe was inserted into SQLite using:

df.to_sql("TableName", con=engine, if_exists="append", index=False)

🗄️ Database Schema Design
✔ Implemented full SQL DDL:

CREATE TABLE statements

Primary key constraints

Foreign key constraints

TIMESTAMP formatting

Data types selected based on dictionary design

All SQL files are included in the /code directory.

📊 Analytical SQL Queries (5 Reports)

The project includes 5 real analysis reports, each with:

Plain English description

SQL Query

Screenshot of results

Examples:

1️⃣ Top Product Categories by Revenue
SELECT product_category_name, SUM(price) AS total_revenue
FROM Order_Items
JOIN Products USING (product_id)
GROUP BY product_category_name
ORDER BY total_revenue DESC;

2️⃣ Average Delivery Delay vs Estimated Delivery
3️⃣ Most Common Payment Method
4️⃣ Top Cities by Number of Orders
5️⃣ Review Scores Distribution

Screenshots included in the final report.

🧰 Technologies Used

Python: Pandas, NumPy, SQLAlchemy

SQLite: SQL engine and storage

Jupyter Notebook: ETL & Cleaning

Draw.io: ERD creation

GitHub: Version control & publishing

📘 Dataset Source

This project uses the public Olist E-Commerce Dataset (Brazil) available on Kaggle.

👨‍💻 Author

Kishor Khatiwada
Business Computer Information Systems
University of North Texas

🔗 Feel free to open issues, fork the repo, or reach out!

⭐ If you found this useful…

Please consider starring the repository — it helps with visibility and supports the project 🙌
