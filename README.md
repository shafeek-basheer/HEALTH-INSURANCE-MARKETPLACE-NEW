# HEALTH-INSURANCE-MARKETPLACE-NEW
The Health Insurance Marketplace offers thousands of insurance plans across states and years, making it difficult to understand differences in costs, coverage, and benefits. This project aims to analyze marketplace data to identify trends in benefit coverage, cost-sharing, and plan availability across states and business years.Here we are only analysis on Benefit_cost sharing.
## Project Structure
```
COVID-19-Vaccination-Outcomes-EDA/
│
├── README.md                          <-- You are here
├── data/
│   ├── raw/                           <-- Original dataset 
│   └── cleaned/                       <-- "clean_benefits.csv"
├── notebooks/                         <-- Jupyter/Colab notebooks with complete analysis
├── scripts/                           <-- data_cleaning.py and visualization_utils.py
├── reports/
│   └── analysis_report           <-- Comprehensive findings document(Colab notebooks with complete analysis_report)
└── visuals/                           <-- Generated charts and graphs
```

## Project Objectives

This project aims to:

- To analyze the distribution of health insurance benefits across different business years (2014–2016).
- To examine the variation of benefit offerings across different states.
- To identify the most frequently defined health benefits in insurance plans.
- To evaluate the overall coverage status of benefits.
- To assess the scale of the insurance market in terms of number of unique plans and issuers.

## Phase 1 — Problem Definition & Dataset Selection

📌 Problem Statement:

###  The health insurance marketplace dataset contains over 5 million benefit-level records across multiple states and business years (2014–2016). Due to the large volume and multi-level structure of the data     (benefits, plans, issuers, and states), it is difficult to clearly understand:
- How benefits are distributed across years
- How coverage varies across states
- Which benefits are most frequently defined
- The overall coverage patterns
- The scale of the market in terms of plans and issuers

 ## 📊 Dataset Details
 ### 📌 Overview
The dataset contains benefit-level information for health insurance plans offered in the United States between 2014 and 2016.
Each row represents a specific benefit under a particular insurance plan.
- Total Records: 5,048,408
- Unique Plans (PlanId): ~52,394
- Unique Issuers (IssuerId): Multiple issuers across states
- States Covered: 39
- Years Covered: 2014, 2015, 2016.

## 🧹 Phase 2 — Data Cleaning & Pre-processing
### 📌 1. Duplicate Handling
- Checked for duplicate records.
- Removed duplicate rows to ensure data integrity.
- Verified uniqueness of key identifiers such as PlanId.

## 📌 2. Missing Value Analysis

- Calculated missing values for all columns.
- Identified columns with significant missing data.
- Differentiated between:
 Structural missing values (e.g., tier-based cost columns)
 True data gaps
### Actions taken:
- Columns with excessive missing values (e.g., >70%) were excluded from basic analysis.
- Moderate missing categorical fields were handled carefully (e.g., labeled as “Unknown” where appropriate).
- No blind imputation was performed.
- 
## 📌 3. Column Selection
To maintain focus and reduce complexity, only relevant columns were selected for structural analysis:
- BusinessYear
- StateCode
- BenefitName
- IsCovered
- PlanId
- IssuerId

## 📌 4. Data Type Verification
- Verified correct data types for numeric and categorical variables.
- Ensured BusinessYear is treated as numeric.
- Confirmed identifier fields (PlanId, IssuerId) are not used in numeric calculations

## 📌 5. Consistency Checks
- Checked for inconsistent categorical labels.
- Verified unique counts for key identifiers.
- Ensured year range is limited to 2014–2016.

## 📌 6. Data Reduction Strategy
- Due to the dataset size (5M+ records):
- Limited analysis to necessary columns.
- Avoided memory-heavy transformations.
- Focused on structural exploration rather than full feature engineering.

 ### Output
- The cleaned dataset is saved at:"C:\data\clean\clean_benefits.csv":

## 📊 Phase 3 — Exploratory Data Analysis (EDA)

### 📌 Objective of EDA
The goal of this phase was to understand the structural characteristics of benefit distribution across years, states, plans, and issuers.
### 📌 1️⃣ Year-wise Distribution of Benefits
- Analyzed number of benefit records per BusinessYear
- Compared distribution across 2014, 2015, and 2016
- Checked whether benefit definitions increased or decreased over time
Insight example (you fill based on your result):
The number of benefit records remained relatively stable across years, indicating structural consistency in plan design.

## 📌 2️⃣ State-wise Distribution
- Counted number of benefit records per StateCode
- Identified states with highest plan activity
- Observed variation in benefit volume across states
Insight example:
Some states show significantly higher benefit counts, suggesting larger insurance market activity.

## 📌 3️⃣ Most Frequent Benefits
- Calculated frequency of BenefitName
- Identified top 10 most common benefits
- Examined concentration of specific healthcare services
Insight example:
Preventive and dental-related benefits appeared most frequently across plans.

## 📌 4️⃣ Coverage Pattern Analysis
- Analyzed distribution of IsCovered
- Calculated percentage of Covered vs Not Covered services
- Assessed overall coverage generosity
Insight example:
The majority of benefit records were marked as "Covered," indicating broad inclusion of essential services.

## 📌 Visualizations Included
- Bar chart: Benefits by Year
- Bar chart: Benefits by State
- Top 10 Most Frequent Benefits
- Coverage Distribution Pie/Bar Chart

## 📌 Conclusion
 This analysis examined the structural characteristics of health insurance benefits between 2014 and 2016 using benefit-level data.
 The dataset includes over 5 million records and more than 52,000 unique plans across multiple states, highlighting the scale and complexity of the marketplace.
Key findings include:
- Stable benefit distribution across years
- Significant variation in plan activity across states
- High frequency of standardized benefit names
- Majority of benefits marked as covered
The results provide a clear structural understanding of benefit-level design and coverage patterns in the U.S. health insurance marketplace.

## How to Use This Project

1. **Clone the repository**
   ```bash
   git clone https://github.com/Anjali9037/EDA-of-COVID-19-Outcomes-by-Vaccination-Status-Using-Python
   ```

2. **Install requirements**
   ```bash
   pip install -r requirements.txt
   ```

3. **Explore the analysis**
   - Complete analysis available in: `/notebooks/`
   - Data cleaning scripts in: `/scripts/`
   - Generated insights in: `/reports/`
  
   - ## Technical Skills Demonstrated

- **Python Programming**: Pandas, NumPy, Matplotlib, Seaborn
- **Data Cleaning & Preprocessing**: Missing value handling, feature engineering, data validation
- **Statistical Analysis**: Descriptive statistics, correlation analysis, trend analysis
- **Data Visualization**: Multiple chart types, effective storytelling, professional presentation
- **Domain Knowledge**: Public health, epidemiology, vaccination strategies
- **Project Management**: End-to-end pipeline execution, documentation, reproducibility

- ## Author

SHAFEEK.M.B
GitHub:https://github.com/Anjali9037

---

*This project serves as a comprehensive demonstration of data analytics capabilities suitable for academic evaluation, job portfolios, and public health research applications.*
