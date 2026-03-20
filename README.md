# AQI-Analytics-Market-Intelligence-Pipeline-for-Air-Purifier-Industry
End-to-End AQI Analytics &amp; Market Intelligence Pipeline for Air Purifier Industry. Built Databricks Medallion pipeline with CDC (MERGE/UPSERT), orchestrated data via ADLS &amp; ADF to Azure SQL, and developed a Power BI solution with DAX. Created a risk model (AQI + population + health) to identify demand, seasonality, and growth opportunities.

# 🌍 End-to-End AQI Analytics & Market Intelligence Pipeline  
### *For the Air Purifier Industry*

---

## 📌 Project Overview  

Air pollution is not just an environmental issue — it’s a **data problem with direct business implications**.  

This project transforms **AQI, health, vehicle, and population data** into **actionable market intelligence** for the air purifier industry. Instead of just analyzing pollution levels, the focus is on:

- Where is the **actual demand**?  
- Which regions are **high-risk but underpenetrated**?  
- When does demand **peak seasonally**?  
- How can companies **optimize strategy using data**?  

The solution combines **data engineering + analytics + business decision-making** in a complete pipeline.

---

## 🏗️ Architecture Overview  

**Databricks → ADLS → Azure Data Factory → Azure SQL → Power BI -> Python EDA and Analysis -> Reporting and Insights -> Decisions**

This architecture ensures:
- Scalable data processing  
- Automated data movement  
- Centralized analytics layer  
- Efficient BI reporting  

---

## ⚙️ Databricks (Data Engineering Layer)

Built using **Medallion Architecture (Bronze → Silver → Gold)**

### 🔹 Key Work:
- Ingested raw datasets (AQI, health, vehicles, population)  
- Performed large-scale data cleaning and transformation using **PySpark, SQL & Python**  
- Structured pipeline into:
  - **Bronze** → Raw ingestion  
  - **Silver** → Cleaned & standardized data  
  - **Gold** → Aggregated, analytics-ready Fact & Dimension tables  
- Implemented **incremental loading** using:
  - `MERGE INTO`  
  - UPSERT logic  
- Ensured schema consistency and optimized transformations  

### 📂 Files Included:
- `Source.ipynb` → Data ingestion  
- `Bronze.ipynb` → Raw processing  
- `Silver.ipynb` → Cleaning & transformations  
- `Gold.ipynb` → Aggregated tables  

---

## ☁️ Azure (Data Movement, Orchestration & Storage)

### 🔹 Key Work:
- Moved curated **Gold layer data → ADLS**  
- Built **Azure Data Factory pipelines** to:
  - Dynamically fetch files  
  - Automate ingestion workflows  
  - Load processed data into **Azure SQL Database**  
- Designed and maintained **Azure SQL as a centralized analytical data store**, enabling efficient querying and seamless integration with Power BI  
- Implemented **parameterized pipelines** for reusable and scalable data ingestion  
- Configured **triggers for automated pipeline execution**  
- Enabled **monitoring and alerting with automated email notifications** upon successful pipeline runs  
- Established a **reliable data flow from engineering layer to BI layer**, ensuring data consistency and availability  

### 📂 Files Included:
- ADF pipeline JSON templates
- Screenshots  
- Linked service configurations  
- Architecture diagram (PDF) 

---

## 📊 Power BI (Analytics & Visualization)

### 🔹 Key Work:
- Connected **Azure SQL → Power BI**  
- Analyzed & verified the previously built (in databricks) structured **data model (fact + dimension tables)**  
- Created **DAX measures** for:
  - AQI trends  
  - Exposure risk  
  - Health impact correlation  
  - Regional demand patterns
  - Risk Score, etc. 
- Designed **interactive dashboards** for:
  - State-wise & city-wise insights  
  - Risk segmentation  
  - Market opportunity analysis  

### 🔍 Analytical Approach:
- **Time-Series Analysis** → Identified seasonal AQI patterns and demand peaks (Nov–Jan)  
- **Exposure-Based Risk Analysis** → Modeled pollution risk using AQI, population, and health data to identify high-demand regions  
- **Segmentation Analysis** → Classified regions into high vs low exposure and demand clusters  
- **Comparative Analysis** → Evaluated AQI trends against vehicle growth and health impact to uncover multi-factor pollution drivers  
- **Geospatial Analysis** → Identified high-risk states and non-metro/industrial hotspots for targeted market expansion  
- **Demand Opportunity Analysis** → Detected underpenetrated high-exposure regions for strategic market entry  
- **Monitoring vs Awareness Analysis** → Compared AQI levels with monitoring infrastructure to distinguish high-awareness vs low-awareness markets  

### 📂 Files Included:
- `AQI_Analysis.pbix` → Power BI dashboard  
- Dashboard pdf 
- Data model images  

---

## 🐍 Python EDA & Data Preparation

Before final visualization, performed **Exploratory Data Analysis (EDA)** and additional cleaning using Python to support deeper analytical insights.

### 🔹 Key Work:
- Handled missing values and inconsistencies  
- Performed grouping and aggregation for trend analysis  
- Validated relationships between AQI, health, and population  
- Prepared structured datasets for Power BI consumption  

### 📂 Files Included:
- `EDA.ipynb` → Exploratory Data Analysis notebook  

---

## 🧠 Analytics & Business Insights  

This project focuses on **decision-making, not just visualization**.

### 🔹 Key Insights:
- Air pollution is **structural**, not occasional → sustained demand  
- **Exposure (population + health)** is a stronger demand driver than AQI alone  
- High-risk regions extend beyond metros → **Tier-2/3 & industrial areas**  
- AQI shows strong **seasonal patterns** → predictable demand cycles  

### 🔹 Strategic Outcomes:
- Enabled **data-driven geographic targeting**  
- Identified **underpenetrated high-potential markets**  
- Supported **seasonal marketing optimization (winter peak demand)**  
- Designed **dual-market strategy**:
  - Premium → High-awareness regions  
  - Affordable → Low-awareness, high-risk areas  
- Highlighted **institutional expansion opportunities** (schools, hospitals, offices)  

👉 Result:
- Improved **market penetration strategy**  
- Optimized **resource allocation**  
- Enabled **revenue-focused decision-making**  

---

## 📄 Documentation  

Detailed analysis and business recommendations are documented in:

### 📂 Files Included:
- `Air Pollution Risk & Market Opportunity Analysis.pdf`  
- Supporting visuals and charts  

---

## 🚀 Key Highlights  

- End-to-end pipeline (**Databricks → Azure → Power BI**)  
- Real-world datasets with scalable architecture  
- Strong focus on **analytics + business impact**  
- Combines **Data Engineering + Data Analysis + Strategy**  

---

## 🛠️ Tech Stack  

- **Databricks (PySpark, SQL)**  
- **Python (Pandas, Matplotlib, Seaborn)**  
- **Azure Data Lake Storage (ADLS)**  
- **Azure Data Factory (ADF)**  
- **Azure SQL Database**  
- **Power BI (DAX, Data Modeling, Reporting)**  

---

## 💡 Final Note  

This project demonstrates how raw environmental data can be transformed into **actionable market intelligence**.  

The core focus was:
> *Using data to drive real business decisions, not just dashboards.*

---
