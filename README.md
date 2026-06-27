 # 📊 Marketing ROI Dashboard

A comprehensive **Marketing ROI Dashboard** project built using **Python, Pandas, and Jupyter Notebook** to analyze marketing performance by combining **web analytics**, **advertising spend**, and **CRM conversion data**. This project helps businesses understand customer behavior, campaign effectiveness, and return on investment (ROI) to make data-driven marketing decisions.

---

## 🚀 Project Overview

Marketing teams often struggle to connect website engagement, advertising costs, and actual conversions. This project integrates multiple datasets to provide insights into the complete marketing funnel:

**Ad Spend → Website Engagement → Lead Conversion**

The dashboard enables analysis of:

* Traffic source performance
* Customer engagement behavior
* Campaign effectiveness
* Conversion outcomes
* Marketing spend efficiency

---

## 🎯 Objectives

* Analyze user engagement from website logs.
* Evaluate advertising performance across channels.
* Examine CRM conversion trends.
* Calculate marketing KPIs such as CTR and CPC.
* Identify high-performing campaigns and traffic sources.
* Support data-driven decision making.

---

## 📂 Dataset Information

The project uses three datasets containing **10,000 records each**.

### 1. Web Analytics Logs (`web_analytics_logs_10k.csv`)

Tracks website user behavior.

**Features:**

* Session ID
* User ID
* Session Date
* Traffic Source
* UTM Source
* UTM Medium
* UTM Campaign
* Device
* City
* Country
* Pages Viewed
* Session Duration (seconds)
* Bounce Flag

---

### 2. CRM Conversion Data (`crm_conversions_10k.csv`)

Captures customer journey and sales outcomes.

**Features:**

* Conversion ID
* User ID
* Lead Date
* Conversion Date
* Lead Stage
* Customer Journey
* Product
* Deal Value
* Country
* City
* Conversion Status

---

### 3. Advertising Spend Data (`ad_spend_10k.csv`)

Contains campaign investment metrics.

**Features:**

* Spend ID
* Date
* Channel
* Campaign
* UTM Source
* UTM Medium
* UTM Campaign
* Impressions
* Clicks
* Ad Spend
* Country

---

## 🛠️ Technologies Used

* Python
* Pandas
* Jupyter Notebook
* NumPy
* Matplotlib
* Git & GitHub

---

## 📋 Data Cleaning Process

### Web Analytics

* Checked missing values.
* Filled missing values in:

  * `utm_campaign`
  * `city`
* Removed duplicate records.
* Verified data types.

The notebook identified approximately **6% missing values** in `utm_campaign` and `city`, which were replaced with `"Unknown"` before analysis. 

---

### Advertising Data

* Filled missing campaign values.
* Filled missing UTM sources.
* Converted dates into datetime format.
* Created additional marketing metrics:

  * CTR
  * CPC

CTR and CPC were calculated using:

```python
ad_spend['ctr'] = ad_spend['clicks'] / ad_spend['impressions']
ad_spend['cpc'] = ad_spend['ad_spend'] / ad_spend['clicks']
```

as shown in the notebook. 

---

## 📈 Exploratory Data Analysis

The project explores:

### Website Analytics

* Traffic source distribution
* Session engagement
* Top sessions by pages viewed
* Bounce behavior
* Device usage patterns

The most frequent traffic channels included:

* Google Ads
* YouTube Ads
* Organic Search
* Email
* Instagram Ads
* LinkedIn Ads
* Facebook Ads

according to the analysis notebook. 

---

### Advertising Performance

Analysis includes:

* Total ad spend by channel
* Click performance
* Campaign comparisons
* Country-wise spend

Example insight:

| Channel        |  Total Spend |
| -------------- | -----------: |
| Organic Search | 7,548,744.59 |
| LinkedIn Ads   | 7,387,917.12 |
| YouTube Ads    | 7,369,202.58 |
| Google Ads     | 7,356,371.49 |

from the notebook outputs. 

---

### CRM Conversion Analysis

