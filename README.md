# Retail Sales Performance Dashboard (Power BI)

## Project Overview
This repository contains an interactive multi-page Power BI dashboard designed to analyze retail sales performance, profitability, customer segment distributions, and geographic regional trends for a business-to-business retail group. 

The goal of this project is to transform raw sales transaction records into an executive-ready business intelligence solution that answers critical operational questions.

## Skills & Tools Used
* **Data Transformation:** Power Query (Data cleaning, text trimming, data type localization, conditional filtering).
* **Data Modeling:** Star Schema design, explicit 1-to-Many relationships, and a custom DAX-generated Master Calendar Table.
* **DAX Formulas:** Calculated Measures for core business metrics (`Total Sales`, `Total Profit`, `Total Orders`, and `Profit Margin`).
* **UI/UX Design:** Container-based card layouts, dynamic report page tooltips, cross-filtering, and cohesive commercial color palettes.

## Data Architecture & DAX
A custom master `Calendar` table was constructed to manage time intelligence calculations. 

### Core DAX Measures Implemented:
* **Total Sales:** `Total Sales = SUM(Superstore[Sales])`
* **Total Profit:** `Total Profit = SUM(Superstore[Profit])`
* **Total Orders:** `Total Orders = DISTINCTCOUNT(Superstore[Order ID])`
* **Profit Margin:** `Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)`

## Dashboard Layout & Visuals

### 1. Executive Summary
Provides a high-level overview of core KPIs over time, allowing managers to instantly monitor sales trajectories and structural business margins.

### 2. Product Performance Analysis
Breaks down categorical sales distributions to isolate high-revenue items versus items with low or negative profitability margins.

### 3. Customer Analysis
Tracks client segment volume distributions and details high-value account contributions using interactive data grids.

### 4. Regional Performance
An interactive geographic map coupled with structured rank metrics to highlight localized areas driving structural losses or revenue gains.

## Key Business Insights
* **Profitability Pitfalls:** The *Technology* category accounts for the highest total profit contribution, whereas specific items in *Furniture* (like Tables) show strong raw sales volume but negative net margins.
* **Regional Drivers:** California and New York serve as core revenue strongholds, while specific regions reveal clear operation-level deficits requiring immediate supply-chain adjustment.
* **Segment Breakdown:** The *Consumer* base remains the primary transactional engine, generating the absolute majority of global order traffic.

## How to Open the Project
1. Clone this repository to your machine.
2. Install the latest version of [Power BI Desktop](https://powerbi.microsoft.com/desktop/).
3. Open the file located in `Dashboard/Retail Sales Dashboard.pbix`.
