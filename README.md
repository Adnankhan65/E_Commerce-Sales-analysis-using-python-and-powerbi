# E-Commerce Business Intelligence Dashboard

## 📌 Project Overview

This project is an end-to-end E-Commerce Business Intelligence Dashboard developed using Python and Power BI. The goal of the project is to analyze sales performance, customer behavior, product profitability, returns analysis, and business KPIs through interactive visualizations and data-driven insights.

The project covers the complete analytics workflow including:

* Data cleaning and preprocessing
* Handling missing values and duplicates
* Data transformation using Python (Pandas)
* Exploratory Data Analysis (EDA)
* Data modeling in Power BI
* DAX measure creation
* Interactive dashboard development

---

# 🛠️ Tools & Technologies Used

* Python
* Pandas
* Microsoft Power BI
* Power Query
* DAX
* Excel / CSV Dataset

---

# 📂 Dataset Information

The project contains the following datasets:

## 1️⃣ Clean_Ecommerce_Data

Main transactional dataset containing:

* Orders
* Customers
* Products
* Revenue
* Profit
* Supplier information

### Columns

* Order_ID
* Order_Date
* Customer_ID
* Product_ID
* Quantity
* Unit_Price
* Discount
* Payment_Method
* Order_Status
* Name
* City
* Signup_Date
* Age
* Gender
* Category
* Cost_Price
* Supplier
* Total_Revenue
* Profit

---

## 2️⃣ Returns_Messy

Contains product return details.

### Columns

* Order_ID
* Return_Reason

---

## 3️⃣ Marketing_Messy

Contains marketing campaign data.

### Columns

* Date
* Channel
* Spend
* Clicks

---

# 🧹 Data Cleaning & Preprocessing

Data preprocessing was performed using Python and Pandas.

## Tasks Performed

* Removed duplicate records
* Handled missing values
* Standardized column names
* Converted date columns into datetime format
* Cleaned inconsistent categorical values
* Merged multiple datasets
* Created calculated fields for analysis

---

# 📊 Exploratory Data Analysis (EDA)

Performed exploratory data analysis to identify:

* Revenue trends
* Profit distribution
* Customer purchasing behavior
* Product performance
* Return patterns
* Marketing effectiveness

---

# 📈 Power BI Dashboard

The dashboard was built using Power BI with interactive visuals and DAX measures.

---

# 📑 Dashboard Pages

## 1️⃣ Executive Overview

### KPIs

* Total Revenue
* Total Profit
* Profit Margin %
* Return Rate %
* Average Order Value

### Visualizations

* Monthly Sales Trend
* Category Revenue Analysis
* Payment Method Distribution
* Customer Count

---

## 2️⃣ Customer Insights & Behavior

### Visualizations

* Repeat vs New Customers
* Top 10 Customers
* City-wise Sales Analysis
* Customer Lifetime Value (CLV)

---

## 3️⃣ Product & Supplier Performance

### Visualizations

* Category Profitability
* Return Reason Breakdown
* Top 10 Products
* Supplier Performance Analysis

---

---

# 📐 Data Modeling

Relationships were created between:



A star schema approach was followed for better performance and scalability.

---

# 🧮 Important DAX Measures

## Total Revenue

```DAX
Total Revenue =
SUM(Clean_Ecommerce_Data[Total_Revenue])
```

## Total Profit

```DAX
Total Profit =
SUM(Clean_Ecommerce_Data[Profit])
```

## Profit Margin %

```DAX
Profit Margin % =
DIVIDE([Total Profit], [Total Revenue]) * 100
```

## Return Rate %

```DAX
Return Rate % =
DIVIDE(
    COUNT(Returns_Messy[Order_ID]),
    DISTINCTCOUNT(Clean_Ecommerce_Data[Order_ID])
) * 100
```

## Customer Lifetime Value (CLV)

```DAX
CLV =
CALCULATE(
    SUM(Clean_Ecommerce_Data[Total_Revenue]),
    ALLEXCEPT(
        Clean_Ecommerce_Data,
        Clean_Ecommerce_Data[Customer_ID]
    )
)
```

---

# 🎯 Key Business Insights

* Identified top-performing product categories
* Analyzed customer purchasing behavior
* Evaluated supplier performance
* Monitored return trends and reasons
* Measured sales and profit growth trends
* Evaluated marketing spend effectiveness

---

# 🚀 Project Outcome

The dashboard helps businesses:

* Monitor KPIs effectively
* Identify profitable products and customers
* Track customer retention
* Improve operational decision-making
* Analyze revenue and profit trends interactively

---

# 📸 Dashboard Preview

![Model View](https://github.com/Adnankhan65/E_Commerce-Sales-analysis-using-python-and-powerbi/blob/main/dashboardpg1.png)
![Model View](https://github.com/Adnankhan65/E_Commerce-Sales-analysis-using-python-and-powerbi/blob/main/dashboardpg2.png)
![Model View](https://github.com/Adnankhan65/E_Commerce-Sales-analysis-using-python-and-powerbi/blob/main/dashboardpg3.png)

---

# 🔗 GitHub Repository Structure

```text
├── Data
├── Python_Data_Cleaning
├── PowerBI_Dashboard
├── Dashboard_Screenshots
├── README.md
```

---

# 👨‍💻 Author

Adnan Khan

Aspiring Data Analyst skilled in:

* Python
* SQL
* Power BI
* Data Visualization
* Data Cleaning

