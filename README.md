# Vrinda Store Sales Performance Dashboard (2022) - Project Plan

This document outlines the revised scope, structure, and objectives for the Vrinda Store Sales Performance Dashboard (2022) project, focusing on core sales, customer insights, and strategic implementation.

## 1. Project Overview & Objectives

**Project Title:** Vrinda Store Sales Performance Dashboard (2022)

**Objective:** To analyze 2022 sales data to identify key revenue drivers, major customer segments, and geographic opportunities, providing actionable strategies for sales growth in 2023.

**Dataset Source:** Vrinda Store Data Analysis.xlsx

**Target Audience:** Vrinda Store Management, Marketing Team, and Inventory Planners

## 2. Dataset Information and Schema Inferences

This analysis is built upon the Vrinda Store Sales Data (2022), which contains 31,047 unique order records.

### 2.1 Inferred Database Schema

The dataset includes 19 columns, categorized as follows:

| Category | Column Name | Data Type | Description |
|----------|-------------|-----------|-------------|
| Order Details | Order ID, SKU, Status, Date | Object, Int/Datetime | Unique identifiers, delivery status, and date of transaction |
| Customer Info | Cust ID, Gender, Age | Int, Object, Int | Demographic information used for segmentation |
| Product Metrics | Category, Size, Qty, Amount | Object, Object, Object/Int, Int | Product line, size, number of units sold, and sales amount (in INR) |
| Logistics | ship-city, ship-state, ship-postal-code, ship-country | Object, Int | Geographical information for shipment and regional analysis |
| Channel Info | Channel, currency, B2B | Object, Object, Boolean | Sales platform (e.g., Myntra, Amazon), currency, and business-to-business flag |

### 2.2 Data Cleaning and Preparation

Based on the initial data inspection, the following critical cleaning steps are required:

- **Date Conversion:** The Date column must be converted from its current 'object' format to a proper datetime format for accurate monthly trend analysis and time series forecasting.
- **Quantity Cleaning:** The Qty column, currently recognized as 'object', needs to be cleaned and converted to an integer (int64). Initial inspection suggests possible text values ("one," "two") may exist and must be standardized to numeric values before aggregation.
- **Standardization:** Clean and standardize text fields, particularly Gender (e.g., ensuring consistency like 'Women' over 'W') and Category names.

## 3. Tableau Dashboard Plan

The project will deliver two primary, interactive Tableau dashboards:

### 3.1 Dashboard 1: Sales Overview

**Purpose:** Provide a high-level, real-time snapshot of overall business performance.

**Key Performance Indicators (KPIs):** Total Sales, Total Quantity, Total Orders, Average Order Value

**Visuals:**
- **Monthly Sales Trend (Line Chart):** To track seasonality and identify peak/trough months
- **Sales by Category (Bar Chart):** To see which product lines drive revenue (Set, Kurta, Western Dress are top)
- **Profit by State (Map):** To visualize geographic sales concentration
- **Sales by Payment Mode (Bubble/Donut Chart):** To determine channel preference (Amazon, Myntra, Flipkart are top)

**Interactivity:** Filters for Year, Month, Category, and State

### 3.2 Dashboard 2: Customer Insights

**Purpose:** Understand customer demographics, segment purchasing patterns, and identify high-value customer groups.

**Visuals:**
- **Sales by Gender (Pie Chart):** To show the sales contribution split (e.g., Females are the primary revenue driver)
- **Sales by Age Group (Bar Chart):** To identify the highest spending demographic (Working age group is top)
- **Top 10 Customers by Revenue (Horizontal Bar Chart)**
- **State-wise Customer Distribution (Map):** To visualize customer concentration across India

**Interactivity:** Click on Gender or Age Group to filter all other charts dynamically

## 4. Business Questions and Key Findings

The project directly addresses and answers the following strategic questions:

### 4.1 Sales & Profit Trends

- **Seasonality:** March generated the highest revenue, while November saw the lowest
- **Channel Performance:** Myntra, Flipkart, and Amazon are the three most preferred and highest-grossing payment/sales channels

### 4.2 Customer Insights

- **Gender:** Female customers are the primary revenue contributor, accounting for the majority of sales
- **Demographics:** The Working age group spends the most money in Vrinda stores
- **Geographic Loyalty:** Maharashtra and Andhra Pradesh have the most loyal and high-spending customers

## 5. Actionable Recommendations & Implementation Plan

This section translates findings into a clear strategic roadmap for the business.

### 5.1 Marketing Strategy

- **Targeted Advertising:** Shift marketing budgets to heavily target Female customers in the Working age group across the highest-performing channels (Amazon, Myntra, Flipkart)
- **Seasonal Campaigns:** Launch high-impact sales campaigns in traditionally weak months (like November) to smooth out sales troughs and maintain momentum

### 5.2 Geographic Expansion

- **Resource Allocation:** Intensify promotional efforts and potentially consider new store locations in top-performing states like Maharashtra and Andhra Pradesh
- **Market Penetration:** Execute targeted digital marketing campaigns in regions showing low sales but high potential, such as Puducherry and Telangana, to increase brand visibility

### 5.3 Inventory and Product Focus

- **Focus on Winners:** Ensure high stock levels and continuous promotion of the most profitable product categories, which include Sets, Kurtas, and Western Dresses
- **Performance Review:** Launch a deeper profitability review for low-performing categories (like Ethnic Dresses, Blouses, and Bottoms) to determine if they need a marketing boost or should be strategically discontinued to free up working capital
