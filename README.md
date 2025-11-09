# 📊 Financial KPI & Growth Analysis Dashboard
Developed a Power BI executive dashboard leveraging DAX calculations and time intelligence to analyze financial performance across geographies, time periods, and customer segments. Delivered actionable insights on peak profit months, most profitable countries, and high-priority product–segment combinations for strategic decision-making.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

  ## A step-by-step project to build an executive financials dashboard in Power BI.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 🚀 Business Problem Statement

  ### A multinational company is analyzing its financial performance across multiple geographies, time periods, and customer segments. Management requires a comprehensive         executive dashboard to support data-driven decision-making by answering:

  ### - When has the company been most profitable? (Identify peak periods)

  ### - Where is the company performing best? (Profit by country/region)

  ### - Which products and segments should be prioritized? (High-value product–segment combos)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 📂 Dataset

  File Used: [Financial Sample.xlsx] (https://github.com/ankitaanand96/executive_financials_dashboard/blob/main/Executive_Financials.xlsx)

  Contains columns like: Date, Country, Segment, Product, Units Sold, Sales, Profit

  Period: 2013–2014

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Tools & Technologies Used 

- 🗄️ [E-R Diagram](https://github.com/ankitaanand96/executive_financials_dashboard/blob/main/Executive_Financials_Dashboard-5.png)
  
- 📗 Excel  

- 🔄 Power Query

- 📈 Power BI
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🛠️ Data Preparation

  - Units Sold → Converted into whole numbers.

  - Segment → Transformed into uppercase for consistency.

  - Month Name → Renamed to Month.

  - Created a Calendar table using CALENDARAUTO() with extra fields: Year, Month, Month Number, Year-Month.

  - Established a relationship: Financials[Date] → Calendar[Date].

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 📐 DAX Calculations Used

  - Total Sales      = SUM ( Financials[Sales] )
    
  - Total Profit     = SUM ( Financials[Profit] )
    
  - Profit Margin %  = DIVIDE ( [Total Profit], [Total Sales] )
    
  - Calendar = 
ADDCOLUMNS (
    CALENDAR ( DATE(2013,1,1), DATE(2014,12,31) ),
    "Year", YEAR ( [Date] ),
    "Month Number", MONTH ( [Date] ),
    "Month", FORMAT ( [Date], "MMM" ),
    "Year-Month", FORMAT ( [Date], "YYYY-MMM" ))
    
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 📊 Dashboard Visuals

  1. [KPI Cards] (https://github.com/ankitaanand96/executive_financials_dashboard/blob/main/Executive_Financials_Dashboard-1.png)

  - Total Sales

  - Total Profit

  - Profit Margin %

  2. Line Chart — Profit by Month & Year

  - X-axis: Calendar[Month Start]

  - Y-axis: [Total Profit]

  - Legend: Calendar[Year]

  *Shows profitability trends, with peak month/year highlighted.*

  3. Map Chart — Profit by Country

  - Location: Country

  - Color/Bubble: [Total Profit]

  *Tooltip: Region, Total Sales, Profit Margin %*

  4. Clustered Column Chart — Sales by Product & Segment

  - Axis: Product

  - Legend: Segment

  - Value: [Total Sales]

  *Identifies top product–segment combinations to invest in.*

  5. Slicer

  - Calendar[Year]
    
  *slicer to toggle between 2013 and 2014.*

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 📈 Executive Insights

  - **Peak Profit Month: December 2014 (~2.03M).**

  - **Top Performing Region: Europe, followed by North America.**

  - **Product–Segment Priority: Products like VTT and Paseo in Enterprise & Government segments generated consistently high sales and margins.**

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## ✅ Deliverables

  - Power BI Report file: FIRSTNAME_LASTNAME-CAPSTONE-PROJECT.pbix

  - Dashboard screenshot: /images/dashboard.png

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🔑 How to Reproduce

  - Clone/download this repo.

  - Open Power BI Desktop.

  - Load dataset: [Financial Sample.xlsx] (https://github.com/ankitaanand96/executive_financials_dashboard/blob/main/Executive_Financials.xlsx)

  - Create Calendar table and DAX measures.

  - Recreate visuals following README steps.

  - Save final PBIX as per naming convention.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 📌 Learnings

  - Applied data cleaning and transformation.

  - Built a Calendar table for time intelligence.

  - Created DAX measures to calculate KPIs and trends.

  - Designed an executive-ready dashboard with actionable insights.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
