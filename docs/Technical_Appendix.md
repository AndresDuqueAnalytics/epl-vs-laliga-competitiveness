Technical Appendix - Methods & implementation

Case Study: Competitive Balance Assessment (EPL vs La Liga, 2023/24)

Purpose of This Appendix

This appendix outlines the technical workflow, data modeling decisions, and logic used in this analysis. It is intended for technical reviewers to verify the integrity of the calculations and the reproducibility of the findings.

Methodology Note
This analysis was developed as a technical portfolio project to demonstrate end-to-end data handling. My goal was to apply industry-standard ETL and DAX patterns to a complex, real-world comparison. 


Tools Used
Microsoft Excel: initial inspection, season filtering, schema alignment, and simple calculated fields
SQLite: data validation, integrity checks, table creation, and aggregation
Power BI Desktop:  data modeling, DAX calculations, and visualization

Each tool was selected for a specific role in the workflow rather than as a standalone solution.

Data Model Overview

Grain
Match-level data: one row per match (home vs away)
Team-level summaries:  one row per team per league (derived)

Core Tables
Fact_MatchTeam_23_24
Unified match-level fact table combining EPL and La Liga using a standardized schema.
Standings_23_24
Team-level table containing final league position and total points.
AwayPoints_23_24
Team-level table containing total points earned in away matches





Schema Standardization

To enable cross-league comparison, both datasets were aligned to a common schema using the Premier League dataset as the reference. Differences in metric availability were preserved rather than corrected.
Columns missing in one league but present in the other were kept as null.
No imputation or assumed values were introduced
Only metrics available in both datasets were used for direct league-level comparison

This approach prioritized analytical integrity over completeness.


Calculated Fields (Match-Level)

The following derived fields were created using consistent logic across both leagues:
FullTimeResult
Categorical match outcome based on final goals (Home/Draw/Away)
MatchResultNumeric
Numeric representation of points earned by the home team (3/1/0)
GoalDifference
Home goals minus away goals
TotalShots
Sum of home and away shots
ShotEfficiency_Home / ShotEfficiency_Away
Shots on target divided by total shots

These fields support aggregation and distribution-based analysis

SQL Transformations (SQLite)

Unified Fact Table
Both league datasets were combined using UNION ALL to form a single match-level fact table with a league identifier.

Away Points Table
Away points were calculated at the team level to support away-match analysis:
Points assigned based on away match result
Aggregated by league and team
Results table contains one row per team per league

This table was later imported into Power BI and merged with standings data.


Power BI Modeling Decisions

Aggregation Choice (MAX vs Sum)

In visuals where league position was used as a dimension (e.g., points by final position), MAX(TotalPoints)  was used instead of SUM to avoid inflating values when duplicate rows existed in the model.

This choice reflects that:
Each league position corresponds to a single team
The goal is to display the representative value for that rank, not to aggregate performance

Distribution Analysis Without Custom Visuals

Due to environment constraints, custom visuals (e.g, Box & Whisker from AppsSource) were not used. Instead, distribution behavior was approximated using native Power BI visual and percentile-based measures.

Percentile Measures (Away performance)

Percentiles were calculated to describe the distribution of away points across teams within each league:
 25th Percentile (P25)
Median
75th Percentile (P75)
Minimum / Maximum

These measures were used together to approximate box-and-whisker behavior (middle 50%, center, and range)

This approach maintains transparency and reproducibility using native tools

Tier-Based Analysis

Teams were grouped into tiers (Top / Mid / Bottom) based on final total points to evaluate how competitiveness varies across the league table.
Tier definitions were applied consistently across both leagues
Aggregations focused on:
Total points
Away points
Distribution ranges
This tiering was used to move beyond averages and examine structural differences in competitiveness.

Metric Limitations
Advanced metrics such as xG, xPTS, and PPDA were available onlyfor La Liga.
To maintain a fair comparison, I utilized Shot Efficiency as a technical proxy for both leagues
Scope: This project focuses on the 23/24 season as a representative snapshot of modern league parity.

All limitations are explicitly acknowledged in the main analysis

Scope Reminder
This appendix documents how the analysis was built. Interpretation, conclusions, and strategic implications are addressed in the main case study document and Executive Summary.



