# Data-Engineering-Project---Azure
End to End Data Engineering Project using Microsoft Azure



## 📘 Project Overview

This repository contains t an end-to-end **Data Engineering pipeline** on **Microsoft Azure**

- 🟫 **Bronze** – Raw data ingestion
- 🥈 Silver – Transformation
- 🥇 Gold – Serving & Analytics

---

# 🟫 Bronze Layer: Data Ingestion – Azure Data Engineering Project

## 🧱 Ingestion Architecture

      [GitHub Data Source]
      ↓
      [Azure Data Factory] —(ForEach + Parameterized Copy)—→ [Azure Data Lake Storage Gen2 (Bronze Zone)]


---

## 🔧 Tools & Technologies Used

- **Azure Data Factory (ADF)** – Orchestration and ingestion
- **Azure Data Lake Storage Gen2 (ADLS)** – Raw data storage
- **Dynamic Content & Parameters** – Used for flexible, reusable pipelines
- **ForEach Activity** – Iterative ingestion from multiple GitHub sources

---

## ⚙️ Key Features

✅ Parameterized ADF pipelines for dynamic ingestion  
✅ Ingestion from GitHub into ADLS Bronze Zone  
✅ Reusable ForEach loop with copy activity  
✅ Scalable structure for future datasets  

---


# 🥈 Silver Layer: Data Transformation – Azure Data Engineering Project

## 🧱 Transformation Architecture
          [ADLS Gen2 (Bronze Zone)]
          ↓
          [Azure Databricks (PySpark)] —→ [ADLS Gen2 (Silver Zone)]

---

## 🔧 Tools & Technologies Used

- **Azure Databricks** – Data transformation and processing
- **Azure Data Lake Storage Gen2 (ADLS)** – Source (Bronze) and target (Silver) storage
- **PySpark (Apache Spark)** – ETL and business logic
- **Azure App Registration** – Authenticated connection between Databricks and ADLS

---

## ⚙️ Key Features

✅ Secure credential-based access from Databricks to ADLS  
✅ Structured PySpark-based transformations  
✅ Writes cleaned and enriched data to Silver Zone in ADLS  
✅ Scalable and modular notebooks for each domain/task  

---

## 🚀 Transformation Logic

1. **Authentication Setup**:
   - Register an application in **Azure Active Directory**
   - Grant access to ADLS container
   - Configure Spark to use OAuth credentials (Client ID, Secret, Tenant ID)

2. **Read Data from Bronze**:
   - Load raw data from ADLS Bronze container using PySpark

3. **Data Transformation**:
   - Clean, normalize, and enrich raw data
   - Apply business logic as needed

4. **Write to Silver**:
   - Save transformed data back into the Silver Zone of ADLS Gen2 in Parquet format

---

## 🟡 Gold Layer – Azure Synapse Analytics & Power BI Integration

### Overview
This layer represents the final stage of the data lakehouse architecture in my Data Engineering project using Azure Synapse Analytics. 
It transforms and exposes curated, business-ready data to enable meaningful analysis and reporting.

### 📌 Key Highlights

 - ✅ Created views from transformed tables available in the Silver Layer.

 - ✅ Used Azure Synapse SQL scripts to define and manage external tables in the Gold Layer.

 - ✅ Leveraged external data sources to access data stored in Azure Data Lake Gen2 using Managed Identity.

 - ✅ Structured the Gold Layer to support Power BI dashboards for insights and decision-making.

### 🔧 Technical Stack

 - *Azure Synapse Analytics (Serverless SQL Pools)*
 - *Azure Data Lake Storage Gen2*
 - *SQL (T-SQL scripts for views & tables)*
 - *Power BI (Direct connection to Synapse for visualization)*




