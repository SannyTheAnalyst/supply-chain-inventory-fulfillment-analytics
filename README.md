# Supply Chain Inventory & Order Fulfillment Analytics

## Overview
This project demonstrates an end-to-end **supply chain inventory and order fulfillment analytics model** built to evaluate service performance, inventory health, and replenishment effectiveness across multiple distribution centers.

The objective is to analyze **fill rate, backorder risk, and on-time delivery performance** using realistic operational data, simulating challenges commonly faced in aerospace, manufacturing, and regulated supply chain environments.

---

## Business Problem
Organizations operating complex supply chains must balance:
- Inventory availability vs. carrying cost
- Customer service levels vs. supplier lead times
- Demand variability vs. replenishment planning

This project addresses the following questions:
- Which items and locations are driving backorders?
- How effectively are customer orders being fulfilled?
- Where do inventory positioning and lead-time constraints impact service performance?
- How can supply chain KPIs be used to identify operational risk?

---

## Data Model & Scope
The dataset was designed to reflect **realistic enterprise-scale supply chain operations**.

### Scope
- **90 days** of daily inventory snapshots
- **3 distribution centers**
- **220 stocked items** across multiple categories
- **10 suppliers** with varying lead times and reliability
- **420 customer sales orders**
- **1,200+ sales order lines**
- **260 purchase order lines**

### Core Tables
- `dim_item` – Item master data (category, cost, criticality)
- `dim_location` – Distribution centers
- `dim_supplier` – Supplier lead times and performance
- `fact_inventory_snapshot` – Daily on-hand, allocated, and on-order inventory
- `fact_sales_order` / `fact_sales_order_line` – Customer demand and fulfillment
- `fact_purchase_order_line` – Replenishment activity

The model follows a **star-schema design**, optimized for analytics and BI reporting.

---

## Key KPIs Analyzed
- **Fill Rate (%)** – Shipped quantity ÷ ordered quantity
- **Backorder Rate (%)** – Backordered quantity ÷ ordered quantity
- **On-Time Shipment (%)** – Orders shipped on or before required date
- **Inventory Availability** – On-hand minus allocated quantity
- **Reorder Risk Indicators** – Inventory vs. reorder point and safety stock

These KPIs are calculated using SQL views and visualized in Power BI.

---

## Key Insights
- Service performance is constrained by **inventory positioning and lead-time variability**
- Certain item categories consistently contribute to **higher backorder rates**
- Priority orders (urgent/AOG) achieve higher on-time shipment rates but increase pressure on inventory
- Replenishment timing and supplier lead time directly affect fulfillment outcomes

The results highlight how **data-driven inventory planning and exception monitoring** can improve service levels.

---

## Tools & Technologies
- **SQL Server** – Data modeling, transformation, KPI calculations
- **Power BI** – Dashboarding and performance visualization
- **Git & GitHub** – Version control and project documentation
- **Excel / CSV** – Data validation and exports (optional)

---

## How This Project Is Relevant
This project mirrors real-world responsibilities found in **Supply Chain Specialist and Operations Analyst roles**, including:
- Inventory monitoring and control
- Order fulfillment tracking
- KPI reporting and performance analysis
- Cross-functional decision support using data

It demonstrates the ability to translate **raw operational data into actionable supply chain insights**.

---

## Repository Structure
