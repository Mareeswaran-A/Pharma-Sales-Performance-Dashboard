Pharma Sales Performance Analysis Dashboard
===========================================

A comprehensive Power BI project analyzing pharmaceutical sales performance to derive actionable business insights.

Repository Structure
--------------------
Pharma-Sales-Analysis/
├── Pharma_Sales.pbix           -> Main Power BI Dashboard File
├── Pahrma_Source.xlsx          -> Sales Transaction Data
├── Metrics.xlsx                -> Target Metrics for Reps and Teams
├── README.txt                  -> Project Documentation (this file)

Project Objective
-----------------
This Power BI dashboard enables the business to:
- Monitor total and YTD revenue
- Evaluate target achievement by team and individual
- Analyze product class and city-wise revenue trends
- Assess sales rep performance
- Understand the impact of marketing channels on sales
- Use time intelligence slicers for dynamic filtering

Tools & Technologies
--------------------
- Power BI Desktop
- DAX & Power Query
- Excel (for data sources)
- Advanced Data Modeling
- Slicers, KPI cards, and dynamic visuals

Dashboard Features
------------------
Page 1: Sales Overview
- KPIs for Total Revenue, YTD Revenue, SPLY
- Dynamic slicers (Year, Month, Quarter, Team)
- Revenue by Product Class, Channel, City

Page 2: Target & Volume Insights
- Total vs. Achieved Targets
- Volume Performance by Product and Team
- Team-wise achievement with grouped bar charts

Page 3 (Planned): Rep & Marketing Performance
- Revenue by Sales Rep (Top/Bottom)
- Channel Performance Analysis
- Team-level contribution breakdown

DAX Highlights
--------------
Total Revenue =
    SUM(Sales[Revenue])

Total Revenue YTD =
    CALCULATE([Total Revenue], DATESYTD('Date_Table'[Date]))

Target Achievement % =
    DIVIDE([Actual Target YTD], [Total Target YTD], 0)

SPLY Revenue =
    CALCULATE([Total Revenue], SAMEPERIODLASTYEAR('Date_Table'[Date]))

Author
------
Mareeswaran A.
Business Analyst | Power BI Developer | Data Enthusiast

LinkedIn: https://www.linkedin.com/in/mareeswarana

Email: mareeswarana465@gmail.com

How to Use
----------
1. Clone the repository or download the ZIP.
2. Open Pharma_Sales.pbix in Power BI Desktop.
3. Refresh data if needed using Excel files:
   - Pahrma_Source.xlsx
   - Metrics.xlsx
4. Interact using slicers and visuals.

Future Enhancements
-------------------
- Add drill-through pages for detailed sales rep profiles.
- Integrate forecasting using Power BI’s analytics.
- Deploy to Power BI Service with Row-Level Security (RLS).
- Implement email subscriptions for scheduled insights.

License
-------
This project is licensed under the MIT License - feel free to use, fork, and build upon it for learning or internal use.
