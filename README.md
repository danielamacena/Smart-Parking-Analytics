# Smart ParkRide Occupancy Analytics Platform

## Project Overview

This project analyzes realtime and historical parking occupancy across Sydney Park&Ride facilities using a modern lakehouse architecture in Databricks.

The solution helps identify parking congestion patterns, high-demand commuter corridors, and parking availability trends to support smarter mobility decisions and reduce unnecessary parking search traffic.

The platform combines realtime API ingestion, historical snapshot accumulation, geospatial analytics, and AI-generated mobility insights to create an intelligent mobility analytics solution.

---

# Realtime Dashboard

<img src="images/realtime_dashboard.png" alt="Realtime Dashboard" width="1000"/>

---

# Historical Trends Dashboard

<img src="images/historical_dashboard.png" alt="Historical Trends Dashboard" width="1000"/>

---

# Business Problem

Commuters often waste time searching for available parking near major transport hubs, especially during peak hours.

Lack of realtime visibility and historical parking intelligence can contribute to:

- Increased traffic congestion
- Longer commuter delays
- Inefficient parking utilization
- Higher vehicle emissions
- Parking overflow into surrounding residential areas

This project aims to improve parking visibility and support smarter commuter decision-making through realtime and historical occupancy analytics.

---

# Solution Overview

The platform ingests realtime occupancy data from the Transport for NSW Park&Ride API and stores historical parking snapshots using a Medallion Lakehouse Architecture.

The solution provides:

- Realtime parking occupancy monitoring
- Historical parking trend analysis
- Facility congestion ranking
- Geospatial parking pressure visualization
- AI-generated mobility insights
- Historical commuter behavior analysis

---

# Architecture

## Medallion Architecture

The project follows a Bronze → Silver → Gold architecture pattern.

```text
Transport for NSW API
            ↓
        Bronze Layer
   Raw Historical Snapshots
            ↓
        Silver Layer
 Normalized Operational Tables
            ↓
         Gold Layer
   Business KPIs & Analytics
            ↓
 Databricks AI Dashboards


---

# Technologies Used

- Databricks
- PySpark
- Delta Lake
- SQL
- Transport for NSW API
- Databricks Dashboards
- Databricks Genie AI
- Medallion Architecture
- Geospatial Analytics

---

# Data Source

Transport for NSW Park&Ride API:

```text
https://api.transport.nsw.gov.au/v1/carpark/full-list
