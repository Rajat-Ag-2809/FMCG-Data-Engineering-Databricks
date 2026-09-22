# 🚀 FMCG Data Engineering Project | Databricks

![Databricks](https://img.shields.io/badge/Databricks-Data%20Engineering-orange?logo=databricks)
![PySpark](https://img.shields.io/badge/PySpark-Data%20Processing-orange?logo=apachespark)
![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![SQL](https://img.shields.io/badge/SQL-Data%20Transformation-blue)
![AWS S3](https://img.shields.io/badge/AWS%20S3-Cloud%20Storage-orange?logo=amazons3)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-Lakehouse-blue)

## 📌 Project Overview

This project implements an **end-to-end FMCG Data Engineering pipeline using Databricks**.

The solution demonstrates how raw data from different sources can be ingested, processed, transformed, and converted into **analytics-ready business data** using the **Medallion Architecture (Bronze → Silver → Gold)**.

The project includes:

- Cloud-based data storage using **Amazon S3**
- Data ingestion and processing using **Databricks**
- Data transformation using **PySpark and SQL**
- Bronze, Silver, and Gold data layers
- Dimension and Fact data modeling
- Full-load and incremental-load processing
- Delta-based data processing
- Business-ready datasets
- Final dashboard for analytics and reporting

---

# 🏗️ Solution Architecture

The project follows a **Medallion Architecture** to organize data processing into multiple layers.

![Project Architecture](resources/project_architecture.png)

### 🔄 High-Level Data Flow

```text
                 Source Data
                     │
                     ▼
              Amazon S3 Storage
                     │
                     ▼
               Databricks
                     │
          ┌──────────┴──────────┐
          ▼                     ▼
     Bronze Layer          Data Processing
          │                     │
          └──────────┬──────────┘
                     ▼
               Silver Layer
                     │
                     ▼
                Gold Layer
                     │
                     ▼
             Business Analytics
                     │
                     ▼
                Dashboard

# 🔄 Data Engineering Workflow

## 1. Data Ingestion

The project uses FMCG source data containing information related to:

* Customers
* Products
* Gross pricing
* Orders

The source data contains both **full-load and incremental-load datasets**.

```text
Source Files
     │
     ├── Customer Data
     ├── Product Data
     ├── Pricing Data
     └── Order Data
```

---

# 🥉 2. Bronze Layer

The Bronze layer stores the ingested source data with minimal transformation.

### Key activities

* Source data ingestion
* Raw data storage
* Initial schema handling
* Maintaining source-level data
* Supporting full and incremental loads

The Bronze layer acts as the foundation for downstream processing.

---

# 🥈 3. Silver Layer

The Silver layer contains cleaned and transformed data.

### Data processing includes:

* Data cleansing
* Data type conversion
* Duplicate handling
* Data validation
* Standardization
* Applying transformation logic
* Preparing dimension and fact datasets

### Dimension Processing

The project processes the following dimension data:

* Customer
* Product
* Pricing
* Date

---

# 🥇 4. Gold Layer

The Gold layer contains **business-ready datasets** designed for analytics and reporting.

The processed dimension and fact data are combined and transformed to create datasets suitable for downstream analysis.

### Key activities

* Business transformations
* Data aggregation
* Fact and dimension integration
* Analytics-ready data preparation
* Dashboard data preparation

---

# 🔁 Full Load & Incremental Load

One of the key components of this project is implementing both **full-load and incremental-load processing**.

### Full Load

The complete dataset is processed during the initial load.

```text
Source
  ↓
Full Dataset
  ↓
Transformation
  ↓
Target Table
```

### Incremental Load

Only newly arrived or changed data is processed during subsequent runs.

```text
New / Changed Data
        ↓
Incremental Processing
        ↓
Transformation
        ↓
Target Table
```

This approach helps reduce unnecessary processing when dealing with continuously arriving data.

---

# 📓 Databricks Notebooks

The project is organized into separate notebooks based on different processing responsibilities.

### Setup

```text
1_codes/
└── 1_setup/
    ├── setup_catalog.ipynb
    ├── utilities.ipynb
    └── dim_date_table_creation.ipynb
```

### Dimension Data Processing

```text
2_dimension_data_processing/
├── 1_customers_data_processing.ipynb
├── 2_products_data_processing.ipynb
└── 3_pricing_data_processing.ipynb
```

### Fact Data Processing

```text
3_fact_data_processing/
├── 1_full_load_fact.ipynb
└── 2_incremental_load_fact.ipynb
```

---

# 📊 Dashboard

The final processed data is used to generate a business dashboard for analyzing FMCG data.

![FMCG Dashboard](2_dashboarding/fmcg_dashboard.pdf)

### Dashboard Focus

The dashboard provides business-level insights from the processed Gold-layer data.

It enables analysis of:

* Sales performance
* Product performance
* Customer trends
* Pricing information
* Order-related metrics
* Business KPIs

---

# 📁 Project Structure

```text
project-de-fmcg-atlikon/
│
├── 0_data/
│   ├── 1_parent_company/
│   │   ├── full_load/
│   │   └── incremental_load/
│   │
│   └── 2_child_company/
│       └── full_load/
│
├── 1_codes/
│   ├── 1_setup/
│   │   ├── setup_catalog.ipynb
│   │   ├── utilities.ipynb
│   │   └── dim_date_table_creation.ipynb
│   │
│   ├── 2_dimension_data_processing/
│   │   ├── customers_data_processing.ipynb
│   │   ├── products_data_processing.ipynb
│   │   └── pricing_data_processing.ipynb
│   │
│   └── 3_fact_data_processing/
│       ├── full_load_fact.ipynb
│       └── incremental_load_fact.ipynb
│
├── 2_dashboarding/
│   ├── denormalise_table_query_fmcg.txt
│   └── fmcg_dashboard.pdf
│
├── resources/
│   ├── project_architecture.png
│   └── databricks_project.excalidraw
│
└── README.md
```

---

# 🔑 Key Data Engineering Concepts

This project demonstrates practical implementation of:

* ✅ Databricks
* ✅ PySpark
* ✅ SQL
* ✅ Delta Lake
* ✅ Lakehouse Architecture
* ✅ Medallion Architecture
* ✅ ETL / ELT
* ✅ Full Load Processing
* ✅ Incremental Load Processing
* ✅ Dimension & Fact Data Modeling
* ✅ Data Transformation
* ✅ Data Cleaning
* ✅ Data Validation
* ✅ Data Aggregation
* ✅ Business Intelligence

---

# 🎯 Project Highlights

### End-to-End Pipeline

Designed a complete workflow from **source data ingestion to business analytics**.

### Medallion Architecture

Implemented **Bronze, Silver, and Gold layers** to organize data processing.

### Incremental Processing

Implemented incremental processing for order/fact data to handle newly arriving data efficiently.

### Dimensional Modeling

Processed customer, product, pricing, and date dimensions along with fact/order data.

### Analytics

Created a final dashboard using the processed business-ready data.

---

# 📚 What I Learned

Through this project, I gained practical experience in:

* Building end-to-end data pipelines using Databricks.
* Working with PySpark and SQL.
* Implementing Medallion Architecture.
* Processing full and incremental data loads.
* Working with Delta Lake.
* Designing fact and dimension data models.
* Transforming raw data into analytics-ready datasets.
* Connecting data engineering pipelines with business dashboards.

---

# 📌 Reference

This project was developed as a **learning project based on a Databricks FMCG Data Engineering tutorial** and was implemented to gain practical hands-on experience with modern data engineering concepts.

[YouTube Tutorial](https://www.youtube.com/watch?v=U6ZUKWdfSLY)
