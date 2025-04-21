# Chelsea FC Performance Insights Vizathon

The Chelsea FC Performance Monitoring Dashboard — a data-driven sports science project built for the **Chelsea FC Vizathon**. 
This project is designed to bridge the gap between raw GPS/recovery data and real-time performance insights, giving coaches and practitioners a clear, digestible view of an athlete's physical state.

---

## Project Ains

The primary aim of this project was to develop my skills in:
- Data processing using **Python**
- Transforming complex metrics into **meaningful performance insights**
- Creating an engaging and actionable **Tableau dashboard**
- Exploring machine learning for **predictive performance analytics**

I wanted to challenge myself to turn raw physical performance data into something that is:
- Easily interpretable
- Visually compelling
- Valuable for daily training decision-making

---

## Data Processing

This project brings together multiple performance data sources provide by the Chelsea Insights team for this vizathon:
- **GPS metrics** — external physical load (e.g., total distance, HSR, Accels/Decels)
- **Recovery scores** — internal readiness signals derived from EMBOSS composite metrics
- **Testing data** — movement benchmarks and top speed profiling
- **Player Priority data** — the players current aims. e.g. different performance scores or nutrtional aims.

**Data Modelling**
- Calculating **EWMA (7-day)** and **28-day rolling averages** to assess acute-chronic workloads
- Creating flags such as:
  - `Readiness to Perform` (based on load spikes, recovery scores / flags, peak speed)
  - `Injury Risk Score` (a weighted score from multiple fatigue indicators)
- Predicting future values (next-day recovery and session load) using machine learning:
  - Random Forest Regressor & Classifier models
  - Metrics Added to dashboard as proof of concept

---

## Dashboard Overview

[**View the Tableau Dashboard**](https://public.tableau.com/views/PhysicalMonitoringinSoccer-ChelseaFCInsightsVizathon/CFCPhysicalMonitoring?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

The Tableau dashboard is structured into 4 key areas to help coaches and performance staff **quickly understand an athlete’s physical status and guide prescription**:

### 1. Calendar Carousel
Provides an at-a-glance summary of the player’s last 4 and next 3 days, including; Match days (opposition logos), Training sessions, Recovery days and Match Day labels (MD–2, MD0, MD+1, etc).

### 2. Acute Chronic Workload Trends
Three key metrics (Total Distance, HSR, Accel/Decel) are visualised as:
- 7-day EWMA vs 28-day average
- Deltas expressed as % change
- Categorised into zones: Elevated, Moderate, Balanced, Reduced
- Visualised with trended bars and KPI BANs

### 3. Readiness to Perform & Injury Risk Section
- Readiness Flag based on load, top speed, and recovery state
- Injury Risk Score from combined penalties across multiple metrics
- Designed for quick daily decision-making

### 4. Predictive Modelling Outputs
- Predicted next-day recovery score
- Predicted session total distance
- Based on trained machine learning models using historical load and recovery data

