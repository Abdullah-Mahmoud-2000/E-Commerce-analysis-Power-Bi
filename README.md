# E-Commerce-analysis-Power-Bi
Data Analysis Project using Power Bi dashboard on E-Commerce dataset

## 📊 Project Overview
This project focuses on analyzing sales transactions using **Power BI**.  
The goal is to clean the data, build a simple and efficient data model, and create interactive dashboards to extract business insights.

The dataset contains transactional sales data including orders, customers, products, dates, quantities, prices, and countries.

---

## 🧹 Data Cleaning (Power Query)
The following steps were applied in Power Query:

- Renamed columns to meaningful business names
- Converted data types (IDs as Text, Dates as Date)
- Handled missing values:
  - Replaced missing Product Name with **"Adjustment"**
  - Replaced missing Customer ID with **"Unknown"**
- Kept negative quantities to represent returns and adjustments
- Removed unnecessary columns

---

## 🧩 Data Model
A **hybrid model** was used to balance simplicity and best practices:

- **Fact Table**
  -`Order`

- **Dimension Tables**
  - `DimCustomer`
  - `DimCountry`
  - `DimDate`

> Product data was kept in the fact table due to data quality issues and limited product attributes.

### Relationships
- Order[Customer ID] → DimCustomer[Customer ID]
- Order[Country] → DimCountry[Country]
- Order[Order Date] → DimDate[Date]

All relationships are **One-to-Many** and **Single Direction**.

---

## 📅 Date Dimension
The `DimDate` table was created from the order date column and includes:
- Year
- Month Number
- Month Name (sorted correctly)
- Quarter
- Day

---

## 📐 Measures (DAX)
Key measures used in the analysis:

- **Total Revenue**
- **Total Quantity**
- **Orders Count**
- **Customers Count**

Revenue was calculated dynamically using DAX to ensure flexibility and performance.

---

## 📈 Dashboard Insights
The dashboard answers key business questions such as:
- Total revenue and total orders and total Quantity and Customers Count
- Sales trend by month
- Revenue by country
- Top selling products
- Impact of adjustments and returns

---

## 🛠 Tools Used
- Power BI Desktop
- Power Query
- DAX
- GitHub

---

## 🚀 Key Learnings
- Data cleaning and preparation using Power Query
- Building a clean and efficient data model
- Creating a Date Dimension without complex DAX
- Using DAX measures instead of calculated columns
- Designing interactive Power BI dashboards

---

Due to file size limitations, the dataset is hosted externally:
The dataset used in this project is available here: [Download the Excel dataset](https://drive.google.com/file/d/1uWLBRNhOheUTNsN7Xi7t4RcyXQ3q-HSc/view?usp=drive_link)
