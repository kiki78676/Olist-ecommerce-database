# 📦 Olist E-Commerce Relational Database System  
### End-to-End Data Engineering • Database Design • SQL Modeling • ETL Pipeline

# 🌟 Overview  
### What This Project Delivers

This project builds a complete end-to-end relational database system using the Brazilian Olist E-Commerce Dataset.  
It includes modeling, ETL, SQL schema creation, data cleaning, and analytical reporting.

Includes:

- 📐 Crow’s Foot ERD  
- 🧼 Python + Pandas cleaning  
- 🗄️ SQLite database with PK/FK  
- 🔌 ETL Pipeline  
- 📊 Analytical SQL reports  
- 🧾 Documentation & data dictionary  

# 🚀 Project Objectives  
### What the Database Answers

Designed to answer business questions about:

- 👥 Customer behavior  
- 📦 Order lifecycle  
- 🏪 Seller performance  
- 🛒 Product categories  
- 🚚 Delivery performance  
- 💳 Payment methods  
- ⭐ Customer reviews  

Dataset size:

- 100k+ orders  
- 70k+ products  
- 100k+ payments  
- 100k+ reviews  
- 3k+ sellers  

# 🗺️ Entity Relationship Diagram (ERD)  
### Full Crow’s Foot Model

Entities:

- Customers  
- Orders  
- Order_Items  
- Products  
- Product_Category  
- Sellers  
- Payments  
- Reviews  

<img width="1226" height="651" alt="ERD drawio" src="https://github.com/user-attachments/assets/f41d1a18-67c6-4d41-84ee-b4b35afc020d" />

# 🧹 Data Cleaning & Transformation  
### Python + Pandas ETL

# ✔ Standardization  
- Trimmed spaces  
- Fixed casing (categories → lowercase, states → UPPERCASE, cities → Title Case)  
- Converted timestamps to `YYYY-MM-DD HH:MM:SS`  

# ✔ Type Conversion  
- Numeric columns → INT / FLOAT  
- ID columns → STRING  
- Clean handling of `NaN` / NULL values  

# ✔ Integrity Checks  
- Removed duplicate primary keys  
- Ensured foreign-key consistency (no orphan `customer_id`, `order_id`, `seller_id`)  

Final load into SQLite:

```python
df.to_sql("TableName", con=engine, if_exists="append", index=False)
```

# 🗄️ Database Schema (DDL)  
### SQL Structure

The database schema is implemented with full DDL, including:

- `CREATE TABLE` statements for all 8 core entities  
- `PRIMARY KEY` and `FOREIGN KEY` constraints  
- Appropriate data types for IDs, numeric values, timestamps, and text  
- Timestamp fields stored as `DATETIME`-compatible strings  

All SQL schema files are included in the `/code` directory.

---

# 📊 Analytical SQL Reports  
### Business Insights from the Database

The project includes **5 analytical SQL reports**, each containing:

- Plain English explanation  
- SQL query  
- Screenshot of result set  

---

# 1️⃣ Top Product Categories by Revenue  
### SQL Query

```sql
SELECT 
    p.product_category_name,
    SUM(oi.price) AS total_revenue
FROM Order_Items oi
JOIN Products p
    ON oi.product_id = p.product_id
GROUP BY p.product_category_name
ORDER BY total_revenue DESC;

# 2️⃣ Average Delivery Delay vs Estimated Delivery  
### Delivery Performance Analysis

- Calculates the difference between `order_delivered_customer_date` and `order_estimated_delivery_date`  
- Determines whether Olist delivers **early**, **on-time**, or **late**  

---

# 3️⃣ Most Common Payment Method  
### Payment Behavior Analysis

- Aggregates orders by `payment_type`  
- Ranks the most frequently used payment methods (credit card, boleto, voucher, etc.)  

---

# 4️⃣ Top Cities by Number of Orders  
### Geography-Based Demand

- Groups total orders by **customer city**  
- Identifies which cities generate the highest order volume  

---

# 5️⃣ Review Score Distribution  
### Customer Satisfaction Overview

- Counts total reviews by `review_score`  
- Shows overall customer satisfaction trends on the Olist platform  

Screenshots for all 5 reports are included in the final notebook/documentation.

---

# 🧰 Technologies Used  
### Tools & Stack

- 🐍 **Python** – data processing & ETL  
- 🧮 **Pandas, NumPy** – data cleaning & transformation  
- 🗄️ **SQLite** – relational database engine  
- 🧩 **SQLAlchemy** – Python–SQL ORM / bridge  
- 📓 **Jupyter Notebook** – analysis & development  
- 🧊 **Draw.io** – ERD design (Crow’s Foot notation)  
- 🧷 **Git & GitHub** – version control & project hosting  

---

# 📘 Dataset Source  
### Olist E-Commerce Public Dataset

This project uses the public **Olist E-Commerce Dataset (Brazil)** available on **Kaggle**.

---

# 👨‍💻 Author  
### Kishor Khatiwada

Business Computer Information Systems  
University of North Texas  

---

# ⭐ Support the Project  
### If You Found This Helpful

If you like the project or learned something from it,  
please consider **starring ⭐ the repository** — it helps with visibility and supports future work 🙌
