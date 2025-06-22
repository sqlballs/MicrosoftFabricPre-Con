# Module 04 - Fabric SQL Database

## Overview

The Fabric SQL Database is a core component of Microsoft Fabric that provides a fully managed, scalable, and performant SQL engine for analytics workloads. It enables users to query structured data using familiar T-SQL syntax while integrating seamlessly with other Fabric components like Lakehouse, Pipelines, and Power BI.

This module introduces the Fabric SQL Database, its architecture, use cases, and how to interact with it using the Fabric portal and external tools.

---

## Learning Objectives

By the end of this module, you will be able to:

- Understand what the Fabric SQL Database is and how it fits into the Microsoft Fabric ecosystem.
- Create and configure a Fabric SQL Database.
- Load and query data using T-SQL.
- Connect to the SQL endpoint from tools like SSMS, Azure Data Studio, and Power BI.
- Understand security, performance, and governance considerations.

---

## Key Concepts

| Concept | Description |
|--------|-------------|
| **SQL Endpoint** | A TDS-compatible endpoint that allows external tools to connect to the Fabric SQL Database. |
| **Warehouse vs Lakehouse** | Warehouses are optimized for structured, relational workloads; Lakehouses are optimized for semi-structured and unstructured data. |
| **Direct Lake Mode** | Enables Power BI to query Fabric SQL Database directly without data movement. |
| **Security** | Supports role-based access control, row-level security, and integration with Microsoft Entra ID. |

---

## Hands-On Lab

### Step 1: Create a Fabric SQL Database

1. Go to https://app.fabric.microsoft.com.
2. Select your workspace.
3. Click **New** > **SQL Database (Warehouse)**.
4. Name your database (e.g., `SalesWarehouse`) and click **Create**.

### Step 2: Load Data

You can load data using:

- **Pipelines**: Use Dataflows Gen2 or Copy Data activities.
- **T-SQL**: Use `COPY INTO` or `INSERT` statements.
- **Shortcuts**: Reference data from Lakehouse or OneLake.

### Step 3: Query Data

Use the built-in SQL editor or connect via:

- **SQL Server Management Studio (SSMS)**
- **Azure Data Studio**
- **Power BI Desktop**

Example query