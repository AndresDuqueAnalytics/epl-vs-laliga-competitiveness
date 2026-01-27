Competitive Balance Assessment (EPL vs La Liga) — Season 2023/24
Executive Summary: Competitive Balance Assessment (2023/24)
The One-Sentence Answer
The data confirms that the Premier League is structurally more competitive than La Liga, driven by a significantly higher performance floor among mid-tier clubs and a broader distribution of offensive quality.
Key Findings
Structural Parity vs. Tactical Closeness
While La Liga produces a higher proportion of close one-goal matches (68% vs. 55%), this tactical compactness does not translate into season-long balance. The Premier League exhibits superior structural competitiveness, reflected in slightly lower points dispersion and a more equitable distribution of performance across the league table.
Mid-Table Resilience (Primary Differentiator)
The Premier League’s “middle class” (positions 4–15) is 14 points tighter than La Liga’s. This mid-tier strength is most evident in away fixtures, where the EPL maintains a 100% higher performance floor (6 points vs. 3 points), significantly reducing the insulation typically enjoyed by top-tier teams.
Offensive Depth as a Technical Driver
Shot-based analysis reveals that the Premier League contains a broader cluster of teams capable of sustained chance creation and conversion. In contrast, La Liga exhibits a larger concentration of offensively struggling teams, contributing to a clearer technical and points-based separation between the top and bottom of the table.
Strategic Implications
Broadcast Value
High structural parity and mid-table compression increase sustained uncertainty across the season. This unpredictability—where a wider range of teams can challenge elite clubs—supports stronger global viewership and premium broadcast valuations.
Investment Risk
The Premier League’s higher performance floor reduces the presence of “dead zones” in the league table. For stakeholders, this offers improved downside protection, as fewer clubs are structurally prone to collapse or prolonged non-competitiveness.
League Positioning
The Premier League’s positioning as the “world’s most competitive league” is supported by data. Its competitiveness is structural and deep, while La Liga’s competitiveness is tactical and narrow.
Bottom-Line Conclusion
La Liga excels at producing close individual matches, while the Premier League excels at producing a balanced league. The EPL’s advantage lies in the strength and resilience of its middle tier. By maintaining a higher baseline of quality and offensive depth across all 20 teams, the Premier League creates a more resilient, uncertain, and commercially valuable sporting environment.

ASK STAGE — Business Scenario
Company Context
I am working as a Data Analyst at a global sports analytics and advisory firm that supports football clubs, investors, and league executives with data-driven insights. The firm has been asked to prepare a high-level competitive analysis comparing the Premier League and La Liga.
Stakeholder
The primary stakeholder is the President of an international football investment group evaluating strategic opportunities within European football, including:
Expanding club ownership across European leagues
Investing in broadcast rights and commercial partnerships
Allocating capital toward leagues with higher competitive balance and global appeal
The stakeholder believes the Premier League is more competitive than La Liga, but this belief is perception-based rather than data-driven. My manager has asked me to validate or challenge this assumption using objective performance and operational data.


Business Problem
The stakeholder seeks a data-supported explanation for why the Premier League is widely considered more competitive than La Liga. The objective is not to determine which team is best or which team wins the league, but rather to assess whether the data supports this perception and in what measurable ways.
Core Business Question
Using match-level performance and efficiency data from the 2023/24 season, what indicators suggest that the Premier League is more competitive than La Liga?
Supporting Analytical Questions
Match outcome balance
Are matches closer in scoreline? Is average goal difference smaller?
Points distribution
Are points more evenly distributed across teams? Do mid-table and lower-table teams take more points from top teams?
Performance efficiency
Are shot efficiency and expected performance metrics evenly spread? Is dominance concentrated among a small group of clubs?
Operational intensity
Do metrics such as PPDA indicate higher pressing intensity? Are teams consistently forced into higher-effort performances?
Predictability
Are match outcomes harder to predict based on dominance metrics?
Competitiveness is treated as a multi-dimensional concept, encompassing match-level tightness, season-long point distribution, and concentration of dominance under both home and away conditions.
Why This Matters to the Stakeholder
If the Premier League demonstrates smaller average goal differences, tighter efficiency margins, and less concentration of dominance, this supports strategic decisions related to:
Broadcast and media rights valuation
Long-term investment confidence
League positioning as a product defined by sustained competitive tension
These outcomes directly influence business strategy rather than fan-driven narratives.

