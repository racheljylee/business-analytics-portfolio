# Apple Global Sales Strategy – Big Data Pipeline & Market Insights

## Overview

**Group Project**

Built an end-to-end big data pipeline to analyze Apple’s global sales performance and identify **actionable strategies for revenue growth, market expansion, and channel optimization**.

This project integrates **data engineering (NiFi, MinIO, Spark)** with **business analytics** to move from raw data → strategic recommendations.

---

## My Contribution

- Structured the **business problem and analytical framework**
- Contributed to **pipeline design (data ingestion → processing → analysis)**
- Led translation of analytical outputs into **strategic insights**
- Developed **product, channel, and market expansion recommendations**

---

## Business Problem

Apple operates across 30+ markets, but performance varies significantly:

- Revenue per urban consumer differs by up to **8× across countries**  
- Sales performance is influenced by:
  - product mix  
  - sales channels  
  - market characteristics  

> Key question:  
**How can Apple optimise its global sales strategy to drive growth and improve market performance?**

---

## Data & Architecture

### Data Sources

- **Apple Global Sales Data (CSV)**  
  - Product category, sales channel, revenue, units sold  

- **World Population Data (JSON)**  
  - Urban population, demographics, market size  

These datasets enable:

> **Per-capita revenue analysis**, separating true market performance from population scale :contentReference[oaicite:0]{index=0}

---

### Big Data Pipeline

The project implements a full pipeline:

**Ingestion → Storage → Processing**

- **Apache NiFi**
  - Ingests CSV and JSON data
  - Handles transformation (CSV → JSON)

- **MinIO (Data Lake)**
  - Stores:
    - raw data  
    - curated data  

- **Apache Spark (PySpark)**
  - Performs transformations and analysis  

As shown in the pipeline architecture (slides, page 6), data flows from source → NiFi → MinIO → Spark processing :contentReference[oaicite:1]{index=1}

---

## Key Insights

### 1. Revenue Drivers Differ Across Markets

- Two distinct models:
  - **High transaction value** (e.g. Hong Kong, India)  
  - **High basket size** (e.g. Norway, Malaysia)  

- Indicates different customer behaviours:
  - Premium purchases vs ecosystem purchases :contentReference[oaicite:2]{index=2}  

---

### 2. Product Mix Is the Strongest Revenue Driver

- Product category explains the largest share of revenue variation  
- Premium devices drive value, but:

> Balanced ecosystems (devices + accessories) outperform single-product focus :contentReference[oaicite:3]{index=3}  

---

### 3. Market Size ≠ Market Performance

- Smaller developed markets show **highest adoption per capita**  
- Large markets (India, China) remain **underpenetrated**

> Indicates **significant untapped growth potential** :contentReference[oaicite:4]{index=4}  

---

### 4. Channel Strategy Drives Performance

- Top markets rely on:
  - Apple Store  
  - Authorised Resellers  

- Lower-performing markets rely on:
  - Carrier stores  
  - Third-party retailers  

> Direct Apple channels are more effective due to **better customer experience and brand control** :contentReference[oaicite:5]{index=5}  

---

## Strategic Recommendations

### 1. Optimise Product Mix

- Prioritise premium devices  
- Expand ecosystem bundles (e.g. Mac + iPad)  

→ Increases customer lifetime value and platform lock-in  

---

### 2. Strengthen Apple Ecosystem Channels

- Invest in:
  - Apple retail  
  - online channels  

- Use partners strategically in emerging markets  

→ Improves customer engagement and conversion  

---

### 3. Capture Growth in Underpenetrated Markets

Focus: **India & China**

- Large population + low adoption  
- Significant long-term opportunity  

Recommended approach:

- **Short-term:** leverage carriers and retail partners  
- **Long-term:** expand Apple-controlled channels  

---

## Business Impact

- Identifies **clear drivers of revenue performance**
- Supports **market entry and expansion strategy**
- Demonstrates how data can inform:
  - product decisions  
  - channel strategy  
  - geographic prioritisation  

---

## What This Project Demonstrates

- End-to-end thinking: **data pipeline → insights → strategy**
- Ability to combine:
  - data engineering (NiFi, Spark, MinIO)
  - business analysis  
- Strong focus on **decision-making and strategic impact**

---

## Tech Stack

- Apache NiFi (data ingestion)
- MinIO (data lake storage)
- PySpark (data processing & analysis)
- Python

---

## Repository Structure