Insights include:

* Lead stage distribution
* Conversion status analysis
* Product performance
* Customer journey patterns
* Revenue trends

---

## 📊 Key Performance Indicators (KPIs)

The dashboard focuses on:

* Total Sessions
* Total Ad Spend
* Total Clicks
* Average Session Duration
* Bounce Rate
* Conversion Rate
* Cost Per Click (CPC)
* Click Through Rate (CTR)
* Total Revenue
* Average Deal Value
* Top Performing Channels

---

## 📁 Project Structure

```
Marketing_ROI_Dashboard/
│
├── dataset/
│   ├── web_analytics_logs_10k.csv
│   ├── crm_conversions_10k.csv
│   └── ad_spend_10k.csv
│
├── project1.ipynb
├── README.md
└── requirements.txt
```

---

## ▶️ How to Run the Project

### Clone the Repository

```bash
git clone https://github.com/yourusername/Marketing_ROI_Dashboard.git
cd Marketing_ROI_Dashboard
```

### Install Dependencies

```bash
pip install pandas numpy matplotlib jupyter
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```bash
project1.ipynb
```

and run all cells.

---

## 💡 Business Impact

This project demonstrates how marketing data from multiple sources can be integrated to answer critical business questions:

* Which channels drive the highest engagement?
* Which campaigns generate the best ROI?
* What customer journeys lead to conversions?
* How can marketing budgets be optimized?

The resulting insights help organizations improve campaign efficiency and maximize returns on marketing investments.

---

## 🎯 Attribution Modeling

Traditional marketing reporting often assigns all conversion credit to the final interaction before purchase. This project extends beyond basic ROI analysis by implementing Multi-Touch Attribution Models.

### Attribution Models

#### First-Touch Attribution
Assigns 100% conversion credit to the first customer interaction.

Example:
Google Ads → Email → Direct → Purchase

Credit:
Google Ads = 100%

---

#### Last-Touch Attribution
Assigns 100% conversion credit to the final interaction before conversion.

Example:
Google Ads → Email → Direct → Purchase

Credit:
Direct = 100%

---

#### Linear Attribution
Distributes conversion credit equally across all touchpoints.

Example:
Google Ads → Email → Direct → Purchase

Credit:
Google Ads = 33.3%
Email = 33.3%
Direct = 33.3%
⭐ If you found this project useful, consider giving it a **star** on GitHub!

## 🗺️ Project Roadmap

### Week 1
- Data Cleaning
- Data Profiling
- EDA
- KPI Development

### Week 2
- SQL Data Warehouse
- Customer Journey Sequencing
- First-Touch Attribution
- Last-Touch Attribution
- Linear Attribution

### Week 3
- Star Schema Design
- CAC Calculation
- ROAS Calculation
- Revenue Attribution

### Week 4
- Power BI Dashboard Development
- Executive Reporting
- Marketing Performance Analysis

## 🗄️ SQL Concepts Used

- INNER JOIN
- LEFT JOIN
- Window Functions
- ROW_NUMBER()
- PARTITION BY
- Common Table Expressions (CTEs)
- Customer Journey Sequencing
- Attribution Logic

## 📊 Dashboard Deliverables

The final dashboard will contain:

1. Executive Overview
2. Marketing Spend Analysis
3. Campaign Performance
4. Attribution Comparison
5. Customer Journey Analysis
6. Conversion Funnel
7. Geographic Insights
8. ROI & ROAS Analysis

## 📈 Advanced Marketing KPIs

- Total Spend
- Total Revenue
- CTR
- CPC
- CAC
- Conversion Rate
- ROAS
- ROI
- Revenue per Campaign
- Revenue per Channel
- Attribution Revenue
- Funnel Conversion %


Final repo or folder structure after week 4
Marketing_ROI_Dashboard/

├── dataset/
├── project1.ipynb
├── sql/
│   ├── schema.sql
│   ├── attribution.sql
│   └── kpis.sql
├── powerbi/
├── README.md
└── requirements.txt
