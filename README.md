## 📊 Data-Driven-Order-Analytics-System-Using-MySQL-Python-SQLAlchemy

### 🔍 Project Summary

This project demonstrates a full **ETL (Extract, Transform, Load)** pipeline using **Python**, **Pandas**, and **SQL Server**, followed by **business-driven data analysis** using SQL. The dataset is sourced directly from **Kaggle** via the **Kaggle API**, processed in Python, and loaded into SQL Server for advanced querying and insights.

---

## 🛠️ Tech Stack & Tools

* **Languages:** Python, SQL
* **Libraries:** `pandas`, `sqlalchemy`, `zipfile`, `kaggle`
* **Database:** SQL Server (via ODBC connection)
* **Data Source:** Kaggle (Retail Orders Dataset)
* **Concepts Covered:** ETL, Feature Engineering, Data Cleaning, SQL Joins, Aggregations, Window Functions, Date Transformations

---

## 📥 Data Extraction & Loading (ETL)

### 1. **Data Download (Extract)**

* Dataset is downloaded using the **Kaggle API**.
* `kaggle.json` is configured for authenticated access.
* Downloaded as a ZIP and extracted using Python’s `zipfile` module.

### 2. **Data Loading & Cleaning (Transform)**

* Data is read using **`pandas.read_csv()`**.
* Null values are treated explicitly: values like `'Not Available'` and `'unknown'` are set as `NaN`.
* Columns are renamed to be lowercase and underscore-separated (e.g., `Order ID → order_id`).
* **Feature Engineering:**

  * `discount`, `sale_price`, and `profit` columns derived.
  * Unnecessary columns (`cost_price`, `list_price`, `discount_percent`) are dropped.
* `order_date` converted to datetime format for temporal queries.

### 3. **Database Load (Load)**

* Cleaned data is loaded into a **SQL Server** table (`df_orders`) using **SQLAlchemy**.
* Table creation and data insertion are handled via `pandas.to_sql()` with proper data types.

---

## 📈 Skills Demonstrated

* ✅ End-to-end **ETL pipeline**
* ✅ Working with **real-world, messy data**
* ✅ Hands-on **SQL querying**, including window functions
* ✅ Feature Engineering & Type Casting
* ✅ Using **Kaggle API** for reproducible workflows
* ✅ Loading data into **SQL Server** with SQLAlchemy
* ✅ Query optimization and business metric reporting
