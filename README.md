
### Retail Sales Performance Dashboard
### Dashboard Link: [Insert Power BI Service Link Here]
### Problem Statement
This retail sales dashboard provides comprehensive insights into the performance of a retail store specializing in Food and Drinks product lines. The dashboard enables data-driven decision making by tracking key metrics, identifying trends, and highlighting areas for improvement across sales, products, customers, and regions.

### Key challenges addressed:

Monitoring sales evolution and growth percentages

Tracking revenue against targets

Identifying best and worst performing products

Analyzing customer coverage by region

Understanding average purchase values

Simulating pricing scenarios

Forecasting future sales

Applying Pareto analysis to customer sales

### Implementation Steps
Data Preparation
Loaded retail sales data into Power BI Desktop from [data source]

### Performed data quality checks in Power Query Editor:

Verified column distributions

Checked for null/missing values

Validated data types

Created date dimension table for time intelligence calculations

Established relationships between tables

### Measures Creation
### Developed key DAX measures including:

DAX
Sales Growth % =   
VAR CurrentSales = SUM(Sales[Amount])  
VAR PreviousSales = CALCULATE(SUM(Sales[Amount]), PREVIOUSMONTH('Date'[Date]))  
RETURN  
DIVIDE((CurrentSales - PreviousSales), PreviousSales, 0)  

Revenue vs Target =   
DIVIDE(SUM(Sales[Amount]), SUM(Targets[TargetAmount]), 0)  

Average Ticket Size =   
DIVIDE(SUM(Sales[Amount]), DISTINCTCOUNT(Sales[TransactionID]), 0)  

Pareto % =   
VAR TotalSales = CALCULATE(SUM(Sales[Amount]), ALL(Sales))  
RETURN  
DIVIDE(SUM(Sales[Amount]), TotalSales, 0)  
### Visualizations
### Sales Performance

Line chart showing monthly sales evolution

Combo chart comparing actual sales vs targets

Card visuals displaying YTD sales and growth percentage

Product Analysis

Matrix of products by sales volume

Bar charts for top/bottom 10 products

Trend line of unsold products by month

Customer Coverage

Map visualization showing sales by region

Donut chart of customer distribution

Table of customer penetration metrics

Pricing Simulation

What-if parameter for price adjustments

Scatter plot showing price elasticity impact

Card showing projected revenue change

Forecasting

Time series forecast for 2025 sales

Confidence interval bands

Pareto Analysis

Cumulative percentage chart of customers by sales

Table highlighting top 20% customers driving 80% sales

Dashboard Design
Applied cohesive color theme and branding

Added interactive slicers for:

Product category

Time period

Region

Incorporated tooltips for detailed insights

Added dynamic titles and KPI indicators

Implemented bookmarks for different analysis views

### Key Insights
### Sales Performance
YTD Sales: $4.2M (87% of target)

Monthly growth rate: 5.3% (average)

Q3 consistently strongest quarter (28% of annual sales)

### Product Analysis
### Top Performers

Premium Coffee Blend - $420K

Organic Snack Box - $380K

Craft Beer Selection - $350K

Underperformers

Specialty Tea Collection - $45K

Artisan Crackers - $52K

Imported Olive Oil - $68K

12% of SKUs account for 0 sales last quarter

### Customer Insights
Northeast region generates 42% of total sales

Top 18% customers drive 82% revenue (Pareto principle)

Average ticket size: $85 (up from $78 YoY)

### Pricing Simulation
5% price increase projected to boost revenue by 3.2% with minimal volume impact

10% discount would require 15% volume increase to maintain revenue

### 2025 Forecast
Predicted annual sales: $5.1M (±8%)

Expected growth rate: 9-12% based on current trends

### Recommendations
Focus marketing efforts on high-value customer segments

Review product assortment to eliminate non-performing SKUs

Implement targeted promotions in underperforming regions

Consider moderate price adjustments on elastic products

Increase inventory for top sellers ahead of peak seasons

[Prueba Power BI Proyecto.pdf](https://github.com/user-attachments/files/20537416/Prueba.Power.BI.Proyecto.pdf)
