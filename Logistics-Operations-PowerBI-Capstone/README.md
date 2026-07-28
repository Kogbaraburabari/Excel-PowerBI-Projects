# Logistics Operations: Power BI Capstone

**Program:** TS Academy Data Analytics Capstone
**Tool used:** Power BI (Power Query + Data Modeling + DAX + Report Design)

## Objective
Design a full logistics operations data model from 14 raw source tables and build a multi-page
Power BI report covering business performance, driver/route efficiency, fleet operations, and
safety/compliance the kind of end-to-end BI build a trucking/freight company would use to run
its business.

## Data Model
14 tables connected in a relational star-schema style model:

| Table | Primary Key | Connects To |
|---|---|---|
| Customers | `customer_id` | Loads |
| Trucks | `truck_id` | Trips, Fuel Purchases, Maintenance Records, Safety Incidents, Truck Utilization Metrics |
| Trailers | `trailer_id` | Trips |
| Drivers | `driver_id` | Trips, Fuel Purchases, Safety Incidents, Driver Monthly Metrics |
| Facilities | `facility_id` | Delivery Events |
| Routes | `route_id` | Loads |
| Loads | `load_id` | Customers, Routes, Trips |
| Trips | `trip_id` | Loads, Drivers, Trucks, Trailers, Fuel Purchases, Delivery Events, Safety Incidents |
| Fuel Purchases | `fuel_purchase_id` | Trips, Trucks, Drivers |
| Maintenance Records | `maintenance_id` | Trucks |
| Delivery Events | `event_id` | Loads, Trips, Facilities |
| Safety Incidents | `incident_id` | Trips, Trucks, Drivers |
| Driver Monthly Metrics | `driver_id` + `month` (composite) | Drivers (aggregated) |
| Truck Utilization Metrics | `truck_id` + `month` (composite) | Trucks (aggregated) |

## Data Cleaning (Power Query)
- **Missing foreign keys** in `trips`, `fuel_purchases`, and `safety_incidents` (unassigned
  driver/truck/trailer on a small share of records) — filled with `"Unassigned"` / `"Unknown"`
  rather than left blank, so these records remain queryable and visible in aggregations instead
  of silently disappearing from joins
- **Missing `termination_date`** in `drivers` left as blank by design, since this correctly
  represents currently active drivers rather than a data quality issue
- Verified referential integrity across the model (no orphaned foreign keys between Loads ↔
  Customers/Routes, Trips ↔ Loads/Drivers/Trucks, etc.) and confirmed no duplicate records or
  primary key collisions across any of the 14 tables

## DAX Measures
Custom measures built to power the report's KPI cards and visuals, including:
`Total Loads Revenue` · `Total Profit` · `Avg Revenue Per Load` · `Profit Margin` ·
`On Time Deliveries` · `Total Active Drivers` · `Total Active Trucks` · `Average MPG` ·
`Preventable Incidents %` · `Driver Liability Rate`

## Report Structure (5 pages)

**Business Performance** Total Loads Revenue, Total Profit, Avg Revenue per Load, Profit
Margin, On-Time Deliveries, Total Customers, plus breakdowns of earnings by customer type,
freight type, route, monthly trend, and top customers.

**Driver & Routes** Revenue, profit, accessorial charges, fuel surcharge, average MPG, and
active driver count, plus driver earnings, on-time delivery rates, most efficient drivers, and
actual vs. typical distance comparisons.

**Fleet & Operations** Maintenance and fuel cost, downtime hours, utilization rate, and active
truck count, plus utilization by truck make, downtime trend, MPG by make, and maintenance cost
breakdown.

**Safety & Compliance** Claim amount, vehicle/cargo damage cost, preventable incident %, and
driver liability rate, plus incident trend over time and an incident map by state.

**Truck Information** Maintenance cost and MPG trends per truck, plus a full truck details table.

## Key Findings
*(calculated directly from the source data)*

- **Total revenue:** $262.5M across 85,410 completed loads (avg. $3,073.71 per load)
- **On-time delivery rate:** 55.7% a clear area for operational improvement
- **Fleet & driver utilization:** 92 of 120 trucks (77%) and 124 of 150 drivers (83%) are currently active; average truck utilization rate sits at 83%
- **Fuel and maintenance costs:** $95.6M in fuel purchases and $5.7M in maintenance costs recorded across the fleet
- **Top customer:** First Group ($9.14M in revenue), followed by First Logistics ($6.38M)
- **Revenue by contract type:** Contract freight leads ($98.8M), followed closely by Spot ($82.9M) and Dedicated ($80.9M) a fairly balanced mix across booking types
- **Fleet composition:** Peterbilt is the most common truck make (24 trucks), followed by Freightliner (22) and Mack (21)
- **Safety:** 170 recorded incidents totaling $2.65M in claims; 37.6% were flagged as preventable and 31.8% as at-fault both areas worth targeted safety interventions

## Files in this project
- [`Logistic Operation Dataset.pbix`](./Logistic%20Operation%20Dataset.pbix) — full Power BI file (raw data, Power Query cleaning steps, data model, DAX measures, and report)

## Skills applied
`Power BI` `Power Query (ETL)` `Data Modeling` `DAX` `Relational Schema Design` `Dashboard Design` `Business Insight Reporting`
