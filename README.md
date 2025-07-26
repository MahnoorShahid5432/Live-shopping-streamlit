# LiveShoppingAnalytics

A real-time analytics dashboard built to help brands unlock insights during live shopping streams. This project captures and models live engagement data to segment customers, predict conversions, and surface actionable metrics that improve digital commerce performance.

---

## 🎯 Purpose

Live shopping is redefining how consumers engage with brands—but most businesses lack the tools to act on that engagement in real time. This project bridges that gap by offering a complete analytics workflow, from event capture to customer segmentation and predictive modeling.

---

## 🏗️ System Design

**🔹 Real-Time Data Simulation & Ingestion**
- Simulated streaming data (views, clicks, purchases) is generated via Python.
- Events are sent to **Google Pub/Sub** and ingested into **BigQuery** for storage and processing.

**🔹 Data Transformation with dbt**
- `fct_sessions`: Processes raw session data  
- `rfm_analysis`: Calculates Recency, Frequency, and Monetary value  
- `train_customer_segments`: Performs K-Means clustering via **BigQuery ML**  
- `customer_segments_named`: Maps clusters to meaningful customer types

**🔹 Predictive Modeling**
- Predicts conversion probability at the session level  
- Outputs high-intent segments and lag-based engagement signals

---

## 📊 Dashboard Insights (via Streamlit)

A lightweight UI built in **Streamlit** for visualizing and interacting with real-time KPIs:

- Total Sessions & Unique Viewers  
- Drop-Off Analysis & Average Session Duration  
- Click-to-Purchase Lag  
- Conversion Probability (model-based)  
- Viewer Engagement Score  
- RFM-Based Customer Segments (e.g., “High-Value Loyal”)

Includes dynamic filters by:
- Viewer ID  
- Device Type  
- Location  

---

## 🚀 Deployment

- File: `streamlit_app.py`  
- Backend: Queries handled using `google.cloud.bigquery`  
- Hosted via **Streamlit Cloud** (auto-deploy from GitHub on push)

---

## 🧰 Tech Stack

| Component       | Tool                     |
|----------------|--------------------------|
| Data Streaming | Google Pub/Sub           |
| Data Warehouse | BigQuery                 |
| Modeling       | BigQuery ML              |
| Transformation | dbt                      |
| Visualization  | Streamlit Cloud          |

---

## 👩‍💻 Project Status

✅ MVP Complete  
🔜 Next: Integrate real-time feedback loop for content adaptation  
📦 Data simulation scripts & queries included

---
<div style="margin-top: 40px; text-align: center; font-family: Arial, sans-serif;">
  <h3 style="color: #333;">Contributors</h3>
  <ul style="list-style: none; padding: 0; font-size: 16px;">
    <li>Jeena Woo</li>
    <li>Kaylyn Nguyen</li>
    <li>Rimsa Shrestha</li>
    <li>Sarah (Xiangwen) Xiong</li>
  </ul>
</div>


*Built to help brands personalize live commerce in real time.*  
