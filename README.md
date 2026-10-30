# 📊 Executive Financial Performance Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Domain](https://img.shields.io/badge/Domain-Financial_Analytics-blue?style=for-the-badge)
![Data Modeling](https://img.shields.io/badge/Data_Modeling-Star_Schema-00758F?style=for-the-badge)
![Project](https://img.shields.io/badge/Project-Executive_Reporting-orange?style=for-the-badge)

An interactive, 3-page Power BI dashboard designed to give business leaders a clear view of company sales, regional growth, product profitability, and discount impacts.

---

## 📷 Dashboard Preview

### Page 1: Executive Summary
A high-level view showing total sales, overall profits, units sold, and year-over-year growth.

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/1217ad94-f99b-4c8d-9725-69379d1ccfa8" />

### Page 2: Product & Regional Analysis
A breakdown showing how different product lines perform across various countries and business segments.

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/2d24a3a7-e8a9-41d1-a249-40082a2ba738" />

### Page 3: Profitability & Discount Impact
An analysis comparing product costs, profit margins, and how offering discounts affects overall earnings.

<img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/7597d1fa-f6c3-40fa-88b8-9d0fe35b33a8" />

---

## 🎯 What This Project Does

The goal of this project was to take raw financial data and turn it into a clear, easy-to-use tool for decision-makers. 

* **Clean Data Layout:** Grouped related information into separate lookup tables (like products and locations) to keep the core sales data organized and fast to load.
* **Smart Data Rules:** Hid raw ID numbers and background calculations so report users only see clean, final metrics.
* **Organized Calculation Library:** Placed all custom formulas into a single `_Measures` folder so the report stays clean and easy to maintain.
* **User-Friendly Theme:** Designed with a sleek dark slate theme (`#111827` / `#1E293B`) and cyan accents (`#06B6D4`) to make numbers pop without straining the eyes.

---

## 📁 File & Folder Structure

```text
Executive_Financial_Performance_Dashboard.pbix
│
├── 📊 Page 1: Executive Summary (Main Sales & Growth Numbers)
├── 🗺️ Page 2: Product & Regional Analysis (Sales by Country & Item)
├── 💰 Page 3: Profitability & Discount Impact (Costs, Margins & Discounts)
└── ⚙️ Data Model: Organized Tables & Central Formula Folder
```

---

## 🛠️ Main Measures Used

Here are the primary measures used to power the key performance indicators:

### 1. Year-Over-Year Sales Growth (%)
Calculates how much total sales grew compared to the previous year:

```text
Sales YOY Growth % = 
   VAR SalesCurrentYear = [Total Sales]
   VAR SalesPriorYear = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Dim_Calendar'[Date]))
   RETURN
   DIVIDE(SalesCurrentYear - SalesPriorYear, SalesPriorYear, 0)
```

### 2. Profit Margin (%)
Shows how much profit is kept from every dollar of revenue:

```text
Profit Margin % = 
DIVIDE([Gross Profit], [Total Sales], 0)
```

---

## 💡 Key Takeaways & Lessons Learned

1. **Keep Dimensions Separate:** Splitting products, geography, and sales into distinct tables keeps the file running quickly and smoothly.
2. **Hide Unnecessary Fields:** Hiding database ID numbers prevents confusion and keeps the field list clean for anyone building visuals.
3. **Consistent Colors Matter:** Using a single dark theme across all pages helps users focus on the numbers rather than getting distracted by changing colors.

---

## ⚙️ How to View This Dashboard

1. Download the `Executive_Financial_Performance_Dashboard.pbix` file from this repository.
2. Open it using **Power BI Desktop** (available for free from Microsoft).
3. Click through the pages to explore the visuals and check out the data structure in the Model View tab.

---

## 🔒 Data Note

> **Disclaimer:** The data used in this project comes from the standard Microsoft Financial Sample dataset and was prepared solely for learning and demonstration purposes.

---

## 👩‍💻 Author

**Yenuli Withanage**  
*B.Sc. in Finance Undergraduate | University of Sri Jayewardenepura (USJ)*  
*AAT SL Level 3 Candidate*  

[LinkedIn Profile](https://www.linkedin.com) • [GitHub Repository](https://github.com/yenuli2005)
