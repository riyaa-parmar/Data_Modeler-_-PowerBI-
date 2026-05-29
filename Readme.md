# 📊 Power BI Data Modeling Project

## 📌 Overview

This project demonstrates Data Modeling concepts in Power BI using:

* Fact Tables
* Dimension Tables
* Relationships
* Cardinality
* Star Schema
* Snowflake Schema
* Hierarchies
* Inactive Relationships

---

# 🛠️ Tools Used

* Microsoft Power BI Desktop
* Power Query Editor

---

# 📂 Tables Used

## Fact Tables

* Sales_Fact
* Returns_Fact

## Dimension Tables

* Customer_Dim
* Product_Dim
* Region_Dim
* Date_Dim

---

# 🔑 Primary Keys and Foreign Keys

## Primary Keys

* Customer_Dim → CustomerID
* Product_Dim → ProductID
* Region_Dim → RegionID
* Date_Dim → DateID

## Foreign Keys

### Sales_Fact

* CustomerID → Customer_Dim.CustomerID
* ProductID → Product_Dim.ProductID
* RegionID → Region_Dim.RegionID
* DateID → Date_Dim.DateID

### Returns_Fact

* OrderID → Sales_Fact.OrderID
* DateID → Date_Dim.DateID (Inactive Relationship)

---

# ✨ Features

* Data Cleaning using Power Query
* Relationship Creation
* Star Schema Design
* Cardinality Handling
* Hierarchies
* Matrix Table Verification
* Model Enhancement

---

# 📖 Concepts Used

* Fact Table
* Dimension Table
* Primary Key
* Foreign Key
* Relationships
* Cardinality
* Star Schema
* Snowflake Schema
* Inactive Relationships
* Cross Filter Direction

---

# 🔄 Project Workflow

1. Imported Data
2. Cleaned and Transformed Data
3. Created Relationships
4. Applied Cardinality
5. Built Star Schema
6. Created Hierarchies
7. Verified Model using Matrix Tables

---

📁 Folder Structure
Data_Modeler_PowerBI
│
├── Document
│   └── Data Modeler (Project Report).pdf
│
├── PowerBI_File
│   └── Data Modeler.pbix
│
├── excel_dataset
│   ├── Customer_Dim.xlsx
│   ├── Date_Dim.xlsx
│   ├── Product_Dim.xlsx
│   ├── Region_Dim.xlsx
│   ├── Returns_Fact.xlsx
│   └── Sales_Fact.xlsx
│
└── Readme.md

---

## 👩‍💻 Author

**Riya Parmar**

GitHub:
https://github.com/riyaa-parmar

---

⭐ If you find this project useful, consider starring the repository!
