# 📊 Power BI Sales Analytics Dashboard – Superstore Dataset

This project showcases an end-to-end **Sales Analytics Dashboard** built in **Power BI** using the publicly available **Superstore dataset**. It simulates a retail business operating across various U.S. regions and provides insights into key business metrics like sales, profit, discount, and returns.

---

## 📂 Dataset Source

- Dataset: [Superstore Dataset – Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
- Format: Excel (`Sample - Superstore.xls`) or CSV
- Industry: Retail / E-commerce (Office Supplies, Technology, Furniture)
- Country: United States

---

## 🛠 Tools & Technologies

| Tool        | Purpose                          |
|-------------|-----------------------------------|
| Power BI    | Dashboard development             |
| Power Query | Data cleaning and transformation  |
| DAX         | Calculated KPIs and logic         |
| Excel       | Source data format                |

---

## 📈 Key Objectives

- Track overall and segmented sales performance
- Identify top and bottom-performing product categories
- Analyze the impact of discounts on profitability
- Evaluate return rates across segments and regions
- Enable user-driven filtering and slicing of insights

---

## 📐 Data Model & Relationships

- **Orders Table**: Contains transactional data (Sales, Profit, etc.)
- **Returns Table**: Contains returned order IDs
- **Relationship**: 
  - `Orders[Order ID]` → `Returns[Order ID]`

---

## 🧮 DAX Measures

```DAX
Total Sales = SUM(Orders[Sales])
Total Profit = SUM(Orders[Profit])
Total Quantity = SUM(Orders[Quantity])
Average Discount = AVERAGE(Orders[Discount])
Profit Margin = DIVIDE([Total Profit], [Total Sales])
Returned Orders = COUNTROWS(Returns)
Total Orders = DISTINCTCOUNT(Orders[Order ID])
Return Rate = DIVIDE([Returned Orders], [Total Orders])
