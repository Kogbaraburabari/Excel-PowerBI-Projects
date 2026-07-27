# Project 2: Exploratory Data Analysis (EDA)

**Tool used:** Microsoft Excel

## Objective
Analyze the cleaned sales dataset from Project 1 to uncover trends, patterns, and anomalies —
turning a clean table of numbers into actionable business insights.

## Dataset
- **1,200 sales transactions** (cleaned in Project 1, zero missing/duplicate records)
- Spans multiple products, payment methods, order statuses, and marketing referral sources

## Methods used
- Descriptive statistics (Mean, Median, Mode, Count, Sum) across all numerical variables
- Pivot tables with conditional formatting to compare trends across categories
- Interquartile Range (IQR) method to detect outliers in `Total Price`
- Pearson correlation analysis between `Quantity` and `Total Price`

## Key Findings

**Overview**
- Total transactions: 1,200
- Total revenue: $1,264,761.96
- No missing or duplicate data remaining after cleaning

**Product performance**
- Chair generated the highest revenue ($195,620.11), Printer close behind ($195,612.61)
- Phone generated the lowest revenue ($151,722.39)
- Revenue is fairly evenly spread across all 7 product categories — a balanced portfolio, no over-reliance on one product

**Payment methods**
- Credit Card led ($263,847.63), Online close behind ($262,442.94), Debit Card lowest ($232,361.18)
- Fairly balanced across methods, though "Online" may need clearer categorization since it describes a channel rather than a distinct payment type

**Order status**
- Cancelled orders had the *highest* associated revenue ($276,396.21) — the most significant finding in the analysis
- This suggests potential revenue loss from inventory shortages, payment failures, or fulfillment delays, and is flagged as a priority area for further investigation

**Referral source**
- Instagram was the top-performing channel ($275,285.45), followed by Email Marketing ($261,808.55)
- The Referral Program underperformed ($226,815.58) and may need optimization

**Outlier detection (IQR method)**
- Q1: $410.52 | Q3: $1,578.47 | IQR: $1,167.96
- Upper bound: $3,330.41 — several transactions exceeded this, likely bulk purchases or VIP customers worth targeting for retention

**Correlation analysis**
- Pearson correlation between Quantity and Total Price: **0.6153** (moderate-to-strong positive)
- Larger order quantities tend to produce higher transaction values, though Unit Price also plays a strong role

## Conclusion
The analysis revealed a balanced product portfolio, strong acquisition performance from Instagram
and Email Marketing, and a critical operational concern — high revenue tied up in cancelled orders —
identified as the top priority for business improvement.

## Skills applied
`Exploratory Data Analysis` `Descriptive Statistics` `Pivot Tables` `Outlier Detection (IQR)` `Correlation Analysis` `Business Insight Reporting`
