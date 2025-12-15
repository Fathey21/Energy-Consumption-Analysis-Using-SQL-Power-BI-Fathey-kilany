# Energy Consumption Analytics – BI Mini Project

## Business Problem
A national energy agency wants to analyze household electricity consumption
to identify high-demand regions, peak usage times, and estimate energy costs
to support efficiency and planning decisions.

## Data Sources
### Source 1 – CSV
Household Power Consumption Dataset  
Link: https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption

### Source 2 – SQL Database
Microsoft SQL Server database containing:
- Households
- Regions
- TariffPlans

## ETL Process (Power Query)
The following transformations were applied:
1. Removed duplicate records
2. Replaced missing values ("?") with null
3. Converted Date and Time columns to proper data types
4. Created DateTime column
5. Created calculated Cost column
6. Merged CSV consumption data with SQL household data
7. Created a Date Dimension table

## Data Model
Star Schema was implemented:
- Fact Table: Energy Consumption
- Dimension Tables: Households, Regions, TariffPlans, DateDim

Relationships were created between fact and dimension tables.

## Power BI Dashboard
### KPIs:
- Total Energy Consumption
- Average Household Consumption
- Estimated Energy Cost
- Peak Usage Hour

### Visuals:
- Line Chart: Energy Consumption Over Time
- Bar Chart: Consumption by Region
- Bar Chart: Consumption by Tariff Plan
- Table: Top 10 Households by Consumption
- Slicers: Region, Year, Tariff Plan

## Insights
- Certain regions show significantly higher consumption.
- Peak usage occurs during specific evening hours.
- Residential tariff households contribute the largest share of usage.

## Recommendations
- Encourage energy efficiency programs during peak hours.
- Apply differentiated tariff strategies for high-consumption regions.

## Challenges
- Handling missing values in large datasets.
- Mapping household identifiers across heterogeneous sources.
