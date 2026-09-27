# 📊 Hybrid E-Commerce Sales Analyser (Python & SQL Engine)

An end-to-end analytical data pipeline designed to ingest, clean, and model complex transactional data from the classic **UK Online Retail Dataset**. 

This portfolio project showcases a **hybrid architecture** that uses Python for programmatic data cleansing/transformation and an In-Memory SQL Engine to run corporate business intelligence queries.

## 🚀 Key Architectural Features
- **Robust Data Cleansing:** Handled real-world spreadsheet issues such as duplicate records, cancelled orders (negative values), null customer attributes, and unformatted data types.
- **In-Memory SQL Processing:** Leveraged an explicit `:memory:` SQLite relational database structure to bypass cloud-computing disk input/output bottlenecks, achieving ultra-high-speed query processing.
- **Relational Aggregations:** Utilized complex SQL windowing, string manipulation techniques (`strftime`), and metrics grouping to compute standard retail key performance indicators (KPIs).

## 🛠️ Tech Stack & Libraries
- **Language:** Python
- **Database Engine:** SQLite (Structured Query Language)
- **Data Wrangling:** Pandas
- **Data Storytelling & Visualization:** Matplotlib, Seaborn

## 📈 Business Insights Extracted
1. **Executive KPIs:** Programmatically determined total unique transactional volume, active customer counts, global reach, and gross scale.
2. **Temporal Performance Analysis:** Formatted raw transaction timestamps using SQL rules to track seasonal revenue growth patterns monthly.
3. **Operational Purchase Timing Spikes:** Traced sales counts by hour of day to identify optimal slots for high-impact commercial marketing pushes.
4. **VIP Customer Retention Identification:** Isolated maximum transactional frequencies and life-cycle values per client to track brand stickiness.

## 💻 Sample Project Queries Embedded
```sql
-- Isolating seasonal trends and scaling patterns over time
SELECT 
    strftime('%Y-%m', InvoiceDate) as Month, 
    ROUND(SUM(TotalSales), 2) as Monthly_Revenue
FROM sales
GROUP BY Month
ORDER BY Month;
```

## 📊 Sample Visual Analytics Output
*The Jupyter notebook pipeline automatically processes outputs into structured Seaborn dashboards displaying multi-axis charts tracking monthly revenue streams, order density distributions, and product contribution matrix curves.*

