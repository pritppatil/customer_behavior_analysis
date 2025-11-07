# customer_behavior_analysis
# 🛍️ Customer Shopping Behavior Analysis

## 🧭 Overview

This project analyzes **customer shopping behavior** using transactional data from 3,900 purchases across multiple product categories. The goal is to uncover insights into **spending patterns, product preferences, customer segments, and subscription behavior** to support data-driven business decisions.

The workflow includes **data cleaning and EDA in Python**, **SQL-based analysis on PostgreSQL Server**, and visualization through a **Power BI dashboard**. A final **Gamma presentation** summarizes the findings for stakeholders.

---

## 📂 Dataset

* **Source:** Dataset by **Amlan Mohanty**
* **File:** `customer_shopping_behavior.csv`
* **Size:** 3,900 rows × 18 columns
* **Key Features:**
  * **Customer Demographics:** `Age`, `Gender`, `Location`, `Subscription_Status`
  * **Purchase Details:** `Item_Purchased`, `Category`, `Purchase_Amount`, `Season`, `Size`, `Color`
  * **Shopping Behavior:** `Discount_Applied`, `Promo_Code_Used`, `Previous_Purchases`, `Frequency_of_Purchases`, `Review_Rating`, `Shipping_Type`
* **Missing Data:** 37 missing values in `Review_Rating` column

---

## 🧰 Tools & Technologies

| Category               | Tools Used                                  |
| ---------------------- | ------------------------------------------- |
| Data Preparation & EDA | Python (Pandas, NumPy)                      |
| SQL Analysis           | PostgreSQL Server                           |
| Data Visualization     | Power BI                                    |
| Presentation           | Gamma                                       |
| Version Control        | Git & GitHub                                |

---

## ⚙️ Project Workflow

### 1. Data Loading (Python)

* Imported dataset using `pandas`
* Explored structure with `df.info()` and `df.describe()`

### 2. Data Cleaning

* Handled 37 missing `Review_Rating` values using median imputation by product category
* Renamed columns to `snake_case` for consistency
* Created new columns:
  * `age_group` (binned customer ages)
  * `purchase_frequency_days` (calculated from transaction dates)
* Verified and dropped redundant column `promo_code_used`
* Exported cleaned dataset to PostgreSQL for SQL analysis

### 3. SQL Analysis

Performed structured queries to answer key business questions:

* **Revenue by Gender:** Compared total sales between male and female customers
* **High-Spending Discount Users:** Identified discount users exceeding the average purchase amount
* **Top 5 Products by Rating:** Ranked products with the best average reviews
* **Shipping Type Comparison:** Compared average spending between Standard vs. Express shipping
* **Subscribers vs. Non-Subscribers:** Measured average spend and total revenue
* **Discount-Dependent Products:** Listed top 5 products most purchased with discounts
* **Customer Segmentation:** Classified users as New, Returning, or Loyal
* **Top 3 Products per Category:** Highlighted category-wise best sellers
* **Repeat Buyers & Subscriptions:** Analyzed link between frequent buyers and subscription likelihood
* **Revenue by Age Group:** Quantified revenue contribution by age segment

### 4. Dashboard in Power BI

An **interactive Power BI dashboard** was created to visualize:

* Overall revenue and sales KPIs
* Gender and age group contributions
* Category-wise performance
* Discount usage impact
* Subscription and loyalty trends

📊 **Dashboard File:** `Customer Shopping Behavior Analysis.pbix`

---

## 📈 Results & Insights

1. **High-Revenue Age Groups:** Middle-aged customers (30–45) drive the highest sales.
2. **Subscription Benefits:** Subscribers spend ~25% more on average.
3. **Top Products:** Categories like *Clothing* and *Electronics* dominate revenue.
4. **Discount Behavior:** Certain products show strong discount dependency, reducing profit margins.
5. **Shipping Preferences:** Express shipping users contribute more per transaction.
6. **Customer Segmentation:** Loyal customers (≥5 purchases) form a small but high-value group.

---

## 💡 Business Recommendations

* **Boost Subscriptions:** Promote exclusive perks for subscribers.
* **Loyalty Programs:** Reward repeat buyers to increase retention.
* **Discount Policy:** Reassess discount-heavy products to protect margins.
* **Product Marketing:** Highlight top-rated items in campaigns.
* **Targeted Marketing:** Focus on high-spending demographics and express-shipping users.

---

## 🚀 How to Run the Project

### 1. Clone Repository

```bash
git clone https://github.com/pritppatil/customer-shopping-behavior.git
cd customer-shopping-behavior
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3.Open Data_Cleaning_Customer_Shopping_Behaviour.ipynb notebook
 
This file contains:

  * Data Import
   
  * Data exploration
   
  * Data cleaning
   
  * Connection to SQL Database
   

### 4. Load Data into SQL Database

* Create a database in SQL

* Run Python code to load data into SQL database

* Open customer_behavior_SQL_Queries.sql

* Answer Business Questions using SQL Queries


### 5. Connect the SQL Database to Power BI

* Open Customer Shopping Behavior Analysis.pbix

* Create interactive dashboard in Power BI



### 6. Create Project Report and Presentation

* Create project report

* Build presentation deck using Gamma AI

---

## 📘 Project Files

| File                                              | Description                           |
| ------------------------------------------------- | ------------------------------------- |
| `customer_shopping_behavior.csv`                  | Raw dataset                           |
| `Data_Cleaning_Customer_Shopping_Behaviour.ipynb` | Python script for data cleaning & EDA |
| `customer_behavior_SQL_Queries.sql`               | PostGre SQL queries                   |
| `Customer Shopping Behavior Analysis.pbix`        | Power BI dashboard                    |
| `Customer Shopping Behavior Analysis.docx`        | Detailed analytical report            |
| `Customer Shopping Behavior Analysis New.pdf`     | Final presentation deck               |

---

## 🧩 Future Enhancements

* Automate ETL pipeline for real-time updates
* Integrate predictive modeling for customer churn and purchase forecasting
* Deploy dashboard online (Power BI Service or Streamlit)

---

**Author:** Pritesh Patil
**Dataset Source:** Amlan Mohanty
**Contact:** [priteshprakashpatil@gmail.com]
**GitHub:** [github.com/pritppatil]
**LinkedIn:** [linkedin.com/in/priteshprakashpatil2507]
**License:** MIT License

