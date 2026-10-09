# E-commerce Sales ETL Pipeline

## 📌 Project Overview

This project demonstrates an ETL (Extract, Transform, Load) pipeline using **Python, Pandas, and MySQL** to process and analyze e-commerce sales data.

The goal is to prepare raw sales data, validate data quality, load the transformed dataset into a MySQL database, and perform SQL analysis to discover useful business insights.

## 🎯 Project Objectives

* Extract sales data from a CSV file.
* Transform and prepare the data using Python and Pandas.
* Create year and month columns from the order date.
* Load the transformed data into MySQL.
* Validate data quality and identify inconsistencies.
* Analyze sales performance using SQL queries.

## 🛠️ Technologies Used

* **Python** – Data processing
* **Pandas** – Data cleaning and transformation
* **Google Colab** – Python development environment
* **MySQL** – Data storage and SQL analysis
* **SQL** – Data validation and business analysis
* **CSV** – Source and transformed data format

## 🔄 ETL Workflow

### 1. Extract

Loaded the e-commerce sales dataset from a CSV file using Pandas.

### 2. Transform

* Converted `order_date` into a datetime format.
* Extracted `order_year` and `order_month`.
* Checked for missing values and duplicate records.
* Validated quantity, price, discount, delivery days, and customer ratings.
* Checked revenue calculations for consistency.

### 3. Load

* Created the `ecommerce_etl` database in MySQL.
* Created the `ecommerce_sales` table.
* Imported 5,000 transformed records into the database.
* Verified the loaded record count using SQL.

### 4. Analyze

Used SQL queries to explore revenue by product category, regional performance, monthly sales trends, top customers, and payment methods.

## 📊 Dataset Information

* **Total records:** 5,000
* **Original columns:** 12
* **Columns after transformation:** 14
* **Source format:** CSV

Key columns include:

`order_id`, `order_date`, `customer_id`, `product_category`, `region`, `quantity`, `unit_price`, `discount`, `payment_method`, `delivery_days`, `customer_rating`, `revenue`, `order_year`, and `order_month`.

## 📈 Key Business Insights

### Revenue by Product Category

| Product Category |      Revenue |
| ---------------- | -----------: |
| Electronics      | 1,829,899.22 |
| Clothing         | 1,531,931.72 |
| Home             |   982,083.92 |
| Beauty           |   765,860.88 |

**Insight:** Electronics generated the highest revenue among the four product categories.

### Revenue by Region

| Region |      Revenue |
| ------ | -----------: |
| West   | 1,345,582.16 |
| North  | 1,281,508.45 |
| South  | 1,246,640.90 |
| East   | 1,236,044.23 |

**Insight:** The West region recorded the highest revenue.

### Payment Method Analysis

| Payment Method | Orders |      Revenue |
| -------------- | -----: | -----------: |
| Card           |  2,270 | 2,366,248.20 |
| COD            |  1,774 | 1,788,408.44 |
| Wallet         |    956 |   955,119.10 |

**Insight:** Card payments accounted for the largest number of orders and the highest revenue.

## ✅ Data Validation

* Loaded and verified 5,000 records in MySQL.
* Confirmed 5,000 distinct order IDs.
* Checked for missing values in key columns.
* Checked for duplicate records in the source dataset.
* Validated quantity, price, discount, delivery days, and customer rating ranges.
* Compared stored revenue values against recalculated revenue.

**Data quality note:** The MySQL revenue recalculation showed a difference of ₹0.01 or equivalent currency units for 92 records. This rounding discrepancy requires further investigation before treating the values as fully reconciled.

## 📂 Project Structure

```text
ecommerce-sales-etl-pipeline/
│
├── README.md
├── ecommerce_sales_analytics_5000.csv
└── ecommerce_sales_transformed.csv
```

The CSV files should be added to the repository only if they are permitted to be shared. The source dataset is used for extraction, and the transformed dataset contains the additional year and month columns.

## 🚀 What I Learned

* Reading CSV data with Pandas.
* Converting date columns and extracting date components.
* Performing basic data-quality checks.
* Creating databases and tables in MySQL.
* Importing transformed data into a relational database.
* Writing SQL queries for business analysis.
* Investigating data inconsistencies during validation.

## 🔮 Future Improvements

* Automate the ETL process.
* Add reusable data-quality checks.
* Investigate and resolve revenue rounding differences.
* Add logging and error handling.
* Build a dashboard to visualize business insights.

## 👩‍💻 Author

**Rakshana Kumar**

Aspiring Data Analyst | Python | SQL | Pandas | MySQL

