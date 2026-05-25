# Data Modeler – Power BI Data Modeling Project

## Project Overview

This project focuses on building a normalized relational data model in Power BI using Star Schema concepts.

The main objective of this project was to understand how fact tables and dimension tables work together using relationships, cardinality, and schema design.

The project was completed using:
- Power Query Editor
- Model View
- Matrix Tables

No DAX calculations or charts were used as per project requirements.

---

# What I Did In This Project

## 1. Imported Data

I imported multiple Excel tables into Power BI:
- Sales_Fact
- Returns_Fact
- Customer_Dim
- Product_Dim
- Region_Dim
- Date_Dim

---

# 2. Data Cleaning Using Power Query

In Power Query Editor I performed:
- Removed blank rows
- Corrected data types
- Renamed columns
- Checked empty values
- Cleaned unnecessary data
- Loaded transformed data into the model

---

# 3. Created Relationships

I connected all tables using Primary Keys and Foreign Keys.

Relationships created:

| From | To | Cardinality |
|---|---|---|
| Customer_Dim | Sales_Fact | 1 : Many |
| Product_Dim | Sales_Fact | 1 : Many |
| Region_Dim | Sales_Fact | 1 : Many |
| Date_Dim | Sales_Fact | 1 : Many |
| Sales_Fact | Returns_Fact | 1 : Many |
| Date_Dim | Returns_Fact | Inactive |

I used single-direction cross filtering to avoid ambiguity and improve performance.

---

# 4. Created Star Schema

I used Sales_Fact as the central fact table and connected all dimension tables around it:
- Customer_Dim
- Product_Dim
- Region_Dim
- Date_Dim

This structure forms a Star Schema.

---

# 5. Implemented Snowflake Concept

Returns_Fact was added as an additional related table to demonstrate advanced relationship handling and inactive relationships.

---

# 6. Created Hierarchies

## Date Hierarchy
Year → Quarter → Month → Date

## Region Hierarchy
Country → State → City

## Product Hierarchy
Category → Subcategory → ProductName

Hierarchies help in drill-down analysis and better data organization.

---

# 7. Data Formatting

I applied proper formatting:
- Revenue → Currency
- Quantity → Whole Number
- Discount → Decimal
- Date → Date Format

---

# 8. Model Enhancement

I also:
- Added table descriptions
- Hid foreign key columns from report view
- Arranged tables neatly
- Aligned model symmetrically

---

# 9. Verification Using Matrix Tables

To verify relationship flow and filtering, I created matrix tables for:
- Sales by Product Category and Region
- Return Reasons by Fiscal Year
- Revenue by Customer Segment

This confirmed that all relationships were working correctly.

---

# Concepts Used

## Fact Table
Fact tables store transactional and numerical data.

Examples:
- Revenue
- Quantity
- Discount

Fact tables used:
- Sales_Fact
- Returns_Fact

---

## Dimension Table
Dimension tables store descriptive information.

Examples:
- Customer details
- Product details
- Region details
- Date information

---

## Primary Key
A Primary Key uniquely identifies each row in a table.

Examples:
- CustomerID
- ProductID
- RegionID

---

## Foreign Key
Foreign Keys are used to connect tables together.

Examples:
- CustomerID in Sales_Fact
- ProductID in Sales_Fact

---

## Cardinality

### 1 : Many Relationship
One record in dimension table connects to many records in fact table.

Example:
One customer can make many sales.

Most relationships in this project are 1:M.

---

## Star Schema
A Star Schema is a model where one central fact table connects directly to multiple dimension tables.

Benefits:
- Better performance
- Easy reporting
- Simple relationship structure

---

## Snowflake Schema
Snowflake Schema is an extended version of star schema where additional related tables are connected.

---

## Inactive Relationship
An inactive relationship exists in the model but is not actively used for filtering.

In this project:
- Date_Dim → Returns_Fact was created as inactive.

---

# Tools Used

- Microsoft Power BI Desktop
- Power Query Editor

---

# Learning Outcomes

This project helped me understand:
- Data Modeling
- Fact and Dimension Tables
- Relationships
- Cardinality
- Star Schema
- Snowflake Schema
- Hierarchies
- Inactive Relationships
- Power Query Transformations

---

# Conclusion

This project successfully demonstrates practical implementation of Power BI Data Modeling concepts including relational modeling, schema design, hierarchy creation, relationship management, and data transformation using Power Query and Model View.

```"# Data-Modeler-PowerBI-" 
"# Data_Modeler-_-PowerBI-" 
