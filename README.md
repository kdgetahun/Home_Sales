
markdown
Copy
Edit
# 🏡 Home Sales Data Analysis with PySpark

## 📌 Overview
This project focuses on performing data analysis on home sales data using **Apache Spark** and **SparkSQL**. It involves reading data from a CSV file hosted on AWS, running SQL-based queries to extract insights, optimizing performance using caching and partitioning, and comparing runtimes of different query approaches.

This was completed as part of a SparkSQL challenge to demonstrate the ability to work with distributed data and optimize queries using Spark's powerful tools.

---

## 💻 Technologies Used
- Python
- PySpark (SparkSession, SparkSQL, DataFrame API)
- Jupyter Notebook
- AWS S3 (for CSV data)
- Apache Parquet (for data output)

---

## 📁 Project Structure
- `Home_Sales.ipynb` – Jupyter notebook containing:
  - Data import and loading into a DataFrame
  - Creation of temporary views
  - Execution of complex SQL queries for metrics analysis
  - Use of caching/uncaching
  - Performance comparison (cached vs. uncached vs. partitioned)
  - Exporting partitioned data to Parquet

---

## 🔍 Key Analytical Tasks

### ✅ Query-Based Analysis:
1. **Average price of four-bedroom homes sold per year.**
2. **Average price of homes with 3 beds and 3 baths by year built.**
3. **Average price for homes with 3 beds, 3 baths, 2 floors, and ≥2,000 sqft by year built.**
4. **Average home price per 'view' rating for properties priced ≥$350,000.**
   - Runtime comparison: uncached vs. cached vs. partitioned data.

### 🧠 Optimization Techniques:
- Used `cacheTable()` to improve performance for repeated queries.
- Verified caching with `is_cached`.
- Partitioned data by `date_built` using Parquet format for better query performance.
- Uncached temporary table and verified uncaching status.

---

## 📝 Notes
- Data was sourced from AWS S3 and formatted for processing with PySpark.
- Runtimes for various query execution methods were recorded and compared.
- All calculations round numeric values to two decimal places for readability.
