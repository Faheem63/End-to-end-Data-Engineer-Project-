🛒 End-to-End E-Commerce Data Engineering Project

<h3 align="center">Azure Data Factory | ADLS | Azure Databricks | PySpark | Delta Lake</h3><p align="center">
  <img src="https://img.shields.io/badge/Azure-Data%20Factory-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white" />
  <img src="https://img.shields.io/badge/Azure-Data%20Lake-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white" />
  <img src="https://img.shields.io/badge/Azure-Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white" />
  <img src="https://img.shields.io/badge/Apache-Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white" />
  <img src="https://img.shields.io/badge/Delta-Lake-00ADD8?style=for-the-badge" />
</p>---

📌 Project Overview

This project demonstrates a real-world End-to-End E-Commerce Data Engineering Pipeline using Azure Data Factory, Azure Data Lake Storage (ADLS), Azure Databricks, Apache Spark (PySpark), Spark SQL, and Delta Lake.

The pipeline extracts source data from APIs using Azure Data Factory, stores it in Azure Data Lake Storage, and processes it through the Medallion Architecture (Bronze → Silver → Gold).

The final output consists of analytics-ready Fact and Dimension tables that support business reporting and data-driven decision-making.

🏗️ Architecture

End-to-End Data Flow

flowchart TD
    A["🌐 Source API"] --> B["Azure Data Factory"]
    B --> C["HTTP Linked Service"]
    C --> D["Copy Data Activity"]
    D --> E[("Azure Data Lake Storage")]
    E --> F["Azure Databricks"]
    F --> G["🥉 Bronze Layer"]
    G --> H["🥈 Silver Layer"]
    H --> I["🥇 Gold Layer"]
    I --> J["Fact & Dimension Tables"]
    J --> K["Spark SQL Analytics"]

    style A fill:#DCEBFA,stroke:#0078D4,color:#000
    style B fill:#DCEBFA,stroke:#0078D4,color:#000
    style E fill:#DCEBFA,stroke:#0078D4,color:#000
    style G fill:#EADCC8,stroke:#9C6B30,color:#000
    style H fill:#E0F0E5,stroke:#27834B,color:#000
    style I fill:#FFF0CC,stroke:#C18B22,color:#000

🔄 Pipeline Implementation

1️⃣ Data Ingestion – Azure Data Factory

- Connected to the source API using an HTTP Linked Service.
- Configured ADLS Linked Service as the destination.
- Implemented the Copy Data activity.
- Extracted data from the API and loaded it into Azure Data Lake Storage.
- Stored raw source data for further processing.

2️⃣ 🥉 Bronze Layer – Raw Data

- Loaded raw CSV files from ADLS.
- Performed minimal transformations.
- Inferred schema from source data.
- Stored data as Delta tables.
- Maintained the historical raw data layer.

3️⃣ 🥈 Silver Layer – Data Cleaning & Transformation

- Removed duplicate records.
- Standardized timestamps.
- Filtered only delivered orders.
- Added derived columns such as Total Order Amount.
- Created clean and validated datasets.

4️⃣ 🥇 Gold Layer – Business & Analytics

- Designed a Star Schema.
- Created Fact and Dimension tables.
- Prepared analytics-ready datasets.
- Used Spark SQL to generate business insights.

---

📂 Dataset Details

Dataset| Description
Customers| Customer information
Orders| Order transaction details
Order Items| Individual items in each order
Products| Product information
Sellers| Seller details

⚙️ Technology Stack

Technology| Implementation
Azure Data Factory| API ingestion
Azure Data Lake Storage| Data storage
Azure Databricks| Data processing
Apache Spark| Distributed processing
PySpark| Data transformations
Spark SQL| Business analysis
Delta Lake| Reliable data storage
Medallion Architecture| Data organization

📊 Business Insights

The Gold layer supports the following business analysis:

- 💰 Revenue by customer state.
- 🛍️ Top-selling product categories.
- 📈 Monthly sales trend analysis.

▶️ How to Execute

1. Configure the source API using an HTTP Linked Service in ADF.
2. Configure the destination ADLS Linked Service.
3. Create and execute the ADF pipeline using Copy Data activity.
4. Load the ingested files into Azure Databricks.
5. Run the Bronze layer notebook.
6. Run the Silver layer notebook.
7. Run the Gold layer notebook.
8. Execute Spark SQL queries for business analytics.

📁 Project Structure

E-Commerce-Data-Engineering/
│
├── ADF/
│   └── Pipeline Configuration
│
├── Notebooks/
│   ├── Bronze_Layer
│   ├── Silver_Layer
│   └── Gold_Layer
│
├── Datasets/
│   ├── Customers
│   ├── Orders
│   ├── Order_Items
│   ├── Products
│   └── Sellers
│
├── Images/
│   └── Data_Pipeline_Architecture.png
│
└── README.md

🎯 Key Learnings

- API data ingestion using Azure Data Factory.
- HTTP Linked Service configuration.
- Data movement from API to ADLS.
- Implementation of Medallion Architecture.
- Data cleaning and transformation using PySpark.
- Delta Lake table management.
- Star Schema and dimensional data modeling.
- Business analytics using Spark SQL.

🚀 Project Outcome

Built an end-to-end E-Commerce Data Engineering pipeline that integrates API ingestion, cloud storage, distributed data processing, and business analytics.

The project demonstrates practical implementation of modern Azure Data Engineering concepts, from raw data extraction to analytics-ready datasets.

---

<p align="center">
  <b>Built with ❤️ using Azure Data Engineering Technologies</b>
</p>
