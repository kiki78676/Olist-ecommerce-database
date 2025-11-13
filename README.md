📦 Olist E-Commerce Relational Database Project
End-to-End Database Design, Data Cleaning, SQL Modeling & Analysis

This project implements a full relational database system using the Brazilian Olist E-Commerce Dataset, covering database design, entity modeling, data cleaning, data loading, and analytical SQL reporting.
It demonstrates real-world skills in SQL, database design, Python data processing, and relational modeling.

🚀 Project Overview

The goal of this project is to build a complete e-commerce relational database capable of analyzing:

Customer behavior

Order patterns

Seller performance

Product categories

Shipping/fulfillment metrics

Payment methods

Review and customer experience trends

The dataset includes 100k+ orders, 3k sellers, 70k products, and a full payment + review system.

This project transforms raw CSV data into a production-ready structured database using SQLite, Python, and Pandas.

📊 ERD (Entity Relationship Diagram)

<img width="960" height="593" alt="d9c09be2375c48f0a9018fe95d4f13fa" src="https://github.com/user-attachments/assets/5d5216db-840e-4739-ba9d-2e3dde15b2d7" />

The full ERD image is included in the report & repository.

🛠️ Features & What This Project Demonstrates
✔ 1. Database Design

Defined business requirements, scope, and objectives

Designed complete relational schema

Created Crow’s Foot ERD

Created full data dictionary with types, constraints, PK/FK relationships

✔ 2. Data Cleaning & Transformation (Python / Pandas)

All raw CSV files from Olist were cleaned:

Trimmed strings & fixed inconsistent casing

Converted timestamps to SQL YYYY-MM-DD HH:MM:SS format

Ensured foreign key integrity

Removed duplicates

Converted numeric fields

Standardized column naming

Handled NULL values properly

Each cleaned dataframe was loaded into SQLite using .to_sql().

✔ 3. Database Creation & Table Generation

All tables were created with CREATE TABLE SQL:

Customers

Orders

Order_Items

Products

Product_Category

Sellers

Payments

Reviews

Each table includes appropriate PRIMARY KEY and FOREIGN KEY constraints.

✔ 4. Data Loading

Thousands of cleaned rows were inserted into SQLite:

Verified constraints

Checked row counts

Ensured no orphan foreign keys

Validated referential integrity

✔ 5. SQL Analysis & Reporting

Five analytical queries were created with:

Full SQL statement

Plain English explanation

Screenshot of result sets

Examples include:

Revenue by product category

Delivery performance vs estimated date

Payment method usage

Customer loyalty analysis

Review score behavior

🧰 Technologies Used

Python (Pandas, SQLAlchemy)

Jupyter Notebook

SQLite

Draw.io / Diagrams.net (for ERD)

Git / GitHub

📘 Source Dataset

This project is based on the public Olist E-Commerce Dataset from Kaggle.
Dataset includes:

100k orders

112k order items

70k products

3k sellers

100k reviews

100k+ payment documents

💡 Key Learning Outcomes

Through this project, the following skills were developed:

Real-world data modeling

ERD design using Crow’s Foot notation

SQL schema creation

ETL pipeline for CSV → DataFrame → Database

Data cleaning with Pandas

Analytical SQL queries

Database documentation (data dictionary)

Version control & GitHub project structure

🧾 Author

Kishor Khatiwada
Business Computer Information Systems
University of North Texas

If you have any suggestions or feedback, feel free to open an issue or contact me!

🎉 Thank you for viewing this project!
