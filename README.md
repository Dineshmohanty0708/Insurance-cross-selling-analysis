# Insurance Cross-Selling Analysis 

# Project Overview

This project focuses on analyzing customer data from **United India Insurance** to understand cross‑selling opportunities. The objective is to identify which customers are more likely to purchase additional insurance products and evaluate how well the company’s lead rating system (Cold/Warm/Hot) aligns with actual conversions.

The project includes:

* Data preprocessing & cleaning
* Exploratory Data Analysis (EDA)
* Understanding conversion behavior
* Validating the rating system
* Insights to improve marketing and sales strategy


# Dataset Summary

**Rows:** 100,000 customers
**Columns:** 16 (demographic, product, behavioral & target variables)

# Key Columns

* **Demographic:** Age, Gender, Marital Status, Education, Occupation, Job Title
* **Product:** Current Product, Current Coverage, New Product Type, New Coverage
* **Behavioral:** Rating (Cold/Warm/Hot)
* **Target Variable:** Converted (Yes/No)

# Data Preprocessing Steps

# 1. Handling Missing Values

* **Numeric columns:** Imputed using mean/median
* **Income column:** Imputed using *occupation-wise averages*
* **Categorical columns:** Imputed using mode
* **Converted column:** Rows with missing target removed

# 2. Cleaning & Standardization

* Standardized column names (spaces replaced with underscores)
* Converted categorical variables to proper types
* Dropped redundant fields such as duplicate status columns

# 3. Target Creation

Converted values were converted into numeric form:

* Yes → 1
* No → 0

# 4. Final Checks

* No missing values remaining
* Data types validated
* Cleaned dataset stored as **Cleaned_ds.csv**

# Exploratory Analysis & Insights

# 1. Univariate Analysis (One variable at a time)

Analysed numeric variables (Age, Family Members, Income, Coverages) using:

* KDE plots
* Boxplots
* Mean comparisons

## Key Findings

* **Younger customers (30–40)** converted more.
* **Higher-income customers** show significantly higher conversion rates.
* Customers with **low current coverage** are more likely to purchase new policies.
* Converted customers often opted for **higher new coverage**.

# 2. Categorical Variable Analysis

Reviewed gender, marital status, education, occupation, job title, and product types.

## Major Insights

* Gender has negligible impact on conversions.
* Single customers convert more than married customers.
* Higher education groups (MD, PD) show higher conversion.
* Certain occupations like **support professionals (SPT)** convert more.
* Customers with **no current product** are more likely to purchase one.
* **Investment (INV)** and **Endowment (END)** product types perform best.


# Lead Rating (Cold/Warm/Hot) Analysis

Comparing lead scores with real conversions:

| Rating | Conversion % |
| ------ | ------------ |
| Cold   | ~5%          |
| Warm   | ~52%         |
| Hot    | ~90%         |

# Insight

The company’s lead rating system is highly accurate. Conversion probability increases steadily from Cold → Warm → Hot.

## 🔗 Conversion vs Product & Occupation

## Best-converting New Product Types

1. Investment (INV)
2. Endowment (END)

Strongest Occupation Segments (Hot leads)

* Support Professionals (SPT)
* Self-Employed (SE)

These groups are ideal targets for cross-selling.


# Conclusion

This project provides deep insight into customer behavior, product preference, and lead quality. The key takeaways include:

* Young, high‑income, underinsured customers convert the most.
* Investment and Endowment products are strongest cross‑sell candidates.
* Lead rating system works very well and should be continued.
* Marketing efforts should focus on Hot & Warm leads, especially in SPT and SE occupations.

The analysis builds a solid foundation for future predictive modeling or campaign optimization.

## Project Files

* **Cross.analysis.pdf** – business understanding + detailed EDA findings
* **Main.ipynb** – full preprocessing, plots, and analysis code
* **Cleaned_ds.csv** – cleaned dataset used for analysis


