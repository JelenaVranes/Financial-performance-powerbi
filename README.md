# 📊 Financial Performance Dashboard – Power BI Project

## 🧩 Overview
This Power BI project analyzes the financial performance of a company using the **Financial Sample** dataset provided by Microsoft. 
The dashboard highlights revenue trends, profitability, country performance, and segment-level insights.

The goal is to deliver clear, actionable business intelligence for decision-makers.

---

## 🗂 Dataset
Dataset source: Microsoft Financial Sample 
Included fields:
- Sales 
- Profit 
- Units Sold 
- COGS (Cost of Goods Sold) 
- Gross Margin 
- Segment 
- Country 
- Date 

Dataset is included in the **/data** folder.

---

## 🔧 Data Preparation
Minimal cleaning was required because the dataset is pre formatted.

Performed:
- Verified data types 
- Added DAX measures for revenue, profit, COGS, YoY performance 
- Added a proper date hierarchy for time analysis 

---

## 🧮 DAX Measures

```DAX
Total Revenue = SUM(financials[Sales])

Total Profit = SUM(financials[Profit])

Gross Margin % = DIVIDE([Total Profit], [Total Revenue])

Units Sold = SUM(financials[Units Sold])

Total COGS = SUM(financials[COGS])

YoY Revenue = 
CALCULATE([Total Revenue], DATEADD(financials[Date], -1, YEAR))

Profit Delta = [Total Revenue] - [Total COGS]
Show more lines
________________________________________
📈 Report Pages
1️⃣ Executive Overview
•	Total Revenue
•	Total Profit
•	Gross Margin %
•	Units Sold
•	Revenue Trend
•	Revenue by Country
•	Revenue by Segment
2️⃣ Profitability Analysis
•	Profit by Country
•	Sales vs Profit
•	Gross Margin % by Segment
•	Revenue/Profit Waterfall Chart
3️⃣ Regional Sales
•	Sales by Country
•	Units Sold by Country
•	Segment vs Country Heatmap
•	AVG Discount
________________________________________
🖼 Screenshots
Screenshots of the report pages are available in the /visuals folder:
•	Executive overview.png
•	Profitability.png
•	Regional_sales.png
________________________________________
💡 Insights (example)
•	Europe generates the highest revenue across all segments
•	Gross Margin is strongest in the Government and Midmarket segments
•	COGS significantly affects profitability in Consumer and Channel segments
•	Year-over-year trends show steady revenue growth
________________________________________
🧠 Tools Used
•	Power BI Desktop
•	Power Query
•	DAX
•	GitHub
________________________________________
📥 How to Use
1.	Download the .pbix file from the /pbix folder
2.	Open in Power BI Desktop
3.	Ensure the financials dataset from /data is connected
________________________________________
📬 Contact
Feel free to reach out via GitHub Issues or Discussions.

