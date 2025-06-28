# azure-cost-analysis
<img width="1992" alt="Screenshot 2025-06-28 at 3 50 22 PM" src="https://github.com/user-attachments/assets/6b457a60-fbf0-4246-b7f8-a683a9970013" />


This project analyzes anonymized Azure cloud cost data to uncover trends, identify high-impact services, and detect potential optimization opportunities. Using SQL for data exploration and Tableau for interactive dashboards, the analysis focuses on spend distribution, regional patterns, service volatility, and Pareto-driven prioritization.

The final dashboard is built to support stakeholders in understanding cost behavior and driving smarter cloud strategy decisions.



Project Overview

This project explores anonymized Azure cloud cost data using SQL and Tableau to simulate a real-world business intelligence engagement. The goal is to identify cost drivers, service usage patterns, and opportunities for optimization using industry-standard analytics practices.

⸻

Objectives
	•	Familiarize with Azure cloud billing structures
	•	Use SQL to clean and explore cost data
	•	Design an interactive Tableau dashboard
	•	Apply analytical techniques like Pareto analysis and volatility scanning

⸻

Dashboard Features

1. KPI Summary Tiles
	•	Total Spend
	•	Number of Services, Regions, and Resource Groups
	•	Top Service and Region by Cost

2. Pareto Chart
	•	Cost distribution by MeterCategory
	•	Cumulative spend to identify 80/20 threshold

3. Cost by Region
	•	Highlights dominant regions and flags “Unassigned” spend

4. Spending Over Time + Moving Average
	•	Daily spend trend with 7-day moving average to identify consistency or volatility

5. Top 5 Cost-Driving Services
	•	Bar chart with percentage of total spend

6. Service Volatility Scatter Plot
	•	Visualizes volatility (max-min variation) against average daily cost
	•	Quadrants for segmenting high-risk services

⸻

SQL Exploration Highlights

SQL was used to:
	•	Validate dataset integrity (row count, null checks)
	•	Analyze top services and regions by cost
	•	Group and aggregate data for Pareto thresholds
	•	Calculate cost volatility per MeterCategory

A link to my queries here: 


⸻

Key Insights
	•	Pareto principle holds: ~80% of spend comes from 12 out of 49 services
	•	High concentration in West Europe: Potential cost redundancy or lack of region optimization
	•	Service volatility varies widely: Certain services show cost spikes, hinting at scaling or mismanagement

⸻

What I’d Do Differently
	•	Integrate more granular Azure metadata (e.g., tags, SKUs)
	•	Simulate a multi-account environment for broader analysis
	•	Add anomaly detection models for forecasting or alerting

⸻

Files
	•	anonymized_costs.json - Raw dataset
	•	sql_exploration.sql - SQL scripts used for analysis
	•	azure_dashboard.twbx - Tableau packaged workbook
	•	preview.png - Dashboard screenshot

⸻

Skills Demonstrated
	•	SQL (aggregations, filtering, joins)
	•	Tableau (dashboard design, calculated fields, parameters)
	•	Cloud cost analysis
	•	Data storytelling

⸻

📣 Acknowledgments

This dataset was sourced from [Kaggle] and resembles Azure’s billing format, though anonymized. It provided a realistic simulation for building cloud cost intelligence.

⸻

Feel free to fork or use this project for learning and reference!
