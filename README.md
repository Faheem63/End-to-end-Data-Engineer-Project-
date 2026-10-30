🛒 End-to-End E-Commerce Data Engineering Project

Azure Data Factory | ADLS | Azure Databricks | PySpark | Delta Lake

---

📌 Overview

This repository contains an end-to-end Data Engineering project built using Azure Data Factory (ADF), Azure Data Lake Storage (ADLS), Azure Databricks, Apache Spark (PySpark), Spark SQL, and Delta Lake, following the Medallion Architecture (Bronze → Silver → Gold).

The project simulates a real-world e-commerce analytics pipeline, where source data is extracted from APIs using Azure Data Factory, stored in Azure Data Lake Storage, and processed using Databricks to create analytics-ready Fact and Dimension tables for business reporting and insights.

🏗️ Architecture – End-to-End Data Pipeline

Pipeline Flow:

"Source API" → "Azure Data Factory" → "Azure Data Lake Storage" → "Databricks" → "Bronze" → "Silver" → "Gold" → "Business Analytics"

⚙️ Pipeline Implementation

1. Data Ingestion – Azure Data Factory (ADF)

- Connected to the source API using an HTTP Linked Service.
- Configured an HTTP Dataset to access API data.
- Created an Azure Data Lake Storage (ADLS) Linked Service.
- Used the Copy Data Activity to extract data from the API and load it into ADLS.
- Stored ingested source data in the Data Lake for further processing.

2. 🥉 Bronze Layer – Raw Data

- Ingested raw CSV files from Azure Data Lake Storage.
- Performed minimal transformations.
- Inferred schema from the source.
- Stored data as Delta tables in Databricks.
- Maintained raw data as a historical and audit layer.

3. 🥈 Silver Layer – Cleaned & Transformed

- Removed duplicate records.
- Standardized timestamps.
- Filtered only delivered orders.
- Added derived columns (total order amount).
- Created clean, business-ready datasets.

4. 🥇 Gold Layer – Analytics & Business

- Designed a Star Schema.
- Created Fact and Dimension tables.
- Optimized data for analytics and reporting.
- Used Spark SQL to generate business insights.

📂 Datasets – E-Commerce

Dataset| Description
Customers| Customer information
Orders| Order details
Order Items| Individual order item details
Products| Product information
Sellers| Seller information

🛠️ Tech Stack

- Azure Data Factory (ADF)
- Azure Data Lake Storage (ADLS)
- Azure Databricks
- Apache Spark (PySpark)
- Spark SQL
- Delta Lake
- Medallion Architecture

🔄 End-to-End Data Pipeline Flow

1. Extract source data from APIs using Azure Data Factory.
2. Configure HTTP Linked Service to connect to the source API.
3. Configure ADLS Linked Service as the destination.
4. Use Copy Data Activity to move API data into Azure Data Lake Storage.
5. Load raw CSV data from ADLS into Databricks Bronze Delta tables.
6. Clean, validate, and enrich data in the Silver layer.
7. Create Fact and Dimension tables in the Gold layer.
8. Perform business analysis using Spark SQL.

📊 Business Insights Generated

- Revenue by customer state.
- Top-selling product categories.
- Monthly sales trend analysis.

▶️ How to Run the Project

1. Configure the source API connection in Azure Data Factory using an HTTP Linked Service.
2. Configure the destination ADLS connection.
3. Execute the ADF pipeline to ingest API data into ADLS.
4. Access the ingested source files from Azure Databricks.
5. Execute the Bronze layer notebook.
6. Execute the Silver layer notebook.
7. Execute the Gold layer notebook.
8. Run Spark SQL queries for business analytics.

📌 Key Takeaways

- End-to-end data ingestion using Azure Data Factory.
- API integration using HTTP Linked Service.
- Data movement from API to Azure Data Lake Storage.
- Practical implementation of Medallion Architecture.
- Real-world PySpark transformations.
- Delta Lake table management.
- Fact and Dimension data modeling.
- Business-driven analytics using Spark SQL.
