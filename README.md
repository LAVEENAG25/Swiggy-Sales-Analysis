# Swiggy Sales Analysis (SQL Data Warehouse Project)

## Project Overview
This project analyzes Swiggy food delivery data using SQL-based data cleaning, dimensional modeling, and business intelligence reporting.

The objective is to transform raw transactional food delivery data into a clean and analytics-ready data warehouse using a Star Schema and generate actionable business insights through KPIs and analytical queries.

---

## Dataset Information

The dataset contains approximately **197,430 food delivery records** with the following attributes:

- State
- City
- Order Date
- Restaurant Name
- Location
- Category
- Dish Name
- Price (INR)
- Rating
- Rating Count

---

## Business Requirements

### 1. Data Cleaning & Validation

Performed the following quality checks:

- Null value detection
- Blank/empty string validation
- Duplicate record identification
- Duplicate removal using ROW_NUMBER()

Validated columns:

- State
- City
- Order_Date
- Restaurant_Name
- Location
- Category
- Dish_Name
- Price_INR
- Rating
- Rating_Count

---

## Data Warehouse Design

### Star Schema

Dimension Tables:

#### dim_date
- Date_ID
- Full_Date
- Year
- Month
- Month_Name
- Quarter
- Day
- Week

#### dim_location
- Location_ID
- State
- City
- Location

#### dim_restaurant
- Restaurant_ID
- Restaurant_Name

#### dim_category
- Category_ID
- Category

#### dim_dish
- Dish_ID
- Dish_Name

### Fact Table

#### fact_swiggy_orders

Measures:
- Price_INR
- Rating
- Rating_Count

Foreign Keys:
- Date_ID
- Location_ID
- Restaurant_ID
- Category_ID
- Dish_ID

---

## ETL Process

### Data Validation
- Null checks
- Blank value checks
- Duplicate detection
- Duplicate removal

### Dimension Loading
- Load distinct values into dimension tables
- Generate surrogate keys using IDENTITY columns

### Fact Loading
- Resolve all dimension keys
- Populate fact_swiggy_orders

---

## KPIs Developed

### Basic KPIs

1. Total Orders
2. Total Revenue (INR Million)
3. Average Dish Price
4. Average Rating

---

## Business Analysis

### Date-Based Analysis

- Monthly order trends
- Quarterly order trends
- Year-over-year growth
- Day-of-week ordering patterns

### Location-Based Analysis

- Top 10 cities by order volume
- State-wise revenue contribution

### Restaurant & Food Analysis

- Top 10 restaurants by orders
- Most popular food categories
- Most ordered dishes
- Cuisine performance by:
  - Orders
  - Average Rating

### Customer Spending Insights

Order distribution by spending range:

- Under ₹100
- ₹100–199
- ₹200–299
- ₹300–499
- ₹500+

### Ratings Analysis

- Rating distribution from 1 to 5

---

## Technologies Used

- SQL Server
- T-SQL
- Star Schema Modeling
- Data Warehousing
- ETL
- Business Intelligence Concepts
- Microsoft Excel / CSV

---

## Project Structure

```text
.
├── Business Requirements.docx
├── SQLQuery1.sql
├── Swiggy_Data.csv
├── swiggy_data.xlsx
└── README.md
```

---

## Key Learning Outcomes

- Data Cleaning using SQL
- Duplicate Handling with Window Functions
- Dimensional Modeling
- Star Schema Design
- Fact and Dimension Table Creation
- ETL Development
- KPI Creation
- Business Performance Analysis

---


## Author

**Laveena Garg**

- GitHub: https://github.com/LAVEENAG25
- LinkedIn: https://www.linkedin.com/in/laveena-garg

