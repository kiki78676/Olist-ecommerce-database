📦 Olist E-Commerce Relational Database System
End-to-End Data Engineering • Database Design • SQL Modeling • ETL Pipeline
🌟 Overview
What This Project Delivers

This project builds a complete end-to-end relational database system using the Brazilian Olist E-Commerce Dataset.
It includes modeling, ETL, SQL schema creation, data cleaning, and analytical reporting.

Includes:

📐 Crow’s Foot ERD

🧽 Python + Pandas cleaning

🗄️ SQLite database with PK/FK

🔌 ETL Pipeline

📊 Analytical SQL reports

🧾 Documentation & data dictionary

🚀 Project Objectives
What the Database Answers

Designed to answer business questions about:

👥 Customer behavior

🛍️ Order lifecycle

🏪 Seller performance

🛒 Product categories

🚚 Delivery efficiency

💳 Payment methods

⭐ Review behavior

Dataset includes:

100k+ orders

70k+ products

100k+ payments

100k+ reviews

3k+ sellers

🗺️ Entity Relationship Diagram (ERD)
8 Fully Normalized Entities

Built using Draw.io with proper Crow’s Foot notation.

Entities:

Customers

Orders

Order_Items

Products

Product_Category

Sellers

Payments

Reviews

ERD Image:
<img width="1226" height="651" alt="ERD drawio" src="https://github.com/user-attachments/assets/f41d1a18-67c6-4d41-84ee-b4b35afc020d" />

🧹 Data Cleaning & Transformation
Python + Pandas ETL
✔ Standardization
Making All Columns Consistent

Removed extra spaces

Fixed upper/lower/title-case

Converted timestamps → SQL datetime

✔ Type Conversion
Ensuring Proper Data Types

Numeric → int64/float

IDs → string

✔ Integrity Enforcement
Validating Relationships

Removed duplicate PKs

No orphan foreign keys

Enforced relationships

Final load:

df.to_sql("TableName", con=engine, if_exists="append", index=False)

🗄️ Database Schema (DDL)
Full SQL Structure

Includes:

CREATE TABLE scripts

Primary keys

Foreign keys

Correct SQL data types

Timestamp fields

All in /code folder.

📊 Analytical SQL Reports
5 Business-Driven Insights

Report includes SQL + explanation + screenshot.

1️⃣ Top Product Categories by Revenue
SQL Query
SELECT product_category_name, SUM(price) AS total_revenue
FROM Order_Items
JOIN Products USING (product_id)
GROUP BY product_category_name
ORDER BY total_revenue DESC;

2️⃣ Delivery Delays
Actual vs Estimated Delivery
3️⃣ Most Common Payment Method
Payment Distribution
4️⃣ Top Cities by Total Orders
Geography-Based Demand
5️⃣ Review Score Distribution
Customer Experience Analysis
🧰 Technologies Used
Tools Behind the Project

Python

Pandas, NumPy

SQLite

SQLAlchemy

Jupyter Notebook

Draw.io

GitHub

📘 Dataset Source
Public Olist Brazil E-Commerce Dataset (Kaggle)
👨‍💻 Author
Kishor Khatiwada

Business Computer Information Systems
University of North Texas

⭐ Support the Project
Star the Repo If You Found It Helpful!
