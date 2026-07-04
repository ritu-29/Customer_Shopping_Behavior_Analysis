# Customer_Shopping_Behavior_Analysis
Data Analytics project analyzing 3,900+ customer records using Python, SQL, and Power BI, including data cleaning, feature engineering, advanced SQL (CTE, window functions), and interactive dashboard for business insights.


## 📌 Project Overview
This project analyzes **customer shopping behavior** using a real-world dataset from Kaggle.  
It combines **Python, SQL, and Power BI** to perform data cleaning, transformation, advanced analysis, and interactive visualization.

## 📊 Dataset Information
- 📁 Source: Kaggle
- 📦 Records: **3,900 rows**
- 📊 Columns: **18 features**

### Key Columns:
- Customer ID
- Age, Gender
- Item Purchased, Category
- Purchase Amount (USD)
- Location
- Season
- Review Rating
- Subscription Status
- Discount Applied
- Payment Method
- Frequency of Purchases

---

## 🐍 Python (Data Cleaning & Feature Engineering)

### 🔹 Libraries Used
- Pandas
- NumPy
- SQLAlchemy
- PyMySQL

### 🔹 Data Cleaning Steps
- Checked null values using `isnull()`
- Filled missing **Review Rating** using **median by category**
- Standardized column names (lowercase + underscores)
- Renamed columns for better readability

### 🔹 Feature Engineering
- Created **age_group** using `pd.qcut()`
- Converted purchase frequency into **days**
- Removed redundant column (`promo_code_used`)
- Verified data consistency

---

## 🧠 SQL (Data Analysis & Business Queries)

### 🔹 Concepts Used
- ✅ Aggregations (`SUM`, `AVG`, `COUNT`)
- ✅ Subqueries
- ✅ **CTE (Common Table Expression)**
- ✅ **Window Functions (RANK)**
- ✅ CASE statements (Segmentation)
- ✅ Filtering & Grouping
- ✅ Conditional Aggregation

---

### 🔍 Key SQL Insights

#### 1. Revenue by Gender
- Compared total revenue between male and female customers

#### 2. Top Customers
- Identified top 5 highest spending customers

#### 3. Discount Behavior
- Customers using discount but spending above average

#### 4. Product Performance
- Top-rated products based on review rating

#### 5. Shipping Analysis
- Compared average purchase across shipping types

#### 6. Customer Segmentation
- New, Returning, Loyal customers using CASE logic

#### 7. Window Function
```sql
RANK() OVER(PARTITION BY category ORDER BY SUM(purchase_amount) DESC)
````

#### 8. CTE Example

```sql
WITH customer_type AS (...)
```

#### 9. Subscription Analysis

* Compared revenue and spending of subscribed vs non-subscribed customers

---

## 📊 Power BI (Dashboard & Visualization)

### 🔹 Key KPIs

* 💰 Total Revenue
* 🛒 Average Purchase Amount
* 👥 Total Customers
* ⭐ Average Review Rating
* 📈 Subscription Rate

---

### 🔹 Measures (DAX)

* Total Revenue
* Average Purchase
* Subscription Rate
* Revenue per Customer
* Revenue with/without Discount
* Repeat Customer Rate
* Top Customers

---

### 🔹 Dashboard Features

* Interactive Filters (Slicers):

  * Gender
  * Category
  * Season
  * Location
  * Age Group
  * Subscription Status

* Visualizations:

  * Bar Charts (Category, Age Group)
  * Donut Chart (Gender)
  * Pie Chart (Customer Segment)
  * Clustered Bar (Seasonal Revenue)
  * Top 5 States Revenue
  * Payment Method Analysis

---

## 📈 Key Insights

* 📊 Clothing category generates highest revenue
* 👥 Majority customers are non-subscribers
* 🎯 Repeat customers contribute significantly to revenue
* 📉 Subscription does not drastically increase spending but still valuable

---

## 🛠️ Tools & Technologies

* 🐍 Python (Pandas, NumPy)
* 🗄️ MySQL
* 📊 Power BI
* 🔗 SQLAlchemy (Data transfer)

---

## 🔄 Workflow

1. Data Collection (Kaggle)
2. Data Cleaning (Python)
3. Feature Engineering
4. Load into MySQL
5. SQL Analysis (Advanced Queries)
6. Data Visualization (Power BI)
7. Dashboard Creation

---





