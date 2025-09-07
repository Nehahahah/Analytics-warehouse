# 📊 Analytics Warehouse – By Neha Pal

This project demonstrates how to design and build a **modern data warehouse** using SQL Server.  
It follows the **Medallion Architecture** (Bronze → Silver → Gold) to transform raw ERP and CRM data into **business-ready insights**.

---

## 🏗️ Data Architecture

The project is structured into three layers:

![Data Architecture](docs/data_architecture.png)

1. **Bronze Layer** → Raw data ingested from ERP & CRM CSV files.  
2. **Silver Layer** → Data cleansing, transformation, and standardization.  
3. **Gold Layer** → Star schema with fact and dimension tables for analytics.  

---

## 📖 Project Overview

- **Data Architecture** → Built a warehouse with Bronze, Silver, and Gold layers.  
- **ETL Pipelines** → Automated ingestion and transformation using SQL scripts.  
- **Data Modeling** → Created fact and dimension tables to support analytics.  
- **Analytics & Reporting** → Delivered insights on customer behavior, product performance, and sales trends.  

---

## 🛠️ Tools & Technologies

| Layer/Function       | Tool/Tech                                  |
| -------------------- | ------------------------------------------ |
| Data Storage         | SQL Server, CSV                            |
| ETL / Transformation | SQL Scripts, Draw\.io                      |
| Data Modeling        | Star Schema, Draw\.io                      |
| Analytics / BI       | SQL Queries, Tableau / Power BI (optional) |
| Documentation        | Markdown, Draw\.io                         |
| Version Control      | Git, GitHub                                |
| Testing              | SQL Test Scripts                           |




