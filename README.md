# 🎓 SDG 4 — Quality Education Dashboard Analysis
### *Investigating the Socioeconomic Drivers of Global Educational Attainment (2000–2023)*

---

## 📌 Project Overview & Core Questions Answered
Using the CRISP-DM framework, this project answers the critical analytics questions regarding **UN SDG 4: Quality Education** by analyzing a dense panel dataset of 191 countries (2000–2023) sourced from Our World in Data, the World Bank, UNESCO, and the ILO. 

By executing data cleaning (linear interpolation, year-median imputation, and log-transformations) and deploying an outlier-resilient **Huber-T Robust Linear Model** via Python’s `statsmodels`, the project addresses these primary questions:

1. **What macro-level forces actually impact global education?** The model evaluates global trends to prove that institutional factors significantly dictate national schooling outcomes.
2. **What are the primary drivers of educational attainment?** The analysis identifies **National Wealth (GDP per Capita)** and **Digital Access (Internet Usage %)** as the most dominant structural drivers accelerating years of schooling.

👉 **Live Dashboard Application:** [https://sdg-nicolas--dashboard.streamlit.app/](https://sdg-nicolas--dashboard.streamlit.app/)

---

## 💻 Author & Course Identity
* **Student Researcher:** Sheikha Maris Nicolas
* **Course Section:** BSIS 3B
* **Subject Focus:** Data Mining / Business Analytics Project Submission
