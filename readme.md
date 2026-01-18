# 🏦 Bank Loan Report Analysis & Prediction

This personal project provides a comprehensive end-to-end analysis of bank loan data. It covers everything from data extraction using **SQL**, UI/UX planning in **Figma**, interactive data visualization in **Tableau**, to advanced **Machine Learning** modeling for predicting loan defaults.

---

## 🎨 Design & Data Engineering

### 🏗️ UI/UX Mockup
Before building the final dashboards, I designed a high-fidelity mockup to plan the user interface and ensure a data-driven user experience.
> 🔗 **[View Figma Mockup](https://www.figma.com/design/Kvj4PV436srQCQcprUef5i/Mock-Up-Dashboard-Bank-Loan)**

### 💾 SQL Query Analysis
I performed extensive data extraction and KPI calculation using SQL to ensure data integrity and accuracy. The analysis includes:
* **Key Performance Indicators (KPIs):** Total applications, funded amounts, and payments received (MTD/QTD trends).
* **Loan Categorization:** Segmenting "Good Loans" vs. "Bad Loans" based on repayment status.
* **Data Aggregation:** Regional and temporal analysis of loan distributions.

---

## 📊 Tableau Business Dashboards

I developed three interactive dashboards in **Tableau** to monitor portfolio health and identify trends. The visualizations are designed for both high-level executive overviews and granular data exploration.

### 1. Summary Dashboard
Tracks core metrics like total loan applications, funded amounts, and interest rates to monitor the overall health of the lending portfolio.
![Dashboard 1 - Summary](Dashboard%201%20-%20Summary.png)

### 2. Overview Dashboard
Provides a breakdown of loan distributions by *Grade*, *Term*, and *Home Ownership* to identify risk concentrations.
![Dashboard 2 - Overview](Dashboard%202%20-%20Overview.png)

### 3. Details Dashboard
Allows for a deep-dive into individual loan records with specific filters for granular analysis.
![Dashboard 3 - Details](Dashboard%203%20-%20Details.png)

---

## 🧩 Key Exploratory Insights

My analysis revealed several critical factors that influence the likelihood of a loan default:

* **DTI (Debt-to-Income):** Borrowers with a DTI between 0.25 – 0.30 show a significantly higher risk profile.
* **Credit Grade:** Lower grades (F & G) have a higher default proportion compared to premium grades (A & B).
* **Loan Term:** 60-month loans are more prone to default than 36-month loans due to the longer commitment period.
* **Home Ownership:** Renters (RENT) tend to have higher default rates compared to homeowners (MORTGAGE/OWN).

---

## 🤖 Modeling Approach

To predict loan outcomes, I implemented 6 different algorithms. To address class imbalance in the dataset, I utilized a **Pipeline + SMOTE** (Synthetic Minority Over-sampling Technique).

* **Logistic Regression** 📈: Baseline model for interpretability.
* **Decision Tree & Random Forest** 🌳: Explored tree-based decision paths.
* **SVM** ⚡: Robust for non-linear data separation.
* **XGBoost & LightGBM** 🔥: High-performance gradient boosting frameworks.
* **Multi-Layer Perceptron (MLP)** 🤖: A deep learning approach for capturing complex patterns.

---

## 🏆 Evaluation Results (Test Set)

The performance of the models on the unseen test set is summarized below:

| Model | Accuracy | ROC-AUC |
| :--- | :---: | :---: |
| **XGBoost** 🔥 | **97.40%** | **0.9814** |
| **LightGBM** 🌟 | 97.37% | 0.9808 |
| **SVM** ⚡ | 96.72% | 0.9746 |
| **Decision Tree** 🌳 | 94.98% | 0.9169 |
| **Random Forest** 🌲 | 93.81% | 0.9452 |
| **Logistic Regression** 📈 | 93.52% | 0.9634 |



> **Conclusion:** **XGBoost** was selected as the final production model due to its superior accuracy and ability to generalize without overfitting.

---

## 🛠️ Strategic Recommendations

* **Risk Filtering:** Apply strict **DTI** thresholds (max 0.25) and minimum **Income** requirements during the initial screening.
* **Term Optimization:** Limit the availability of **60-month terms** for borrowers in lower grade categories (E, F, G).
* **Scoring Integration:** Include **Home Ownership** and **Credit Grade** as primary weights in the internal credit scoring engine.
* **Pricing Strategy:** Adjust interest rates for high-risk segments to compensate for the higher probability of default identified in the model.

---

## 💻 Technical Stack

* **Database:** SQL (SQL Server)
* **Design:** Figma
* **Visualization:** Tableau
* **Programming:** Python (Pandas, NumPy, Scikit-learn, XGBoost, LightGBM, Matplotlib, Seaborn)
* **Environment:** Jupyter Notebook / VS Code