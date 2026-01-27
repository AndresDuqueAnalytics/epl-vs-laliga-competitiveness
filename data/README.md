## Data Availability

This project uses publicly available match-level datasets sourced from Kaggle
(Premier League and La Liga, 2023/24 season).

Raw or cleaned CSV files are not included in this repository to:
- respect the original distribution source
- avoid duplicating large files in GitHub
- keep the repository focused on analysis artifacts and documentation

All data preparation steps (season filtering, schema alignment, calculated fields,
null handling, validation) are documented in:
- /docs/Case_Study_Report.md
- /docs/Technical_Appendix.md

Reproducible logic is provided through:
- SQL scripts in /sql
- Power BI model and dashboard in /dashboard
