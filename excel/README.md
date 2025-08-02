# Excel Analysis Process

## Data Cleaning Steps
1. Imported raw CSV data
2. Removed blank rows and duplicates
3. Fixed data types:
   - OrderDate formatted as date
   - UnitPrice and TotalPrice as currency
4. Created additional columns:
   - Month = TEXT(OrderDate, "mmm")
   - Quarter = "Q" & ROUNDUP(MONTH(OrderDate)/3, 0)
   - Year = YEAR(OrderDate)

## Analysis Performed
1. Pivot Tables:
   - Sales by Category
   - Sales by Country
   - Monthly/Quarterly Sales Trends
   - Top 10 Products by Revenue
   - Payment Method Analysis

2. Charts Created:
   - Line chart for sales trends
   - Bar chart for top products
   - Pie chart for category breakdown
   - Map chart for country sales

## Dashboard Elements
- KPI Cards: Total Revenue, Orders, Average Order Value
- Sales Trend Chart
- Top Products Bar Chart
- Category Breakdown
- Geographic Distribution
- Payment Method Analysis