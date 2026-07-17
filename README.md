# Customer Response Analysis for Marketing Campaign

**Tools:** Microsoft Excel (PivotTables, XLOOKUP, AVERAGEIF, SUMPRODUCT, COUNTIFS, Slicers)

**Dataset:** [Marketing Campaign Dataset - Kaggle](https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign)

**Records:** 2,236 customers after cleaning


## Project Overview

This project analyzes customer behavior and marketing campaign performance for a retail company.
The goal is to identify which customers are most likely to respond to a campaign offer - and what characteristics define them.
The analysis covers customer profiling, campaign effectiveness, spending patterns, and purchase channel preferences.


## Workbook Structure

| Sheet | Description |
|---|---|
| Raw Data | Original dataset - untouched source |
| Data Cleaning | Removed outliers, filled missing values, created derived columns |
| Typical Client | Customer demographic and spending profile |
| Campaign Analysis | Response rates by campaign, income, age group, and education |
| Channel Analysis | Purchase behavior across store, web, catalog, and deals channels |
| Dashboard | Interactive summary dashboard with KPI cards and slicers |


## Data Cleaning Steps

- Removed 2 constant columns (Z_CostContact, Z_Revenue) with no analytical value
- Filled 24 missing Income values with the median
- Removed 3 age outliers (customers born before 1910)
- Removed 1 income outlier (€666,666)
- Standardized Marital_Status - recategorized non-standard values (Absurd, YOLO, Alone)
- Created derived columns: Age, Age_Group, Income_Clean, Income_Segment, Income_Label, TotalSpend, TotalCampaigns, HasChildren
- Applied Data Bars to Income_Clean column to visualize income distribution at a glance
- Highlighted Top 30 customers by TotalSpend using conditional formatting (green fill)

**Final clean dataset: 2,236 rows**


## Key Excel Functions Used

| Function | Purpose |
|---|---|
| AVERAGEIF | Avg. spend and income by response group |
| COUNTIFS | Customer count by multiple segment criteria |
| XLOOKUP | Income label lookup from reference table |
| SUMPRODUCT | Weighted average spend for loyal customers |
| PERCENTILE | Dynamic income segmentation thresholds |
| IFS | Age group and income segment classification |
| PivotTables + Slicers | Interactive dashboard filtering |


## Key Findings

- **14.9%** overall response rate on the final campaign
- Responders spend nearly **2x more** than non-responders (€987 vs €539)
- **Campaign 2 dramatically underperformed** - 1.3% response rate vs. 7% average
- Among high-income customers who responded, **77% are Seniors (56+)** - the priority audience for future campaigns
- **Physical store** is the #1 purchase channel across all segments
- Seniors unexpectedly **lead in online purchases** (avg. 4.47 vs. 3.65 for Young customers)
- **Wine dominates spending** - nearly 50% of total product expenditure


## Business Recommendations

1. **Focus future campaigns on high-income Senior customers** - they respond most and spend most
2. **Conduct a post-campaign review of Campaign 2** to identify weaknesses in targeting strategy, offer design, and communication channels before launching similar initiatives
3. **Expand digital marketing efforts toward Senior customers**, whose online purchasing activity exceeds expectations and demonstrates strong engagement potential
4. **Use purchase history as a predictor** - customers who accepted previous campaigns are significantly more likely to respond again
