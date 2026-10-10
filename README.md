# Bank Customer Churn Analysis & Retention Strategy (Excel)

## 📌 Project Overview
This project delivers an end-to-end data analysis of 10,000 banking customers from a European bank to investigate why the bank's customer churn rate is sitting at an alarming **20.37%**. By cleaning, transforming, and visualizing the data entirely within Microsoft Excel, this project identifies critical high-risk segments and translates raw descriptive data into actionable, revenue-saving business recommendations for executive stakeholders.

### 🎛️ Interactive Dashboard Preview
*Replace this text with a high-quality screenshot of your Excel dashboard once uploaded to your repository!*
![Excel Churn Dashboard Layout]

---

## 🛠️ Data Toolkit & Analytics Techniques
* **Data Cleansing & Validation:** Utilized formulas (`COUNTIF`, `COUNTA`, `IF`, `IFS`) to audit 10,000 records for missing values, duplicates, and boundary errors.
* **Feature Engineering:** Developed 3 derived grouping fields (`Age Group`, `Tenure Group`, `Account Balance Group`) to unlock deeper demographic segmentation.
* **Data Modeling:** Built comprehensive Pivot Tables to cross-examine customer profiles against credit scores, balances, and activity rates.
* **Interactive Visualization:** Engineered a dynamic executive dashboard featuring **Interactive Slicers** (`Country`, `Gender`, `Has Credit Card`) to allow stakeholders to drill deep into localized risk factors.

---

## 📊 Key Business Insights & Findings

### 1. High-Level Retention Health
* **Overall Churn Rate:** **20.37%** (Approximately 1 in 5 customers have exited the bank).
* **The High-Value Capital Leak:** Exited customers held an average balance of **\$91,108.54**, which is **\$18,363.24 higher** than customers who stayed. The bank is actively losing its high-liquidity clients.

### 2. Demographic & Behavioral Risk Zones
* **Geographic Spikes:** While the global baseline is 20.37%, filtering by the **Country** slicer reveals that **Germany** is experiencing a staggering **32.44% churn rate**—double that of France (16.15%) and Spain (16.67%).
* **The Inactivity Trap:** Inactive members churned at **26.85%** compared to active members at 14.27%. Lack of engagement is a direct proxy for attrition.
* **The Age Elasticity:** Churn peaks drastically in the **50–59 age bracket at 56.04%**, followed closely by the 40–49 bracket at 30.79%. 

### 3. Product Optimization Anomalies
* **The Sweet Spot:** Customers holding exactly **2 products** demonstrated the strongest loyalty with a remarkably low churn rate of **7.58%**.
* **The Over-Saturation Risk:** Churn rates hit **82.71% for 3 products** and a absolute **100% for 4 products**. While these sample sizes are small, it heavily implies that product over-saturation or aggressive cross-selling correlates with immediate customer exit.

---

## 💡 Strategic Business Recommendations

1. **Re-Engineer Inactive Customer Journeys:** Launch targeted re-engagement initiatives (personalized email marketing, fee waivers, or product education) specifically targeting the inactive segment to bridge the 12.58% churn gap.
2. **Deploy a German Market Taskforce:** Conduct an urgent operational and competitive audit in Germany to isolate why 32.44% of customers are fleeing. Investigate localized competitor offers, app localized reviews, or regional customer service bottlenecks.
3. **Tailor Wealth/Retention Offers for Ages 40–59:** Since this mature demographic represents the highest churn and holds higher average balances, design dedicated high-yield retention accounts or premium customer service perks to protect the bank's liquidity.
4. **Audit Multi-Product Pipelines:** Investigate the onboarding and customer experience for users holding 3 or 4 products. Ensure sales teams are not forcing low-value secondary products that drive severe attrition.

---

## 📂 Repository & Workbook Structure
The underlying Excel workbook is systematically structured across four primary layers:
* `Bank_Churn`: Cleaned base dataset with engineered grouping columns.
* `Churn Analysis`: Aggregated segment computations and baseline counts.
* `Churn Pivot Table`: Dynamic pivot frameworks powering the data cuts.
* `Churn Dashboard`: Visual interface featuring 6 core customer charts and interactive slicers.

```text
Bank-Customer-Churn-Analysis/
├── Cleaned_Data/
│   └── Bank_Churn_Cleaned.xlsx
├── Documentation/
│   └── Bank Customer Churn Analysis.pdf
├── Raw_Data/
│   ├── Bank_Churn.csv
│   ├── Bank_Churn_Data_Dictionary.csv
│   └── Bank_Churn_Messy.xlsx
└── README.md
```
*(Note: File structure reflects portfolio layout; adjust filenames if your active repository files differ.)*

---

## ⚠️ Project Limitations
* **Descriptive Scope:** This analysis is strictly descriptive; it uncovers strong correlations and behavioral patterns but does not establish direct mathematical causality. 
* **Sample Size Constraints:** Micro-segments, specifically the 4-product cluster (60 customers) and the $1–$50k balance tier (75 customers), should be interpreted carefully due to limited variance. Advanced predictive modeling (Logistic Regression) is required to identify true independent churn drivers.

---

## 📋 Dataset Attribution
This project uses the **Bank Customer Churn** dataset provided through the Maven Analytics Data Playground. Maven Analytics identifies the original source as Kaggle and describes the dataset as account information for 10,000 customers at a European bank.

**Source:**
[Maven Analytics Data Playground — Bank Customer Churn](https://mavenanalytics.io/data-playground/bank-customer-churn?utm_source=chatgpt.com)

**Original source credited by Maven Analytics:** Kaggle

This repository is a personal portfolio project for data analysis practice, business intelligence dashboards, strategic insight translation and demonstration of Microsoft Excel skills.

