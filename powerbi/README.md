# Power BI Dashboard Development

## Data Preparation
1. Imported cleaned Excel dataset
2. Created date table using DAX:
DateTable = CALENDAR(MIN('Sales Data'[OrderDate]), MAX('Sales Data'[OrderDate]))
3. Established relationships between tables

## DAX Measures Created
Total Revenue = SUM('Sales Data'[TotalPrice])
Total Orders = DISTINCTCOUNT('Sales Data'[OrderID])
Average Order Value = [Total Revenue] / [Total Orders]
YoY Growth = DIVIDE([Total Revenue] - [Total Revenue LY], [Total Revenue LY])
Total Revenue LY = CALCULATE([Total Revenue], SAMEPERIODLASTYEAR('DateTable'[Date]))

## Visualizations
1. KPI Cards:
   - Total Revenue
   - Total Orders
   - Average Order Value
   - YoY Growth

2. Charts:
   - Monthly Revenue Trend (Line Chart)
   - Top 10 Products (Bar Chart)
   - Sales by Category (Donut Chart)
   - Geographic Sales Map
   - Payment Method Distribution

3. Slicers:
   - Date Range
   - Category
   - Country