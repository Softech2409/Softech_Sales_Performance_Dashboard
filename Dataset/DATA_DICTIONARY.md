# Power BI Sales Portfolio Dataset (Synthetic, Realistic)

This dataset is synthetic (no real customer data) but designed to behave like real enterprise sales data.
It supports a star schema model and common Power BI features (time intelligence, drill-through, etc.).

## Tables
- FactSales (25,000 rows): transactional sales lines
- DimDate (2023-01-01 to 2025-12-31): calendar table
- DimProduct (220 products): includes Brand/Category/SubCategory and UnitPrice/UnitCost
- DimCustomer (1,200 customers): includes Segment/City/Country
- DimRegion (20 regions): includes MacroRegion for rollups

## Key Columns
FactSales:
- OrderID: unique order line identifier
- OrderDate: date of order
- ProductID, CustomerID, RegionID: foreign keys to dimensions
- Quantity: units sold
- DiscountPct: discount applied (0 to 0.25)
- SalesAmount: net sales after discount (Quantity * UnitPrice * (1-DiscountPct) + noise)
- CostAmount: cost of goods sold (Quantity * UnitCost + noise)

DimDate:
- Date, Year, Month, MonthNumber, Quarter, Day, Weekday, IsWeekend


## Targets (added)
- TargetsOverall_Monthly: monthly targets for the whole business
- TargetsByCategory_Monthly: monthly targets per product Category

Columns:
- MonthStart: first day of the month (date)
- YearMonth: month key (YYYY-MM) recommended for relationships
- TargetRevenue, TargetProfit, TargetMarginPct

Modeling tip:
Create DimDate[YearMonth] in Power BI and relate it to Targets[YearMonth] (many-to-one).
