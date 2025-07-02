# Walmart Data Analysis: End-to-End SQL + Python + Power BI Project

## Project Overview

![Project Pipeline](https://github.com/PrachiSwarnim/walmart_analysis/blob/main/walmart_cover.jpg)

This end-to-end Walmart Sales Data Analysis project combines Python for data preprocessing and SQL for advanced insights extraction. It uncovers key business trends across branches, product lines, payment methods, and customer behaviors. The insights are visualized through an interactive Power BI dashboard, enabling data-driven decision-making on sales performance, revenue patterns, and customer trends.

---

## Project Steps
## 1. Set Up the Environment
- **Tools Used:** Visual Studio Code (VS Code), Python, MySQL, Power BI
- **Objective:** Build a clean, structured workspace for seamless development, data processing, SQL querying, and visualization.

## 2. Configure Kaggle API for Data Access
- **Step 1:** Obtain your Kaggle API token from Kaggle under Account Settings.
- **Step 2:** Place the downloaded kaggle.json file in the following directory:
  ```bash
  C:\Users\<YourUsername>\.kaggle\
  ```
- **Step 3:** Use the command below to download datasets directly into your project folder:
  ```bash
  kaggle datasets download -d najir0123/walmart-10k-sales-datasets
  ```

## 3. Data Acquisition
- **Source:** [Walmart Sales Dataset](https://www.kaggle.com/datasets/najir0123/walmart-10k-sales-datasets)
- **Storage:** Organize the dataset under a ```data/``` directory for easy access.

## 4. Install Required Libraries & Load Data
- **Install Python Libraries:**
  ```bash
  pip install pandas numpy sqlalchemy mysql-connector-python
  ```
- **Data Loading:** Import data into a Pandas DataFrame for exploration, cleaning, and transformation.

## 5. Initial Data Exploration
- **Goals:**
  - Understand data distribution
  - Check data types and schema
  - Detect missing values or anomalies
- **Methods:**
  - Use Pandas functions like:
    ```bash
    df.info(), df.describe(), df.head()
    ```
## 6. Data Cleaning Pipeline:
- **Duplicate Handling:** Remove redundant records to ensure data integrity.
- **Missing Values:** Impute, fill, or remove nulls based on significance.
  **Data Type Correction:**
  - Convert date columns to ```datetime```
  - Ensure numeric columns (like revenue or quantity) are floats or integers
- **Currency & String Formatting:** Clean up currency symbols or inconsistent string patterns.
- **Data Validation:** Confirm there are no outliers, inconsistencies, or logical mismatches.

## 7. Feature Engineering:
- **Derived Columns:**
  - **Total Revenue/Amount:**
    ```bash
    df['total_amount'] = df['unit_price'] * df['quantity']
    ```
  - **Time-based Features:** Extract year, month, day, hour for temporal analysis.
  - **Categorical Segmentation:** Payment type grouping, time-of-day buckets (morning, afternoon, etc.).
- **Purpose:** Enrich the dataset for deeper insights in SQL and Power BI.

## 8. Data Loading into MySQL Database
- **Establish Connection:** Use SQLAlchemy to create an engine and connect Python with MySQL.
- **Table Creation:** Auto-generate SQL tables from DataFrame schemas.
- **Data Insertion:** Push cleaned and feature-engineered data into MySQL for persistent storage and query-based analysis.
- **Validation:** Run basic SQL queries (```SELECT *```, ```COUNT(*)```, ```LIMIT```) to verify successful insertion.

## 9. SQL Analysis — Business Problem Solving
- **Address complex business queries, such as:**
  - **Revenue Trends:** Across years, branches, and categories.
  - **Top Product Categories:** What sells best and where.
  - **Time-Based Sales Patterns:** Identify high-performing hours, days, or months.
  - **Payment Method Analysis:** Customer preferences by location or time.
  - **Revenue Drop Alerts:** Branches or categories with negative YoY growth.
  - **Profitability Metrics:** Breakdown by branch, category, or time.

## 10. Power BI Analysis
- **Revenue Analysis:** Tracked revenue trends YoY by branch and product line.
- **Customer Behavior:** Analyzed purchase patterns by day, time, and rating.
- **Branch Performance:** Compared branch revenues and flagged revenue drops.
- **Sales Trends:** Visualized peak sales hours and days using heatmaps.
- **Top N Analysis:** Identified top-performing branches/products dynamically.
- **Payment Method:** Monitored shifts in payment preferences over time.
- **Transaction Volume:** Evaluated how transaction count impacts revenue.
- **Time Series:** Analyzed monthly and yearly revenue seasonality patterns.
- **Geographical Analysis:** Visualized revenue distribution by branch location.
     
## Requirements

- **Python 3.8+**
- **SQL Databases**: MySQL
- **Python Libraries**:
  - `pandas`, `numpy`, `sqlalchemy`, `mysql-connector-python`
- **Kaggle API Key** (for data downloading)

## Getting Started

1. Clone the repository:
   ```bash
   git clone <repo-url>
   ```
2. Install Python libraries:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up your Kaggle API, download the data, and follow the steps to load and analyze.

---

## Project Structure

```plaintext
|-- data/                     # Raw data and transformed data
|-- sql_queries/              # SQL scripts for analysis and queries
|-- notebooks/                # Jupyter notebooks for Python analysis
|-- README.md                 # Project documentation
|-- requirements.txt          # List of required Python libraries
|-- main.py                   # Main script for loading, cleaning, and processing data
```
---

## Results and Insights

This section will include your analysis findings:
- **Sales Insights**: Key categories, branches with highest sales, and preferred payment methods.
- **Profitability**: Insights into the most profitable product categories and locations.
- **Customer Behavior**: Trends in ratings, payment preferences, and peak shopping hours.

---

## Acknowledgments

- **Data Source**: Kaggle’s Walmart Sales Dataset
- **Inspiration**: Walmart’s business case studies on sales and supply chain optimization.

---
"# walmart_analysis" 
"# walmart_analysis" 
