# 📊 Pricing Dashboard – Mini Project 1

Welcome to my Power BI Mini Project! This interactive dashboard visualizes pricing and sales performance data for over 345,000 transactions extracted from SAP. It's designed to showcase my data modeling, DAX, and business intelligence skills — especially in analyzing trends, contribution margin, and customer value.

---

## 🧠 Business Context

The data simulates a real-world manufacturing sales environment, with detailed line-level transaction data including:

- Part number (Material)
- Net sales and cost
- Sales district and territory manager
- Sold-To and End User customer groups
- Date of transaction

The goal: Provide at-a-glance KPIs and dynamic insights into **sales performance**, **margins**, and **top customers**, enabling better pricing decisions.

---

## 🔍 Dashboard Features

✅ Clean KPI summary cards:
- Total Net Sales  
- Total Cost  
- Contribution Margin  
- Contribution Margin %

✅ Trend Visuals:
- Net Sales over Time by Product Group  
- Sales by Sales District  
- Contribution Margin by Material

✅ Interactive Controls:
- Slicers for Year, Main Group, Customer Group  
- Top 5 Customers by Net Sales (dynamic filter)  
- YTD / QTD Measures with Date Slicer support

---

## 🧮 DAX Highlights

```DAX
Contribution Margin = [Total Net Sales] - [Total Order Cost]

Contribution Margin % = 
    DIVIDE([Contribution Margin], [Total Net Sales], 0)

Net Sales YTD = 
    CALCULATE([Total Net Sales], DATESYTD('DateTable'[Date]))

Net Sales QTD = 
    CALCULATE([Total Net Sales], DATESQTD('DateTable'[Date]))
```

## 📁 File Structure
- `PricingDashboard.pbix` – Power BI report file (open with Power BI Desktop)
- `README.md` – This documentation
- `data/`
