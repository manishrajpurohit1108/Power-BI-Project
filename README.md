# 📊 Superstore Sales Analysis – Power BI Project  

## 📝 Project Title  
**Superstore Sales Analysis Dashboard**  

## 🎯 Problem Statement / Goal  
The objective of this project is to analyze **Superstore sales data** and provide actionable business insights related to revenue, orders, customers, and products.  
The dashboards help in monitoring **sales trends, category performance, customer behavior, and regional contributions etc.** to support data-driven decision-making.  

---

## 📂 Dataset Details  
- **Dataset Name:** Superstore Sales Dataset  
- **Source:** Public sample dataset  
- **Columns (18 total):**  
  - `Row ID`, `Order ID`, `Order Date`, `Ship Date`, `Ship Mode`  
  - `Customer ID`, `Customer Name`, `Segment`, `Country`, `City`, `State`, `Postal Code`, `Region`  
  - `Product ID`, `Category`, `Sub-Category`, `Product Name`, `Sales`  

---

## 🔄 Steps Followed  

### 1. Data Loading & Cleaning  
- Loaded dataset into Power BI  
- Assigned correct data types to date and numeric fields  
- Removed **2 null-value rows**  

### 2. Calendar Table Creation  
- Built a **Calendar Table** with additional calculated columns:  
  - Year, Quarter, Month Number, Month Name, Day  
- Created a **date hierarchy** (Year → Quarter → Month → Day)  
- Built **location hierarchy** (Country → State → City) in the main table  
- Built **category hierarchy** (Category → Sub-Category → Product Name) in the main table  

### 3. Data Modeling  
- Established relationship between **Superstore_Sales table** and **Calendar table** using `Order Date` ↔ `Date`  

### 4. DAX Measures  
Created the following measures for analysis:  
- **Total Sales** = SUM(Sales)  
- **Total Orders** = DISTINCTCOUNT(Order ID)  
- **Total Customers** = DISTINCTCOUNT(Customer ID)  
- **Average Sales per Order (ASPO)** = Total Sales / Total Orders  
- **Growth Measures:**  
  - YoY% Sales, YoY% Orders, YoY% ASPO  
  - MoM% Sales, MoM% Orders, MoM% ASPO  
- **Conditional Formatting (CF):** Applied to highlight positive/negative growth in **green/red**  

### 5. Dashboard Design  
- Designed **two interactive dashboard pages**  
- Added **slicers** for Year, Month, and State filters  
- Added **navigation button/icon** to switch between dashboards  
- Added **info button (Q&A)** to allow users to ask questions and get more insights  
- Applied a **consistent purple-pink theme** for a professional look  

---

## 📑 Dashboards / Pages  

### **Page 1 – Sales Overview**  
- KPIs: **Total Sales, Total Orders, Average Sales per Order**, with comparisons vs last year & last month  
- **Sales Trends:** Sales by Date hierarchy (Line Chart), Sales by State (Map Chart)  
- **Top 10 Products by Sales** (Funnel Chart)  
- **Category-level insights:** Sales Contribution % & Average Order Value (Donut & Bar Chart)  

### **Page 2 – Customer & Product Insights**  
- **Sales by Sub-Category** (Treemap)  
- **Total Orders by Sub-Category** (Bar Chart)  
- **Top 10 Customers by Sales** (Table)  
- **Orders by Segment** – Consumer, Corporate, Home Office (Area Chart)  
- **Orders Contribution % by Category** (Donut Chart)  

---

## 🔑 Key Insights  
- 📈 **Total Sales:** $2.26M with **4,922 orders** and an **average sales per order of $459.48**  
- 🛒 **Category Contribution:** Technology leads with **36.6% of sales**, followed by Furniture and Office Supplies  
- 💵 **Top Product:** Canon imageCLASS 2200 Advanced Copier → **$61.6K sales**  
- 🌍 **Regional Insight:** Sales are concentrated on the **East & West coasts of the US**  
- 👥 **Customer Insight:** Sean Miller → Top customer with **$25K in sales**  
- 📊 **Segment Insight:** Consumer segment contributes **50%+ of total orders**  
- 🔻 **ASPO (Average Sales per Order)** declined slightly compared to last month/year  

---

## 🛠️ Tools Used  
- **Power BI** → Data cleaning, modeling, DAX measures, dashboards  

---

## 📸 Dashboard Screenshots  
### Page 1 – Sales Overview  
![Dashboard Page 1](Dashboard%20Page%201.png)  

### Page 2 – Customer & Product Insights  
![Dashboard Page 2](Dashboard%20page%202.png)  

---

✨ This project demonstrates an **end-to-end BI workflow**: from **data preparation → modeling → DAX calculations → visualization → business insights**.  
