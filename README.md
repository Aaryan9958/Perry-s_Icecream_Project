# Project Boost – Production & Operations Analytics for Perry’s Ice Cream

## Overview
**Project Boost** is an end-to-end production and operations analytics project conducted for **Perry’s Ice Cream** in collaboration with **Simon Business School, University of Rochester**.  
The objective was to identify how Perry’s could **safely increase plant output using existing equipment, labor, and operating hours**, without compromising reliability.

The project analyzes real production data across multiple work centers, products (SKUs), and time periods to uncover **hidden capacity losses, operational inefficiencies, and data-backed improvement opportunities**.

---

## Business Problem
Perry’s operates a complex manufacturing environment with multiple production lines, diverse SKUs, and varying operational conditions. While the plant is reliable, leadership needed clarity on:

- Where is production time being lost?
- Which lines can safely run faster?
- How do product characteristics affect throughput?
- What targeted actions can increase total output without increasing downtime?

---

## Key Outcomes & Impact
- Identified that **downtime, not running speed**, is the primary driver of lost throughput
- Quantified **16–31% throughput headroom** across production lines at optimal speeds
- Modeled a scenario delivering **+7.4 million units (+22%)** in output with only **+0.1 pp change in downtime**
- Built a **SKU clustering framework** to support smarter line routing and scheduling
- Delivered a **line-specific optimization roadmap**, avoiding one-size-fits-all speed increases

---

## Analytical Approach
The analysis followed a structured, consulting-style workflow:

### 1. Exploratory Data Analysis (EDA)
- Compared throughput, uptime, downtime, efficiency, and variability across all WorkCenters
- Demonstrated that **uptime and efficiency move together**, confirming stop elimination as the main lever
- Identified stability vs. volatility patterns by line

### 2. Regression Analysis (Mechanical Capability)
- Built a True Speed regression model (R² ≈ 0.91) to isolate machine capability
- Quantified the impact of:
  - WorkCenter design differences
  - Product weight (≈ −3.5 units/min per additional lb)
  - Run duration (no impact on mechanical speed)
- Established a clean baseline for machine performance under controlled conditions

### 3. Time Series Analysis
- Converted run-based logs into **continuous hourly performance**
- Revealed:
  - Weekly fatigue patterns
  - Hour-of-day performance rhythms
  - Ramp-up losses and recurring breakdown signatures
- Identified systemic vs. acute capacity losses using statistical and autoregressive methods

### 4. SKU Clustering (K-Means)
- Grouped SKUs into **four performance clusters** based on:
  - Speed
  - Uptime / downtime
  - Run duration
  - Weight
- Enabled clearer separation of **SKU-driven vs. line-driven** performance issues
- Created a practical framework for production planning and routing

### 5. Optimal Speed Simulation
- Modeled throughput as a function of speed and uptime for each line
- Identified **line-specific “sweet spots”** where throughput is maximized
- Demonstrated that **selective speed tuning**, not blanket increases, unlocks capacity safely

---

## Tools & Technologies
- **Python** (pandas, numpy, statsmodels, scikit-learn, matplotlib)
- **Statistical Modeling** (OLS regression, correlation analysis)
- **Machine Learning** (K-Means clustering, XGBoost for predictive modeling)
- **Time Series Analysis** (resampling, autoregression, anomaly detection)
- **Data Visualization** (Python plots, dashboards)
- **Excel & PDF Reporting** for stakeholder-ready outputs

---

## Repository Structure
├── code/ Data cleaning, EDA, regression, clustering, simulations
├── reports/ Final report and executive summaries
├── dashboard/ # Slide Deck and visuals
├── README.md
└── requirements.txt

---

## Confidentiality Note
Due to client confidentiality, **raw production data is not included** in this repository.  
All code, methodology, visuals, and results are shared for demonstration of analytical approach and problem-solving depth.

---

## Why This Project Matters
This project mirrors real-world **manufacturing analytics, operations consulting, and supply chain optimization** work.  
It demonstrates the ability to:
- Translate complex data into executive-level insights
- Balance throughput, reliability, and operational risk
- Design analytics that drive **practical, implementable decisions**

---

## Next Steps
Future extensions could include:
- Live monitoring dashboards for supervisors
- Integration with maintenance logs for root-cause tracking
- Automated speed recommendations by SKU and shift