PREPARE STAGE
Data Sources
The analysis uses publicly available datasets from Kaggle:
Premier League: match-level performance data
La Liga: match-level performance and advanced metrics data
Both datasets contain structured observations suitable for analytical and educational use. The analysis is limited to the 2023/24 season to ensure comparability.
Data Organization
Each dataset was provided as a CSV file with one row per match. While the datasets shared a similar analytical grain, they differed in column naming conventions, metric availability, schema structure, and inclusion of advanced metrics.
To prepare the data for comparison, both datasets were reorganized into a unified schema using the Premier League structure as the reference model.
Metric Availability and Limitations
La Liga includes advanced metrics such as expected goals (xG), expected points (xPTS), and PPDA, while the Premier League dataset does not. Conversely, the Premier League dataset includes disciplinary and halftime metrics not present in La Liga.
These differences were preserved rather than imputed to ensure transparency, analytical integrity, and defensible comparisons. Only metrics available in both datasets were used for direct league-level comparison.
Data Credibility and Bias Considerations
Both datasets were assessed using ROCCC criteria and reviewed for potential sources of bias, including differences in data collection methodology and metric definitions. All limitations were documented and accounted for in the analysis design.






PROCESS STAGE — Data Cleaning & Transformation
The objective of the process stage was to transform raw datasets into a clean, consistent, and analysis-ready structure suitable for cross-league comparison.
Tools Used
Microsoft Excel: initial inspection, filtering, schema alignment, and calculated fields
SQLite: integrity checks, validation, and aggregation
Power BI Desktop: data modeling, DAX calculations, and visualization
Key Cleaning and Transformation Steps
Filtered both datasets to the 2023/24 season
Standardized column names and ordering
Preserved missing metrics as NULL values
Created derived fields including goal difference, match result values, total shots, and shot efficiency
Validated data types and logical consistency
Combined datasets into a unified fact table using UNION ALL
All steps were documented to ensure reproducibility and transparency.

ANALYZE STAGE — Competitiveness Assessment
The analysis evaluated competitiveness across multiple dimensions, focusing on distribution, variance, and resistance rather than averages or elite dominance.
Match Outcome Tightness
La Liga exhibited lower average absolute goal difference and a higher proportion of close matches, indicating tighter match-level outcomes.
Points Distribution (Home Matches)
While average home points per team were similar across leagues, the Premier League showed slightly tighter point distribution across the season, suggesting stronger underdog resistance.
Away Match Performance
Away performance revealed greater structural separation in La Liga, where success was more concentrated among top teams. In contrast, the Premier League demonstrated more evenly distributed away success.
Tier-Based and Structural Analysis
Top-tier teams performed similarly across leagues, but mid-tier Premier League teams accumulated more points and performed better away from home. This pattern suggests that the Premier League’s competitiveness is driven by mid-tier strength rather than elite dominance.
Key Interpretation
Match-level closeness does not necessarily equate to season-level competitiveness. La Liga’s tactical compactness coexists with structural separation, while the Premier League exhibits sustained uncertainty driven by depth and resilience across the league table.

SHARE STAGE — Communicating Insights
Insights were communicated through an interactive Power BI dashboard designed for executive consumption. Visuals were selected to minimize cognitive load while clearly mapping to stakeholder questions.
Four primary visuals were used to illustrate points distribution, away-match stress testing, tactical versus structural competitiveness, and offensive depth. Data limitations were explicitly acknowledged to maintain credibility.
The dashboard supports strategic discussion rather than operational monitoring, enabling stakeholders to quickly understand where and why competitive differences emerge.

ACT STAGE — Strategic Implications & Recommended Next Steps
Broadcast & Media Strategy
The Premier League’s structural balance supports higher broadcast valuations, stronger demand for non-marquee fixtures, and sustained global engagement.
Club Ownership & Capital Allocation
Mid-tier resilience in the Premier League suggests greater upside and reduced downside risk for club investment compared to more concentrated league structures.
League Positioning
The Premier League’s competitive advantage is structural and deep, aligning closely with long-term commercial and strategic objectives.
Recommended Analytical Extensions
Multi-season analysis
Financial context integration
Fixture difficulty normalization
Volatility and stability metrics
Final ACT Perspective
The Premier League’s competitiveness is rooted in depth, resilience, and systemic balance. For stakeholders prioritizing sustainable value and long-term engagement, these characteristics materially enhance the league’s strategic appeal.
