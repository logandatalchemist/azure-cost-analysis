# azure-cost-analysis 
<img width="1992" alt="Screenshot 2025-06-28 at 3 50 22 PM" src="https://github.com/user-attachments/assets/6b457a60-fbf0-4246-b7f8-a683a9970013" />

# Azure Cost Analysis — Cloud BI Project

## Purpose

This project is a personal exploration into **cloud cost visibility** using an **anonymized Azure billing dataset**. My goal was to simulate the process of a **BI/Data Analyst** at a cloud-reliant organization:

- Understand spending patterns  
- Surface optimization opportunities  
- Practice cloud cost governance analysis  
- Use SQL + Tableau to tell a compelling data story

> While the dataset is from Kaggle and can't be verified as official, it realistically mimics the structure and semantics of Azure Cost reports. This made it a useful proxy for exploration.

---

## Tools Used

- **SQL (MySQL)** – Data exploration and aggregation  
- **Tableau** – Data visualization and storytelling  
- **Excel** – Quick checks and column understanding

---

## Project Stages

### 1. **Data Understanding**
- Cleaned and imported `anonymized_costs.json`
- Evaluated key fields: `MeterCategory`, `ResourceGroup`, `ResourceLocation`, `UsageDate`, `CostInBillingCurrency`
- Confirmed this dataset simulates a **single account’s** billing data

### 2. **SQL Exploration**
Foundational questions explored:
- Which services drive most cost?
- Where is cloud spend geographically concentrated?
- What is the monthly trend and volatility?
- Are there untagged or unassigned costs?
- Does the Pareto principle (80/20 rule) apply?


### 3. **Visualization in Tableau**
Final dashboard includes:
- KPI tiles (Total spend, Top service, Top 3 spend share)
- Cost over time with 7-day moving average
- Pareto chart for top services
- Cost by region
- Forecasting future spend
- Volatility vs. total spend (scatter plot)


### 4. **Insight Synthesis**
- **Top 3 services = 48% of total spend** → Opportunity to focus optimizations  
- **Westeurope dominates cloud region use** → Redundancy/risk management needed  
- **~$1.4K in unassigned region spend** → Potential tagging/policy issue  
- **Pareto holds** → 80% of cost comes from just 12 out of 49 services  
- **Daily spend is stable** → Predictable usage trend  
- **Volatility varies by service** → Target high-variability services for investigation  

---

## What I Learned

- How to simulate a realistic cloud BI workflow using anonymized data  
- Best practices for dual-axis visuals (e.g., Pareto) and cumulative line plots  
- Tradeoffs between different volatility metrics (std dev vs. min-max range)  
- Tableau parameter filters for date interactivity across dashboard  
- Importance of dashboard UX: grouping, tiling, tooltip design

---

## What I'd Do Differently

- Use real Azure exports from Cost Management + Billing  
- Enrich the dataset with tags or account hierarchy if available  
- Automate the data prep pipeline (e.g., Snowflake or dbt)  
- Evaluate cost efficiency with metrics like "cost per usage unit"

---

## Future Ideas

- Integrate real-time Azure spend via API  
- Build alerts for anomalies or mis-tagged spikes  
- Cross-cloud comparison (Azure vs AWS vs GCP)  
- Drill-down pages by resource group or service owner

---

## Acknowledgments

This dataset was sourced from https://www.kaggle.com/datasets/carrucciu/azure-costs and resembles Azure’s billing format, though anonymized. It provided a realistic simulation for building cloud cost intelligence.

Feel free to fork or use this project for learning and reference!

