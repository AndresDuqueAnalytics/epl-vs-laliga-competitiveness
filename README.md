# EPL vs La Liga — Competitive Balance Analysis (2023/24)

## Overview
This project analyzes the competitive balance between the Premier League and La Liga during the 2023/24 season.  
The goal is to evaluate whether the Premier League is more competitive **structurally**, not just perceptually.

The analysis focuses on:
- Points distribution
- Mid-table strength
- Away-match performance
- Offensive depth and efficiency

This case study was developed as a portfolio project using real match-level data and standard analytical workflows used in business and BI contexts

## Business Question
Is the Premier League truly more competitive than La Liga, and if so, in what measurable, structural ways?

## Key Insight (TL;DR)
The Premier League is structurally more competitive than La Liga in 2023/24, driven by stronger mid-table resistance and a higher away-performance floor, even though La Liga produces tighter individual match scorelines.

## Context
This project evaluates league competitiveness from an investment and operations perspective, focusing on competitive balance, mid-table resistance, and performance distribution rather than title outcomes or star players.

## Data & Tools
- Public match-level datasets (Kaggle)
- SQL (SQLite) for validation and aggregation
- Power BI for visualization
- Excel for initial cleaning and schema alignment

  ## Repository Structure
- /dashboard  
  Power BI dashboard (.pbix) and exported PDF preview

- /sql  
  SQL scripts used for validation, table creation, and summary outputs (SQLite)

- /data  
  Cleaned datasets used for analysis (CSV)

- /docs  
  Case study documentation (Ask/Prepare/Process/Analyze/Share/Act)

## How to Review This Project
1. Start with `/docs/Executive_Report.pdf.`
2. Review `/dashboard/` for visuals
3. Inspect `/sql/` for transformation logic
4. Read `/docs/Technical_Appendix.md` for methodology

## Notes on Data
Raw CSVs are not included to respect dataset licensing.  
All data sources are public (Kaggle) and documented in `/data/README.md`.

## Deliverables
- 📊 **Power BI Dashboard:** `/dashboard/EPL_LaLiga_Dashboard.pdf`
- 📄 **Full Case Study Report:** `/docs/Case_Study_Report.md`
- 🛠 **Technical Appendix:** `/docs/Technical_Appendix.md`
- 🧮 **SQL Logic:** `/sql/epl_laliga_competitiveness_analysis.sql`

### Supporting Analysis — EPL Exploratory Dashboard

In addition to the comparative analysis, I built an exploratory Power BI dashboard using the EPL match-level dataset. The purpose of this dashboard was to understand team performance distributions, efficiency patterns, and league-wide variance before conducting cross-league comparisons.

This dashboard is included as supporting analysis and is not intended as a standalone case study.


## Author
Andres Felipe Duque
Data Analyst -  Portfolio Project
