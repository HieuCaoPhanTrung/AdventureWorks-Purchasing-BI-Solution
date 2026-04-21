# AdventureWorks-Purchasing-BI-Solution

A comprehensive Business Intelligence solution for procurement optimization using SSIS, SSAS, and Power BI based on the AdventureWorks database.

## 📌 Project Overview
This project delivers an end-to-end Business Intelligence (BI) pipeline designed to analyze and optimize the purchasing workflow for **AdventureWorks Cycles**. By transforming raw operational data into actionable insights, the system empowers stakeholders to monitor vendor performance, manage inventory levels, and evaluate employee productivity effectively.

## 🛠 Tech Stack
* **Database:** Microsoft SQL Server (AdventureWorks 2019)
* **ETL Tool:** SQL Server Integration Services (SSIS)
* **Data Modeling:** SQL Server Analysis Services (SSAS) - Multidimensional Mode
* **Visualization:** Microsoft Power BI
* **Languages:** T-SQL, MDX, DAX

## 🏗 Solution Architecture
The project follows a standard BI lifecycle:
1.  **Data Staging:** Extraction from OLTP sources, data profiling, and cleaning.
2.  **Data Warehouse (DWH):** * Implemented **Slowly Changing Dimension (SCD)** types to track historical changes in vendors and products.
    * Designed a **Galaxy Schema** (Fact Constellation) featuring core Fact tables: `FactPurchaseOrders` and `FactInventory`.
3.  **Analytics Layer (OLAP):** * Developed Multidimensional Cubes in SSAS for high-speed analytical processing.
    * Configured complex Measures, KPIs, and Calculated Members using MDX.
4.  **Reporting:** Developed 6 interactive Power BI dashboards providing a 360-degree view of the procurement process.

## 📊 Key Performance Indicators (KPIs)
* **Received Rate:** Percentage of items successfully received vs. ordered (Target: 90%+).
* **Return Rate:** Monitoring defective goods returned to vendors to assess quality.
* **Average Lead Time:** Duration from order placement to warehouse receipt.
* **Inventory Turnover:** Analyzing how efficiently stock is managed and sold.

## 📂 Repository Structure
```text
├── 1.Docs                 # Project Report (PDF), Bus Matrix, Data Dictionary
├── 2.ETL_SSIS             # .dtsx files and control flow logic
├── 3.Analysis_SSAS        # Visual Studio Solution (Cubes, Dimensions, Measures)
├── 4.Visualization_PBI    # Power BI Dashboard files (.pbix)
├── 5.Scripts_SQL          # T-SQL scripts for Staging, DWH, and Stored Procedures
└── README.md              # Project documentation
