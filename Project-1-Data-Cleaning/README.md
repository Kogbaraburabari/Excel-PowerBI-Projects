# Project 1: Data Cleaning & Preparation

**Tool used:** Microsoft Excel

## Objective
Clean a raw sales transactions dataset by identifying and resolving missing values, duplicates,
and formatting inconsistencies — preparing it for exploratory data analysis (EDA).

## Dataset
- **1,200 sales transaction records**
- **14 columns:** Order ID, Date, Customer ID, Product, Quantity, Unit Price, Shipping Address,
  Payment Method, Order Status, Tracking Number, Items In Cart, Coupon Code, Referral Source, Total Price

## Process

**1. Duplicate check**
Checked all records for duplicate entries. Confirmed none were present — no removal needed.

**2. Text consistency**
Reviewed categorical/text fields for spelling inconsistencies and applied `TRIM()` to remove
leading, trailing, and extra spaces, ensuring consistent formatting across text columns.

**3. Formatting fixes**
- Converted the `Date` column from numeric serial format to a proper date format
- Formatted `Unit Price` and `Total Price` as currency for readability and consistency

**4. Column renaming**
Standardized column headers to a consistent naming convention:

| Original | Renamed |
|---|---|
| OrderID | Order ID |
| CustomerID | Customer ID |
| UnitPrice | Unit Price |
| ShippingAddress | Shipping Address |
| PaymentMethod | Payment Method |
| OrderStatus | Order Status |
| TrackingNumber | Tracking Number |
| ItemsInCart | Items In Cart |
| CouponCode | Coupon Code |
| ReferralSource | Referral Source |
| TotalPrice | Total Price |

**5. Missing values**
Found 309 blank entries in `Coupon Code`, representing orders where no coupon was applied.
Replaced blanks with `"None"` to clearly distinguish "no coupon used" from missing/unknown data.

## Result
A clean, consistent, complete dataset — ready for exploratory data analysis. Both the raw and
cleaned versions are included in `Project_1.xlsx` on separate sheets for comparison.

## Skills applied
`Data Cleaning` `Data Validation` `Excel Functions (TRIM)` `Data Standardization` `Documentation`
