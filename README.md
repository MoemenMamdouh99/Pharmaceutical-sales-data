# Pharmaceutical Sales Performance Analysis

## Project Overview

This project analyzes pharmaceutical sales data to evaluate distributor performance, product performance, and sales team effectiveness. The objective was to transform raw sales data into actionable business insights through data cleaning, SQL analysis, and interactive Power BI dashboards.

The project follows a complete analytics workflow:

1. Data Cleaning and Validation using SQL Server
2. Data Modeling and Analysis
3. KPI Development
4. Interactive Dashboard Creation in Power BI
5. Business Insights and Recommendations

---

## Business Problem

Management needed a reliable way to monitor sales performance across:

* Distributors
* Pharmaceutical products
* Area Managers
* District Managers
* Medical Representatives
* Geographic sales zones

The raw dataset contained data quality issues, including incorrect revenue calculations and date formatting problems, making it unsuitable for direct analysis.

---

## Dataset Information

The dataset contains pharmaceutical sales transactions covering multiple years and includes:

* Sales Date
* Distributor Name
* Product Name
* Area Manager
* District Manager
* Medical Representative
* Product Line
* Revenue
* Quantity Sold
* Sales Zone
* Unit Price

---

## Tools & Technologies

* SQL Server
* Power BI
* DAX
* Microsoft Excel

---

## Data Cleaning Process (SQL)

A separate working table was created to preserve the original dataset.

### Data Quality Improvements

#### Revenue Correction

Some records contained missing or incorrect revenue values.

Revenue was recalculated using:

```sql
Revenue = Quantity_Sold * Price
```

#### Date Conversion

The sales date column was originally stored as text.

Using TRY_CONVERT(), dates were safely transformed into SQL DATE format before altering the column datatype.

#### Duplicate Validation

A duplicate detection process was implemented using:

```sql
ROW_NUMBER()
```

No duplicate records were found after validation.

#### Data Verification

Additional validation confirmed that revenue calculations were inconsistent across the dataset, so all records were recalculated to ensure consistency.

---

## SQL Views Created

### Distributor Analysis

```sql
vw_distributer_analysis
```

Used to evaluate:

* Revenue by distributor
* Quantity sold by distributor
* Sales trends over time

### Product Analysis

```sql
vw_product_analysis
```

Used to analyze:

* Product revenue
* Product quantity sold
* Product performance trends

### Team Performance Analysis

```sql
vw_teams_performance
```

Used to evaluate:

* Area Manager performance
* District Manager performance
* Medical Representative performance
* Zone contribution

---

## Power BI Dashboard

The dashboard consists of three analytical pages.

### 1. Distributor Analysis

Focuses on:

* Revenue by Distributor
* Quantity Sold by Distributor
* Distributor Contribution %
* Sales Trend Analysis

Visuals Used:

* Bar Chart
* Donut Chart
* KPI Cards
* Slicers

---

### 2. Product Analysis

Focuses on:

* Best Selling Products
* Highest Revenue Products
* Product Trends Over Time
* Product KPI Tracking

Visuals Used:

* Bar Charts
* Line Charts
* KPI Gauges
* Tables
* Slicers

---

### 3. Team Performance

Focuses on:

* Area Manager Performance
* District Manager Performance
* Medical Representative Performance
* Zone Contribution Analysis

Visuals Used:

* Bar Charts
* Decomposition Tree
* KPI Cards
* Tables
* Slicers

---

## Key Business Questions Answered

### Distributor Performance

* Which distributors generate the highest revenue?
* Which distributors sell the largest quantities?

### Product Performance

* Which products generate the most revenue?
* Which products are the strongest volume drivers?
* Are there seasonal product trends?

### Sales Team Performance

* Which Medical Representatives are top performers?
* Which Area Managers lead the highest-performing territories?
* Which District Managers contribute the most revenue?

### Regional Performance

* Which sales zones outperform others?
* How does Alexandria compare across territories?

---

## Skills Demonstrated

### SQL

* Data Cleaning
* Data Validation
* Data Transformation
* Views
* CTEs
* Window Functions
* Data Quality Management

### Power BI

* Data Modeling
* DAX Measures
* KPI Development
* Interactive Dashboards
* Drill-Down Analysis
* Decomposition Tree Analysis

### Business Analysis

* Sales Performance Analysis
* Revenue Analysis
* Product Analytics
* Team Performance Evaluation
* Territory Performance Assessment

---

## Business Impact

The solution provides management with a centralized dashboard that enables:

* Faster decision-making
* Identification of top-performing products
* Evaluation of sales team productivity
* Monitoring distributor effectiveness
* Tracking regional sales performance
---
## Business Recommendation

* We can hire more Medical Reps in Hany Wadie's team. Each representative in his team generates an average of 736.41K EGP, and they generate a total revenue of 10.310M EGP
  which can be easily increased 2 times if we hire 14 more Medical Reps, or we move 14 Reps from team Samir Habib to his district.
---
## Data Limitation

* The data provided from 2015 to 2021 which is not complete in 2021
* Change in prices from 2021 to 2026, so we can ask for more data and add to the database, which is connected to Power BI
---
## Author

**Moemen El Khouly**

Data Analyst specializing in SQL, Power BI, and Business Intelligence solutions. Passionate about transforming business data into actionable insights and data-driven decisions.
