# Closing the Power Gap
### Electrification Access Across Sub-Saharan Africa, 1990–2024

An end-to-end data analytics project analyzing the urban–rural electricity access gap across 48 Sub-Saharan African countries, built with Power BI and the World Bank's World Development Indicators (WDI).

**Capstone project — AnalystLab Africa Data Analytics Internship, Week 8**

---

## 🔍 The Question

> How has electricity access evolved across Sub-Saharan Africa since 1990, and which countries still show the widest gap between rural and urban access?

National access figures often hide a sharper divide: what a country's cities enjoy versus what its rural population goes without. This project quantifies that gap, ranks it by country, and tracks it over time.

## 📊 Dashboard Preview

**Widest Gap Countries view** — Angola, Mauritania, and Niger, the three countries with the steepest urban–rural divide
![Widest Gap Countries view](screenshotsdashboard-widest-gap.png)

**Major Economies view** — Kenya, Nigeria, and South Africa, the region's largest economies
![Major Economies view](screenshotsdashboard-major-economies.png)
## 🔑 Key Findings

| Metric (latest reporting year) | Value |
|---|---|
| Regional avg. total electricity access | 58.23% |
| Regional avg. urban–rural access gap | 40.39 pts |
| Year-over-year change (regional) | +2.10 pts |
| Countries covered | 48 |

**Widest current urban–rural gaps:** Mauritania (94.2 pts), Equatorial Guinea (84.2 pts), Angola (76.7 pts), Burkina Faso (75.1 pts), Mozambique (67.5 pts).

Full findings, insights, and recommendations are in the [final report](Closing_the_Power_Gap_Final_Report.pdf).


## 🧹 Data & Methodology

- **Source:** [World Bank World Development Indicators](https://datatopics.worldbank.org/world-development-indicators/) bulk CSV download
- **Indicators:** Access to electricity, % of population (total, rural, urban) — `EG.ELC.ACCS.ZS`, `EG.ELC.ACCS.RU.ZS`, `EG.ELC.ACCS.UR.ZS`
- **Scope:** 48 Sub-Saharan African countries, 1990–2024
- Cleaned from 396,970 raw rows down to a 1,400-row analysis table: reshaped from wide to long format, joined against a country reference table to isolate the correct region, checked for duplicates, and one confirmed data anomaly (Chad's 2024 rural access figure) corrected.
- Full cleaning steps and DAX methodology are documented in Sections 3–4 of the final report.

## 📈 Dashboard Features

- 5 KPI cards (regional access level, gap, YoY change, rolling average, country count)
- Choropleth map of Sub-Saharan Africa shaded by current access gap
- Top 10 countries ranked by widest gap
- Rolling 3-year average trend line, filterable by country
- Rural vs. urban comparison chart
- Country/Year slicers and two bookmark-linked preset views

## 🛠️ Tools Used

- **Power BI Desktop** data modeling, DAX, dashboard design
- **Power Query**  data cleaning and transformation
- **World Bank WDI** source dataset

## 📄 Full Report

See [`Closing_the_Power_Gap_Final_Report.pdf`](Closing_the_Power_Gap_Final_Report.pdf) for the complete write-up: objective, dataset description, cleaning process, methodology, findings, insights, and recommendations.

## 👤 Author

**Burabari Kogbara**
Data Analytics Intern, AnalystLab Africa

---

*This project was completed as the capstone deliverable for the AnalystLab Africa Data Analytics Internship program.*
