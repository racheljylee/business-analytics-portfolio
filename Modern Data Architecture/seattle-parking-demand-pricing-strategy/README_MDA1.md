# Parking Space Optimization in Seattle: Modern Data Architecture Project

## Project Overview
This project was developed as part of a **group assignment** for the *Modern Data Architectures for Big Data I* course. It focuses on designing and implementing a scalable data pipeline to analyze parking usage in Seattle and generate insights to support data-driven decision-making.

The central objective is to answer the question:

**How can the Seattle Department of Transportation (SDOT) optimize parking spaces across the city?**

---

## Problem Statement
Seattle is one of the most congested cities in the United States, with a significant portion of traffic caused by drivers searching for parking.  

SDOT aims to:
- Reduce congestion  
- Improve parking turnover  
- Align pricing with demand  

This project combines historical and real-time data to analyze parking utilization and pricing efficiency.

---

## Data Sources

### 1. Annual Parking Study Data (CSV)
- Period: 2014–2019  
- Contains:
  - Occupancy rates  
  - Block-level parking data  
  - Time-of-day segments  
- Purpose: Analyze long-term parking trends  

### 2. Paid Parking Transactions (JSON)
- Source: Seattle Open Data Portal  
- Period: ~1 week (recent data snapshot)  
- Contains:
  - Transaction timestamps  
  - Locations  
  - Payment amounts  
  - Parking duration  
- Purpose: Capture real-time parking behavior  

---

## Architecture Overview

The project implements a modern data pipeline with the following components:

### Data Ingestion (Apache NiFi)
- CSV data ingested from local files  
- JSON data ingested via API  
- Data routed and processed using NiFi workflows  
- Stored in object storage (MinIO/S3-compatible)

Example flow:
- `GetFile` → ingest CSV data  
- `InvokeHTTP` → fetch JSON data  
- `PutS3Object` → store data in object storage  

---

### Data Storage (MinIO)
- S3-compatible object storage  
- Separate storage paths for:
  - `/csv/` (historical data)
  - `/json/` (transaction data)

---

### Data Processing (PySpark)
- Data cleaning and transformation  
- Feature engineering:
  - Occupancy rate (utilization)
  - Time-based aggregations  
- Analytical queries to extract insights  

---

### Data Analysis (Jupyter Notebook)
- Exploratory data analysis  
- Visualization of utilization patterns  
- Comparison across:
  - Study areas  
  - Years  
  - Pricing levels  

---

## Key Concepts

### Parking Utilization
- Occupancy Rate = Number of parked vehicles / Total available spaces  

High utilization (> 0.80) indicates high demand  
Low utilization (< 0.70) indicates low demand  

---

## Key Insights

### 1. Demand is Location-Driven
- Largest variation in utilization occurs across study areas  
- Demand is driven more by location than supply  

### 2. Construction Impacts Parking
- Construction reduces parking utilization  
- Effects can persist beyond active construction periods  

### 3. Clear High- and Low-Demand Zones
- High-demand areas: First Hill, Green Lake, Uptown, Fremont  
- Low-demand areas: Roosevelt, Columbia City, Commercial Core  

### 4. Pricing Misalignment
- Prices are not always aligned with demand levels  
- Opportunity for dynamic pricing strategies  

---

## Recommendations

### 1. Pricing Optimization
- Increase prices in high-demand areas  
- Reduce prices in low-demand areas  

### 2. Infrastructure Optimization
- Reallocate parking spaces from low-demand zones  
- Convert underutilized areas to alternative uses  

### 3. Dynamic Management
- Implement real-time dynamic pricing  
- Use predictive analytics for demand forecasting  
- Conduct regular performance reviews
