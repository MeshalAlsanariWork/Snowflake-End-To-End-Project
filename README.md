# ❄️ Snowflake End-to-End Data Engineering Project

## 🌟 Introduction
In the modern data landscape, efficiency, automation, and security are the pillars of a successful data warehouse. This project, **GSITS (Global Sales and Inventory Tracking System)**, is a hands-on implementation of a full-scale Snowflake environment. It moves beyond basic queries to demonstrate how a Data Engineer manages the entire lifecycle of data—from ingestion to automation and governance—using only Snowflake’s native SQL and scripting capabilities.

## 📌 Project Overview
This project is a comprehensive demonstration of **Snowflake's core and advanced capabilities**. It simulates a global retail environment, covering the entire data lifecycle from environment setup and data loading to automated processing and secure data sharing.

## 🏗️ Technical Architecture
The project follows a modern data warehousing flow:
1. **Ingestion:** Data loading from Internal Stages using `COPY INTO`.
2. **Transformation:** Utilizing DML, Multi-table inserts, and SQL Functions.
3. **Programmability:** Implementing procedural logic via **Stored Procedures (Snowflake Scripting)** and **UDFs/UDTFs**.
4. **Automation:** Scheduling workflows using **Snowflake Tasks**.
5. **Governance:** Implementing **Role-Based Access Control (RBAC)** and Zero-Copy Cloning for dev environments.
    

---

## 💡 Why This Project? (Learning Objectives)
By exploring this repository, you will understand how to:
- **Architect for Scale:** Set up multi-cluster warehouses and structured namespaces.
- **Build Resilient Pipelines:** Use `COPY INTO` with robust file formats for reliable ingestion.
- **Enable Data DevOps:** Utilize **Zero-Copy Cloning** and **Time Travel** to support development and disaster recovery without increasing storage costs.
- **Automate Workflows:** Replace manual reporting with **Stored Procedures** and **Tasks**.
- **Secure Data Assets:** Implement professional-grade **RBAC** (Role-Based Access Control).
    

---

## 🔄 The "End-to-End" Data Flow
1. **Landing:** Raw data (CSV/JSON) is placed in an **Internal Stage** (the Landing Zone).
2. **Structuring:** Data is moved into structured **Permanent Tables** via `COPY INTO`.
3. **Processing:** * **Multi-Table Inserts** split inventory data into specialized tables.
    - **Window Functions** and **UDFs** calculate running totals and commissions.
4. **Automation:** A **Stored Procedure** is triggered by a **Task** every 2 minutes to aggregate daily summaries.
5. **Recovery:** **Time Travel** is used to restore data from previous states, and **Cloning** provides an instant Sandbox for testing.
6. **Egress (Unload):** Refined data is transformed back into **JSON** via `OBJECT_CONSTRUCT` and unloaded to a stage for downstream use.
    


## 🚀 Key Features Demonstrated
### 1. Data Modeling & DDL
- Designed a relational schema with `PRODUCTS` and `SALES_TRANSACTIONS` tables.
- Managed environments using Databases, Schemas, and Virtual Warehouses.
    
### 2. Data Movement (Load/Unload)
- Created **File Formats** (CSV/JSON) and **Named Stages**.
- Performed bulk loading and data unloading to semi-structured JSON.
    
### 3. Advanced SQL & Time Travel
- Used **Zero-Copy Cloning** to instantly create a `DEV` environment.
- Demonstrated **Time Travel** to recover data after accidental deletion.
- Applied **Window Functions** to analyze running totals and category performance.
    
### 4. Automation & Procedural Logic
- **Stored Procedures:** Automated daily summary logging.
- **UDFs:** Created reusable logic for commission calculations.
- **Tasks:** Scheduled serverless-style execution of procedures.
    
### 5. Security & Management
- Implemented **RBAC** by creating custom roles and assigning granular permissions.  
- Managed user defaults and warehouse auto-suspend settings for cost optimization.
    
## 🛠️ Tools & Technologies
- **Platform:** Snowflake (Cloud Data Warehouse)
- **Language:** Snowflake SQL (DDL, DML), Snowflake Scripting 
- **Key Features:** Time Travel, Cloning, Tasks, Stored Procedures, UDFs, RBAC.
    

## 📁 How to Use
1. Open the `snowflake_project.sql` file.
2. Copy the code into a Snowflake Worksheet.
3. Execute the blocks sequentially to build the environment, load data, and trigger automation.

## 🏁 Outro

The **GSITS Project** serves as a blueprint for building high-performance, automated data solutions within the Snowflake ecosystem. It showcases a deep understanding of not just how to write SQL, but how to manage a cloud data platform at an enterprise level—from cost optimization to data integrity.

**Developed by: Meshal Alsanari**
