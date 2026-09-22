# 🚀 FMCG Data Engineering Project | Databricks

## 📌 Project Overview

This project implements an **end-to-end FMCG Data Engineering pipeline using Databricks**.

The solution demonstrates how data from multiple sources can be ingested, processed, transformed, and converted into analytics-ready datasets using a structured **Medallion Architecture**.

The project includes **full-load and incremental data processing**, dimensional and fact data modeling, data transformations, and a final business dashboard for analytics.

---

## 🏗️ Project Architecture

The project follows a layered data engineering architecture to process source data into business-ready datasets.

![Project Architecture](Resources/project_architecture.png)

### 🔄 High-Level Data Flow

```text
Source Data
     │
     ▼
Data Ingestion
     │
     ▼
┌───────────────┐
│ Bronze Layer  │
│ Raw Data      │
└───────┬───────┘
        │
        ▼
┌───────────────┐
│ Silver Layer  │
│ Cleaned Data  │
└───────┬───────┘
        │
        ▼
┌───────────────┐
│ Gold Layer    │
│ Business Data │
└───────┬───────┘
        │
        ▼
   Dashboard
