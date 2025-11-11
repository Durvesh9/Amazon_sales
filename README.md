# 🛒 Amazon India Sales Analysis – Power BI Project

## 📊 Project Overview
This project analyzes **Amazon India Sales Data** to uncover business insights such as revenue trends, fulfillment performance, and regional growth.  
It covers the complete process from **data cleaning** to **Power BI dashboarding** and **report generation**.

---

## 🎯 Objectives
- Clean and prepare raw sales data for analysis  
- Identify key business metrics and KPIs  
- Visualize sales performance across categories, states, and fulfillment types  
- Build a Power BI dashboard for dynamic insights  
- Provide actionable business recommendations  

---

## 🧾 Dataset Summary
- **Records:** 120,000+ orders  
- **Columns:** 24 fields (Order ID, Date, Category, Amount, Qty, State, City, Fulfillment, Status, etc.)  
- **Period Covered:** 1 year of Amazon India order data  
- **Source:** Internal dataset (anonymized)

---

## ⚙️ Tools Used
| Purpose | Tools |
|----------|--------|
| Data Cleaning | Python (Pandas, NumPy) |
| Visualization & Dashboard | Power BI |
| Documentation & Reporting | PowerPoint / PDF |
| Version Control | Git & GitHub |

---

## 📈 Dashboard Highlights
**Dashboard File:** `Amazon_sales.pbix` (open in Power BI Desktop)

### 🟦 Page 1: Sales Overview
- Total Sales, Total Orders, Quantity Sold, Average Order Value  
- Monthly Sales Trend  
- Sales by Category (Bar Chart)  
- Sales by State (Map View)  
- Fulfillment Type Share (Pie Chart)  

### 🟨 Page 2: Order & Fulfillment Analysis
- Delivered vs Cancelled Orders  
- Fulfillment Rate %  
- Courier Status Performance  
- Sales by Channel (Online, Merchant, etc.)  

### 🟩 Page 3: Product & Regional Insights
- Top 10 Cities by Sales  
- Category vs State Matrix  
- Quantity vs Revenue (Scatter Plot)  
- KPIs: Top Category, Top City, Top State  

---

## 💡 Key Insights
- **Maharashtra, Delhi, and Karnataka** drive the highest revenue.  
- **Electronics and Apparel** dominate category sales.  
- **Fulfilled-by-Amazon** (FBA) orders show better delivery success and lower cancellations.  
- **Promotional orders** increase sales volume but slightly reduce AOV.  
- **Tier-2 cities** show emerging growth opportunities.  

---

## 📊 KPIs & Measures (Power BI DAX)
```DAX
Total Sales = SUM(Sales[Amount])
Total Orders = DISTINCTCOUNT(Sales[Order ID])
Average Order Value = DIVIDE([Total Sales], [Total Orders])
Orders Delivered = CALCULATE([Total Orders], Sales[Status] = "Delivered")
Cancelled Orders = CALCULATE([Total Orders], Sales[Status] = "Cancelled")
Fulfillment Rate = DIVIDE([Orders Delivered], [Total Orders])
