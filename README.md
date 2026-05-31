# 🎓 SDG 4: Quality Education — Inferential Analytics & Dashboard
### *A Cross-National Analysis on the Socioeconomic Drivers of Global Educational Attainment (2000–2023)*

---

## 📌 Project Overview
This repository contains a comprehensive data mining project that investigates the structural forces shaping global education outcomes. Grounded in the **CRISP-DM framework**, the study transitions from raw data engineering to inferential statistical modeling, culminating in a public-facing interactive web application.

👉 **Live Interactive Dashboard:** [https://sdg-nicolas--dashboard.streamlit.app/](https://sdg-nicolas--dashboard.streamlit.app/)

---

## 🎯 1. Problem Definition
Following the required analytical framework, this project addresses the core research question:
> **"What factors influence UN SDG 4 (Quality Education) across countries over time?"**

### Research Scope
* **Response Variable ($Y$):** Educational Attainment Index (Mean/Expected Years of Schooling).
* **Objective:** Move beyond basic descriptive charts to isolate true structural drivers, controlling for economic scale, infrastructure availability, gender demographics, and state allocations.

---

## 📊 2. Data Collection & Sources
The analytical dataset profiles a robust panel of **191 countries over a 24-year horizon (2000–2023)**. To construct a reliable data matrix, primary indicators were extracted and merged from premier international institutions:
1. **Our World in Data (OWID):** Core learning outcomes and literacy baseline indicators.
2. **The World Bank Open Data:** National macro-financial indicators and demographic metrics.
3. **UNESCO Institute for Statistics (UIS):** Public education expenditures and standardized completion indices.
4. **International Labour Organization (ILO):** Youth workforce participation and equity distributions.

---

## 🛠️ 3. Data Preparation Pipeline
Before modeling, raw data underwent a rigorous cleaning pipeline within Jupyter Notebook to guarantee statistical integrity:
* **Handling Missing Data:** Addressed unbalanced panels by executing a localized **Linear Interpolation** for country-specific series, supplemented by **Year-Median Imputation** for systemic regional data gaps.
* **Feature Transformation:** Applied mathematical **Logarithmic Transformations** to skewed distribution features (such as Log GDP per Capita) to satisfy linearity assumptions.
* **Feature Engineering:** Compiled independent indicators into an integrated, standardized panel dataset matching ISO-3 country codes across consistent time cycles.

---

## 🔬 4. Regression Analysis & Modeling
The inferential modeling was completely executed using Python's `statsmodels` library to isolate key drivers while adhering to classical statistical assumptions.

### Exploratory Data Analysis & Diagnostics
* **Multicollinearity Checks:** Assessed variance inflation boundaries. High-dimensional variables were pruned until all remaining features achieved a **Variance Inflation Factor (VIF) < 5**.
* **Assumption Testing:** Heavy-tailed residual distributions and extreme cross-national leverage points violated standard Ordinary Least Squares (OLS) assumptions. 
* **Model Selection:** To compensate for non-normal error distributions and cross-border outliers, an outlier-resilient **Huber-T Robust Linear Model (RLM)** was deployed.

### Variables & Literature Justification
* **National Wealth (Log GDP per Capita):** Supported by classic human capital theory (Schultz/Becker), confirming macro-wealth dictates state infrastructure investments.
* **Digital Access (Internet Usage %):** Supported by contemporary digital divide literature, tracking how modern educational access requires robust telecommunication pipelines.
* **Workforce Gender Equity & Public Spending:** Integrated as key socioeconomic covariates reflecting institutional progress.

### Core Model Findings
* The robust framework evaluated global trends as highly significant ($p < 0.001$), explaining **83.6% ($R^2 = 0.836$)** of global variance in educational attainment.
* **Key Drivers Identified:** **National Wealth** ($\beta = +1.866$) and **Digital Access** ($\beta = +0.932$) emerged as the dominant structural drivers accelerating global education progress.

---

## 🖥️ 5. Interactive Dashboard Architecture
To communicate these insights to stakeholders, the underlying data pathing was integrated into an open-access web dashboard built via **Streamlit** and **Plotly**.

### Dashboard Features
* **Time-Based Global Filter:** Features a dynamic synchronized year-slider (2000–2023) that re-renders all on-screen elements on user change.
* **Dynamic KPIs:** Real-time summary banners showing global educational health metrics relative to the chosen period.
* **Cross-Country Comparison:** Interactive geospatial choropleth heatmaps and comparative rank charts allowing users to drill down into country-specific performance versus global baselines.
* **UI Design:** Designed in an intuitive dark-mode interface optimized for scannability and professional presentation.

---

## 💻 Author & Course Identity
* **Student Researcher:** Sheikha Maris Nicolas
* **Course Section:** BSIS 3B
* **Subject:** Business Analytics
