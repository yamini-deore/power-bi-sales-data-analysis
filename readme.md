# Sales Data Analysis Dashboard using Power BI

## Project Description

This project focuses on analyzing sales data and transforming raw business information into meaningful insights using Power BI. The objective was to design an end-to-end Business Intelligence solution that enables stakeholders to monitor sales performance, profitability, discount impact, and customer purchasing trends through an interactive dashboard.

The project involved data extraction, data cleaning, transformation, data modeling, DAX calculations, and dashboard development. A star schema data model was implemented to ensure efficient reporting and analysis.

---

# Business Requirements

The business required a dashboard capable of:

* Tracking Total Sales, Net Sales, Profit, and Quantity Sold.
* Monitoring sales performance across different cities.
* Analyzing the impact of promotional discounts on revenue.
* Identifying sales trends over time.
* Providing interactive filtering capabilities for business users.
* Delivering key performance indicators (KPIs) through a centralized reporting solution.

---

# Project Implementation

## Step 1: Data Loading

Imported multiple datasets into Power BI Desktop, including:

* Sales Data
* Product Data
* Customer Data
* Promotion Data

The primary sales transaction table was renamed as **Fact Table** to follow data modeling best practices.

---

## Step 2: Data Profiling and Quality Assessment

Performed data profiling using Power Query Editor by enabling:

**Column Profiling Based on Entire Dataset**

This helped identify:

* Null values
* Incorrect data types
* Duplicate records
* Data quality issues

Each table was reviewed individually before transformation.

---

## Step 3: Data Transformation

### Customer ID Standardization

The Customer ID column was converted to Text data type because it serves as a business identifier and is not used in mathematical calculations.

### Promotion Data Transformation

Promotion values contained percentage-based discounts.

Example:

* 10% Discount
* 20% Discount
* 30% Discount

Using Conditional Columns in Power Query, discount percentages were extracted into a separate numeric column for further calculations.

### Null Value Handling

Null values in the Discount Percentage column were replaced with 0 to ensure accurate calculations and prevent reporting errors.

### Fact Table Cleanup

The Fact Table contained:

* Unnecessary columns
* Duplicate columns
* Columns with 100% null values

These columns were removed to improve model performance and maintain data quality.

---

## Step 4: Business Calculations

### Total Sales Calculation

The existing Total Sales column contained only null values.

A new calculated column was created using:

Total Sales = Units Sold × Price Per Unit

This generated the sales amount for every transaction.

### Discount Value Calculation

Calculated the discount amount using:

Discount Value = Total Sales × Discount Percentage ÷ 100

### Net Sales Calculation

Calculated the actual revenue after discount:

Net Sales = Total Sales − Discount Value

### Profit Calculation

Calculated profit using:

Profit = Net Sales − Total Cost

The Profit column was assigned the Decimal Number data type for accurate financial reporting.

---

## Step 5: Data Modeling

A Star Schema data model was designed consisting of:

### Fact Table

* Sales Transactions

### Dimension Tables

* Product Table
* Customer Table
* Promotion Table
* Date Table

Relationships were established using matching keys and appropriate cardinality.

Relationship types used:

* One-to-Many
* Many-to-One

All relationship columns were validated to ensure matching data types.

---

## Step 6: Date Table Creation

Two Date Tables were created using DAX:

Date Table 1 = CALENDARAUTO()

Date Table 2 = CALENDARAUTO()

These tables were used for date analysis and inactive relationship scenarios.

---

## Step 7: DAX Measures

Developed advanced DAX measures using:

* CALCULATE
* SUM
* ALL
* USERELATIONSHIP

### Total Net Sales Measure

Calculated Net Sales while activating an inactive relationship with the Date Table.

### Total Profit Measure

Calculated overall Profit while maintaining proper date context.

### Quantity Sold Measure

Calculated the total number of units sold across all transactions.

---

## Step 8: Dashboard Development

Designed an interactive dashboard containing:

### KPI Cards

* Total Sales
* Net Sales
* Total Profit
* Quantity Sold

### Visualizations

* Sales by City
* Profit by City
* Monthly Sales Trends
* Product Performance Analysis
* Discount Impact Analysis

### Interactive Filters

* Date
* City
* Product
* Promotion Type

---

# Key Insights

The dashboard enabled business users to:

* Identify top-performing cities.
* Monitor sales and profit trends.
* Measure the impact of discounts on revenue.
* Evaluate product performance.
* Make data-driven business decisions using real-time insights.

---

# Skills Demonstrated

* Power BI
* Power Query Editor
* Data Cleaning
* Data Transformation
* Data Modeling
* Star Schema Design
* DAX
* Business Intelligence Reporting
* Dashboard Development
* Data Visualization

---

# Project Outcome

Successfully developed an end-to-end Sales Analytics Dashboard that transformed raw transactional data into actionable business insights. The solution improved reporting efficiency and provided stakeholders with a centralized platform for monitoring sales performance and profitability.

## Author

Yamini Deore

Power BI Developer | Data Analyst
