# MS_Fabric_LAB_7
# Real-Time Intelligence with Microsoft Fabric 🚀

This project demonstrates how to collect, analyze, visualize, and set up alerts using real-time stock market data with **Microsoft Fabric Real-Time Intelligence**.


## 📖 Overview

In this project, you will:
- Set up real-time data streaming (Stock Market Data).
- Persist events into an Eventhouse database.
- Query live data using KQL.
- Create real-time dashboards.
- Configure automated email alerts based on data changes.

## ✨ Features

- Real-time data ingestion
- Eventhouse (KQL Database) integration
- Live querying with KQL
- Real-time dashboard creation
- Automated email alert system

## 🛠️ Technologies Used

- Microsoft Fabric:
  - Real-Time Hub
  - Eventstream
  - Eventhouse (KQL Database)
  - Dashboards
  - Activator (Alerts)
- Kusto Query Language (KQL)

## ⚙️ Setup Instructions

### 1. Create a Fabric Workspace
- Visit [Microsoft Fabric](https://app.fabric.microsoft.com/home?experience=fabric).
- Create a new workspace and ensure Fabric capacity is enabled.

### 2. Connect to the Real-Time Data Stream
- Open the Real-Time Hub.
- Under **Data Sources**, find **Stock Example**.
- Click **Connect**, and name your data source `stock`.
- Name your Eventstream `stock-data-stream`.

### 3. Create an Eventhouse (KQL Database)
- In your workspace, go to **Create > Real-Time Intelligence > Eventhouse**.
- Name your Eventhouse (e.g., `stock-eventhouse`).

### 4. Persist Incoming Events to the Eventhouse
- Open the Eventhouse and access the KQL Database.
- Select **Get Data > Eventstream > Existing Eventstream**.
- Create a table named `stock` and connect it to the `stock-data-stream`.

### 5. Query Real-Time Data
- Open the Query Editor and run the following sample queries:

```kql
stock
| take 100
