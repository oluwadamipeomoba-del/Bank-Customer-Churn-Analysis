# Bank Customer Churn Analysis — Excel

A customer churn analysis project using Microsoft Excel to identify customer segments associated with higher churn and translate the findings into actionable business insights.

## Project Overview

This project analyses customer churn within a dataset of 10,000 customers from a European bank.

The objective was to:

* Validate and assess the quality of the customer dataset.
* Calculate the overall customer churn rate.
* Identify customer segments with higher or lower churn.
* Explore relationships between churn and customer characteristics.
* Create visualisations to communicate key findings.
* Translate analytical findings into practical business recommendations.

The analysis was completed using **Microsoft Excel**.

---

## Dataset

**Dataset:** Bank Customer Churn
**Records:** 10,000 customers
**Original fields:** 13
**Data type:** Customer account information
**Source:** Maven Analytics Data Playground
**Original source credited by Maven Analytics:** Kaggle

Maven Analytics describes the dataset as account information for 10,000 customers at a European bank, covering characteristics such as credit score, balance, products and customer churn status.

**Dataset source:**
[Maven Analytics — Bank Customer Churn](https://mavenanalytics.io/data-playground/bank-customer-churn?utm_source=chatgpt.com)

---

## Dataset Fields

The original dataset contains the following 13 fields:

| Field           | Description                              |
| --------------- | ---------------------------------------- |
| CustomerId      | Unique customer identifier               |
| Surname         | Customer surname                         |
| CreditScore     | Customer credit score                    |
| Geography       | Customer country                         |
| Gender          | Customer gender                          |
| Age             | Customer age                             |
| Tenure          | Number of years with the bank            |
| Balance         | Customer account balance                 |
| NumOfProducts   | Number of banking products held          |
| HasCrCard       | Whether the customer has a credit card   |
| IsActiveMember  | Whether the customer is an active member |
| EstimatedSalary | Estimated customer salary                |
| Exited          | Customer churn status                    |

For analysis, the workbook also includes derived fields such as **Age Group, Tenure Group, and Account Balance Group**.

---

## Data Quality & Validation

Before analysing churn, the dataset was reviewed for common data-quality issues.

### Missing Values

All 13 original columns were checked for blank values.

**Result:** No missing values were identified.

**Action:** No changes were required.

### Duplicate Records

Customer IDs and records were checked for duplicates.

**Result:** No duplicate customer IDs or duplicate records were identified.

**Action:** No records were removed.

### Categorical Validation

The following categorical fields were reviewed:

* Geography
* Gender
* Has Credit Card
* Is Active Member
* Exited

Geography contained only:

* France
* Spain
* Germany

Gender contained only:

* Female
* Male

Binary fields contained only their expected `0` and `1` values.

**Result:** No inconsistent or unexpected categories were identified.

### Numerical Validation

The following ranges were reviewed:

* **Age:** 18–92
* **Credit Score:** 350–850
* **Tenure:** 0–10 years
* **Number of Products:** 1–4
* **Estimated Salary:** 11.58–199,992.48

No obviously invalid values were identified.

### Header Standardisation

The cleaned workbook uses clearer, more readable column names, including:

* Customer ID
* Credit Score
* Country
* Tenure (Years)
* Account Balance
* Number of Products
* Has Credit Card
* Is Active Member
* Estimated Salary

Additional analytical fields were created for segmentation.

---

## Analysis Performed

The analysis examined the following questions:

1. What percentage of customers exited the bank?
2. Does churn differ by country?
3. Does churn differ by gender?
4. Does customer activity relate to churn?
5. Does churn differ by age group?
6. Does the relationship between number of products and churn vary by age group?
7. Does account balance differ between customers who stayed and exited?
8. Does credit score differ between customers who stayed and exited?
9. Does churn differ across account balance ranges?
10. Does churn vary substantially across tenure groups and credit-card ownership?

---

## Key Findings

### Overall Churn

Out of 10,000 customers:

* **7,963 customers stayed**
* **2,037 customers exited**
* **Overall churn rate: 20.37%**

This means approximately one in five customers in the dataset exited the bank.

---

### Churn by Country

| Country | Total Customers | Customers Exited | Churn Rate |
| ------- | --------------: | ---------------: | ---------: |
| France  |           5,014 |              810 |     16.15% |
| Spain   |           2,477 |              413 |     16.67% |
| Germany |           2,509 |              814 | **32.44%** |

Germany recorded the highest churn rate at **32.44%**, substantially above the overall churn rate of 20.37%.

This identifies the German customer segment as an important area for further investigation rather than evidence that the German operation itself is the cause of churn.

---

### Churn by Gender

| Gender | Total Customers | Customers Exited | Churn Rate |
| ------ | --------------: | ---------------: | ---------: |
| Female |           4,543 |            1,139 | **25.07%** |
| Male   |           5,457 |              898 |     16.46% |

Female customers had an **8.61 percentage-point higher churn rate** than male customers.

This suggests that gender is associated with different churn patterns in this dataset, although further analysis would be required to determine what underlying factors may explain the difference.

---

### Churn by Customer Activity

| Customer Status | Total Customers | Customers Exited | Churn Rate |
| --------------- | --------------: | ---------------: | ---------: |
| Inactive        |           4,849 |            1,302 | **26.85%** |
| Active          |           5,151 |              735 |     14.27% |

Inactive customers had a churn rate **12.58 percentage points higher** than active customers.

Customer activity therefore emerged as one of the stronger differences observed in the analysis.

---

### Churn by Age Group

| Age Group | Churn Rate |
| --------- | ---------: |
| 18–29     |      7.56% |
| 30–39     |     10.88% |
| 40–49     |     30.79% |
| 50–59     | **56.04%** |
| 60+       |     27.95% |

Churn increased considerably among older customer groups.

The **50–59 age group recorded the highest churn rate at 56.04%**, while customers aged 18–29 recorded the lowest at 7.56%.

---

### Number of Products and Churn

Customers with two products recorded a notably low churn rate of **7.58%**.

Customers with three and four products showed substantially higher churn rates. However, these groups contained considerably fewer customers.

All customers in the four-product group had exited.

**Important:** These results should not be interpreted as evidence that having more products causes churn. The smaller sample sizes require cautious interpretation and further investigation.

---

### Account Balance

Average account balance differed between customers who stayed and those who exited:

| Customer Status | Average Account Balance |
| --------------- | ----------------------: |
| Stayed          |               72,745.30 |
| Exited          |           **91,108.54** |

Exited customers had an average balance approximately **18,363.24 higher** than customers who stayed.

This suggests that potentially valuable customers with higher account balances may warrant additional attention when considering retention strategies.

---

### Credit Score

| Customer Status | Average Credit Score |
| --------------- | -------------------: |
| Stayed          |               651.85 |
| Exited          |               645.35 |

The difference was only **6.50 points**, indicating a relatively modest difference between the two groups.

Based on this descriptive analysis, credit score appears to be a lower-priority churn factor compared with characteristics such as customer activity and age.

---

### Account Balance Segments

| Account Balance Range | Total Customers | Customers Exited | Churn Rate |
| --------------------- | --------------: | ---------------: | ---------: |
| 0                     |           3,617 |              500 |     13.82% |
| 1–50,000              |              75 |               26 |     34.67% |
| 50,001–100,000        |           1,509 |              300 |     19.88% |
| 100,001–150,000       |           3,830 |              987 | **25.77%** |
| 150,001+              |             969 |              224 |     23.12% |

The 1–50,000 balance group recorded the highest churn rate at 34.67%, but contained only 75 customers.

Among the larger groups, customers with balances between 100,001 and 150,000 had a churn rate of 25.77%.

The relationship between balance and churn was therefore not simply linear.

---

### Tenure

Churn rates across tenure groups showed relatively limited variation:

| Tenure Group | Churn Rate |
| ------------ | ---------: |
| 0–2 years    |     21.15% |
| 3–5 years    |     20.76% |
| 6–8 years    |     18.87% |
| 9–10 years   |     21.30% |

The difference between the lowest and highest tenure-group churn rates was relatively small.

Tenure therefore appears to be a lower-priority factor based on this analysis.

---

## Key Insights

| Finding                                             | Evidence                               |
| --------------------------------------------------- | -------------------------------------- |
| Germany had the highest geographic churn            | Germany: **32.44%** vs overall: 20.37% |
| Female customers had higher churn                   | Female: **25.07%** vs Male: 16.46%     |
| Inactive customers were more likely to churn        | Inactive: **26.85%** vs Active: 14.27% |
| Churn increased substantially among older customers | Age 50–59: **56.04%**                  |
| Two-product customers had notably lower churn       | 2 Products: **7.58%**                  |
| Higher-balance segments showed elevated churn       | 100,001–150,000: **25.77%**            |
| Credit score showed only a small difference         | Stayed: 651.85 vs Exited: 645.35       |
| Tenure showed relatively little variation           | Churn ranged from **18.87%–21.30%**    |

---

## Business Recommendations

### 1. Prioritise Customer Engagement

Inactive customers had a **26.85% churn rate**, compared with 14.27% for active customers.

**Recommendation:**
Develop targeted re-engagement initiatives for inactive customers, including personalised offers, product education, reminders and digital engagement strategies.

---

### 2. Investigate the German Customer Segment

Germany recorded a churn rate of **32.44%**, compared with 16.15% in France and 16.67% in Spain.

**Recommendation:**
Investigate the German customer experience, product mix and service patterns to identify factors associated with the higher churn rate before developing Germany-specific retention strategies.

---

### 3. Investigate Customers Aged 40–59

Customers aged 50–59 had a churn rate of **56.04%**, while customers aged 40–49 had a churn rate of 30.79%.

**Recommendation:**
Prioritise further analysis of customers aged 40–59 to understand whether financial needs, product suitability, customer experience or service expectations differ from younger customers.

---

### 4. Consider Customer Account Value

Exited customers had a higher average account balance than customers who stayed.

**Recommendation:**
Include account value when prioritising retention efforts so potentially valuable customers at risk of churn can receive appropriate attention.

---

### 5. Investigate Product Usage

Two-product customers had a notably low churn rate of **7.58%**, while three- and four-product customers showed substantially higher churn.

**Recommendation:**
Investigate whether customers with multiple products experience product complexity, dissatisfaction or service issues.

The analysis does **not** establish that having more products causes churn.

---

### 6. Monitor Balance Segments

Churn varied across account balance ranges, although some groups were considerably smaller than others.

**Recommendation:**
Monitor balance segments as part of customer profiling while avoiding major decisions based solely on small customer groups.

---

## Lower-Priority Factors

Based on the descriptive analysis, the following factors showed relatively limited differences:

* Tenure
* Credit-card ownership
* Credit score
* Estimated salary

These factors should receive lower priority in immediate retention strategies unless further analysis identifies interactions with stronger churn indicators.

---

## Visualisations

The Excel workbook includes charts created to communicate key findings from the analysis, including:

* Overall customer churn
* Churn by country
* Churn by gender
* Churn by customer activity
* Churn by age group
* Churn by product usage
* Account balance comparisons
* Other supporting churn patterns

---

## Tools Used

* **Microsoft Excel**

  * Data validation
  * Data cleaning
  * `COUNTIF`
  * `COUNTA`
  * Calculated fields
  * Customer segmentation
  * Pivot-style analysis
  * Charts and visualisation
  * Descriptive analysis

* **GitHub**

  * Version control
  * Project documentation
  * Portfolio presentation

---

## Repository Structure

```text
Bank-Customer-Churn-Analysis/
│
├── Cleaned_Data/
│   └── Bank_Churn_Cleaned.xlsx
│
├── Documentation/
│   └── Bank Customer Churn Analysis.pdf
│
├── Raw_Data/
│   ├── Bank_Churn.csv
│   ├── Bank_Churn_Data_Dictionary.csv
│   └── Bank_Churn_Messy.xlsx
│
└── README.md
```

### Folder descriptions

**Raw_Data**
Contains the original dataset files and data dictionary used as the starting point for the project.

**Cleaned_Data**
Contains the final Excel workbook after data validation, analysis, derived fields and visualisation.

**Documentation**
Contains the detailed project analysis report.

---

## Limitations

This analysis is descriptive and identifies patterns and associations within the customer data. It does not establish causal relationships.

Some segments, particularly customers with three or four products and customers with balances between 1 and 50,000, contain relatively few observations and should therefore be interpreted cautiously.

Further analysis using statistical testing or predictive modelling would be required to determine which factors are the strongest predictors of customer churn.

---

## Conclusion

The analysis identified several customer characteristics associated with higher observed churn, particularly **customer activity, geography and age**.

The strongest patterns included:

* Higher churn among inactive customers.
* Substantially higher churn in Germany.
* Significantly higher churn among customers aged 40–59.
* Higher average account balances among customers who exited.
* Lower observed churn among customers with two products.

These findings provide useful starting points for customer-retention analysis, while further investigation would be required to determine the underlying causes and build predictive churn models.

---

## Dataset Attribution

This project uses the **Bank Customer Churn** dataset provided through the Maven Analytics Data Playground. Maven Analytics identifies the original source as Kaggle and describes the dataset as account information for 10,000 customers at a European bank.

**Source:**
[Maven Analytics Data Playground — Bank Customer Churn](https://mavenanalytics.io/data-playground/bank-customer-churn?utm_source=chatgpt.com)

**Original source credited by Maven Analytics:** Kaggle

This repository is a personal portfolio project for data analysis practice and demonstration of Microsoft Excel skills.

