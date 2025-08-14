🛒 Zepto E-commerce SQL Data Analyst Portfolio Project

A real-world SQL data analytics project using an e-commerce inventory dataset scraped from Zepto — one of India’s fastest-growing quick-commerce startups.

This project replicates the actual workflows of a Data Analyst, from raw data ingestion to business-focused insights that drive decision-making.

📌 Project Objectives

Simulating a real e-commerce analytics environment to:

✅ Set up a realistic, messy e-commerce inventory database
✅ Conduct Exploratory Data Analysis (EDA) to uncover trends & anomalies
✅ Perform Data Cleaning — handle missing values, remove invalid entries, standardize prices
✅ Write business-driven SQL queries to analyze pricing, inventory, stock levels, and revenue opportunities

📂 Dataset Overview

Source: Kaggle (originally scraped from Zepto’s product listings)

Structure: Each row represents a SKU (Stock Keeping Unit)

Realistic challenges: Duplicate product names (due to different sizes, packages, and discounts), inconsistent pricing, mixed quantity units

Key Columns:

sku_id — Synthetic Primary Key

name — Product name

category — Product category (Fruits, Snacks, Beverages, etc.)

mrp — Maximum Retail Price (₹)

discountPercent — Discount applied

discountedSellingPrice — Final selling price (₹)

availableQuantity — Units in stock

weightInGms — Weight in grams

outOfStock — Stock status

quantity — Package quantity or weight info

🔧 Project Workflow
1. Database Setup

Created PostgreSQL table with proper data types:

CREATE TABLE zepto (
  sku_id SERIAL PRIMARY KEY,
  category VARCHAR(120),
  name VARCHAR(150) NOT NULL,
  mrp NUMERIC(8,2),
  discountPercent NUMERIC(5,2),
  availableQuantity INTEGER,
  discountedSellingPrice NUMERIC(8,2),
  weightInGms INTEGER,
  outOfStock BOOLEAN,
  quantity INTEGER
);

2. Data Import

Imported CSV into PostgreSQL using pgAdmin or \copy command

Fixed UTF-8 encoding issues by saving the CSV in UTF-8 format

3. Data Exploration

Checked record count & dataset structure

Identified null values

Listed distinct product categories

Compared in-stock vs out-of-stock products

Detected duplicate SKUs for different packaging

4. Data Cleaning

Removed entries with zero MRP or selling price

Converted prices from paise to rupees for consistency

5. Business Insights Derived

Top 10 products by highest discount

High-MRP products currently out of stock

Potential revenue per product category

Premium products (MRP > ₹500) with low discounts

Top 5 categories with highest average discount

Value-for-money products based on price per gram

Classified inventory into Low / Medium / Bulk weight categories

Measured total inventory weight per category

🛠 Skills & Tools Used

SQL (PostgreSQL) — database creation, EDA, data cleaning, business analysis

Data Analysis — identifying trends, anomalies, and insights

Problem Solving — handling messy, real-world data challenges

This project demonstrates end-to-end SQL data analysis skills, business thinking, and the ability to work with realistic e-commerce datasets — exactly the kind of work done in industry settings.
