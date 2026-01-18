## Customer 360 – Microsoft Fabric (E‑Commerce)
A complete end‑to‑end Customer 360 solution built using Microsoft Fabric Lakehouse, PySpark, Data Pipelines, and Power BI to unify customer data scattered across multiple e‑commerce systems.

📌 Project Overview
Modern e‑commerce companies interact with customers across multiple channels such as:
Website
Mobile Apps
Customer Service
Order Management System (OMS)
Payment Gateways

However, customer data is often fragmented across these systems, making it difficult to:

Understand the full customer lifecycle
Identify high‑value customers
Personalize marketing campaigns
Improve customer retention
Analyze behavior across touchpoints

To solve these challenges, this project builds a single, unified Customer 360 view inside Microsoft Fabric.

🎯 Objective
Create a Customer 360 Dashboard in Microsoft Fabric by integrating, cleaning, and modeling data from multiple messy sources using:

ADLS / Data Pipelines
Microsoft Fabric Lakehouse
PySpark Notebooks
Silver & Gold Medallion Layers
Power BI

The final dashboard provides insights across the entire customer journey, including:

Customer Profile
Purchase Behavior
Payment History
Customer Support Interactions
Website & App Activity


📂 Architecture & Data Flow
1. Data Ingestion (Bronze Layer)

Raw data from various source systems (Web/App Logs, Orders, Payments,  Customer Support) is copied to Azure Data Lake Storage (ADLS).
A Data Pipeline is used to load the raw files into the Fabric Lakehouse.
Files are stored in Parquet format under the Bronze folder.

Tools & Technologies:
✔ Data Pipelines
✔ ADLS Gen2
✔ Lakehouse (Bronze)
✔ Parquet Files

2. Data Cleaning & Standardization (Silver Layer)

Using PySpark Notebooks, raw data is cleaned, validated, and standardized.
Transformations performed:

Removing duplicates
Handling missing values
Standardizing date formats

Cleaned data is saved into Silver Tables in the Lakehouse.

Outputs:
✔ Cleaned, structured Silver tables
✔ Ready for analytics and modeling

3. Business Modeling (Gold Layer)

From Silver tables, curated Gold tables are created for analytics.
Only business‑ready fields are selected.
Tables created include: gold_cust_360

These tables serve as the semantic layer for Power BI.

4. Reporting & Insights (Power BI)
A Power BI report is built on top of the Gold layer to provide:

Customer Profile Summary
Total Spend
Purchase Patterns & Frequency
Payment History
Customer Service Tickets
Web/App Engagement Metrics
High‑value Customer Segmentation

Final Output:
📊 A complete Customer 360 Dashboard consolidated from all channels.
