Analytics Warehouse Naming Conventions

Author: Neha Pal
Version: 1.0
Last Updated: 2025-09-08

This document defines the naming conventions for schemas, tables, views, columns, and stored procedures in the Analytics Warehouse project. Following these conventions ensures consistency, clarity, and maintainability across the data warehouse.

Table of Contents

General Principles

Table Naming Conventions

Bronze Layer

Silver Layer

Gold Layer

Column Naming Conventions

Surrogate Keys

Technical Columns

Stored Procedure Naming

General Principles

Case & Format: Use snake_case with lowercase letters; separate words with underscores (_).

Language: All names must be in English.

Reserved Words: Avoid using SQL reserved keywords as object names.

Descriptive Names: Names should clearly indicate the object’s purpose.

Table Naming Conventions
Bronze Layer

Tables should directly reflect source system names without modification.

Format: <sourcesystem>_<entity>

<sourcesystem>: Name of the source system (e.g., crm, erp).

<entity>: Original table name from the source system.

Example: crm_customer_info → Customer information from CRM.

Silver Layer

Follow the same convention as Bronze for clarity and traceability.

Example: erp_orders → Orders table from ERP system.

Gold Layer

Use business-aligned, meaningful names starting with a category prefix.

Format: <category>_<entity>

<category>: Describes table type: dim (dimension), fact (fact table), report (aggregated/report table).

<entity>: Descriptive name aligned with business concepts.

Examples:

dim_customers → Dimension table for customer data

fact_sales → Fact table for sales transactions

report_sales_monthly → Aggregated monthly sales report

Category Glossary
Prefix	Meaning	Examples
dim_	Dimension table	dim_customer, dim_product
fact_	Fact table	fact_sales, fact_orders
report_	Report table	report_customers, report_sales_monthly
Column Naming Conventions
Surrogate Keys

Primary keys in dimension tables must end with _key.

Format: <table_name>_key

Example: customer_key in dim_customers

Note: Fact tables reference these keys as foreign keys.

Technical Columns

System-generated or metadata columns start with dwh_.

Format: dwh_<column_name>

Examples:

dwh_load_date → Date the record was loaded

dwh_source_file → Source file name for auditing

Stored Procedure Naming

All stored procedures should indicate the action and layer.

Format: load_<layer>_<entity> (entity is optional for full layer loads)

<layer>: bronze, silver, or gold

Examples:

load_bronze → Load entire Bronze layer

load_silver_orders → Load Silver layer orders table

load_gold_sales → Load Gold layer sales data