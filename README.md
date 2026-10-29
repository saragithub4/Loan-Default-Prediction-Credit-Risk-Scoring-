#  Loan Default Prediction & Credit Risk Scoring

## 📌 Project Overview

This project focuses on analyzing LendingClub loan data to identify the key factors associated with loan defaults and assess borrower credit risk.

Using historical loan records from 2007 to 2018, the project explores relationships between borrower income, credit scores, loan purpose, interest rates, debt-to-income ratio, employment length, and loan repayment outcomes.

The objective is to understand the characteristics associated with higher default risk and develop a data-driven approach to credit risk analysis and loan default prediction.

## 📂 Dataset Description

The dataset used in this project is **LendingClub Loan Data (2007–2018 Q4)**, published by `wordsforthewise` on Kaggle.

**Dataset source:** https://www.kaggle.com/datasets/wordsforthewise/lending-club?select=accepted_2007_to_2018Q4.csv.gz  

**File name:** `accepted_2007_to_2018Q4.csv.gz`

The dataset contains historical records of loans accepted through LendingClub, a peer-to-peer lending platform. It provides detailed information about borrowers, loan characteristics, credit history, and loan performance.

### Dataset Details

| Attribute | Description |
|---|---|
| Dataset Name | LendingClub Loan Data |
| Data Source | Kaggle |
| Publisher | wordsforthewise |
| Time Period | 2007–2018 Q4 |
| File Format | Compressed CSV (`.csv.gz`) |
| License | CC0: Public Domain, as specified on Kaggle |
| Primary Domain | Finance, Lending, and Credit Risk Analytics |
| Main Application | Loan Default Prediction and Credit Risk Scoring |

The accepted-loans file contains approximately 2.26 million loan records and 151 columns. Exact counts may vary depending on the dataset version and subsequent preprocessing.

## 📊 Dataset Features

The dataset contains numerous variables describing borrower characteristics, financial information, loan terms, credit history, and repayment outcomes.

The following are some important features used in credit risk analysis.

| Feature | Description |
|---|---|
| `loan_amnt` | Amount of the loan requested |
| `funded_amnt` | Total amount funded for the loan |
| `term` | Loan repayment term |
| `int_rate` | Interest rate charged on the loan |
| `installment` | Monthly loan payment |
| `grade` | LendingClub-assigned loan grade |
| `sub_grade` | More detailed loan risk classification |
| `emp_length` | Length of the borrower's employment |
| `home_ownership` | Borrower's home ownership status |
| `annual_inc` | Borrower's self-reported annual income |
| `verification_status` | Status of income verification |
| `purpose` | Purpose for which the loan was requested |
| `dti` | Debt-to-income ratio |
| `fico_range_low` | Lower bound of the borrower's FICO score range at application |
| `fico_range_high` | Upper bound of the borrower's FICO score range at application |
| `delinq_2yrs` | Number of credit delinquencies in the preceding two years |
| `open_acc` | Number of open credit accounts |
| `pub_rec` | Number of derogatory public records |
| `revol_bal` | Total revolving credit balance |
| `revol_util` | Revolving credit utilization rate |
| `loan_status` | Current or recorded status of the loan |

*Note: These are selected examples, not the complete list of dataset columns. The availability and interpretation of particular fields should be verified against the downloaded file.*

## 🎯 Project Objectives

The main objectives of this project are:

- **Data Cleaning:** Identify and handle missing values, duplicate records, inconsistent data types, and invalid values.
- **Exploratory Data Analysis (EDA):** Understand the structure, distribution, and characteristics of the loan dataset.
- **Income Analysis:** Investigate how borrower income relates to loan characteristics and repayment outcomes.
- **Credit Score Analysis:** Examine the relationship between FICO scores and loan performance.
- **Loan Purpose Analysis:** Identify differences in repayment outcomes across loan purposes.
- **Interest Rate Analysis:** Explore the association between interest rates, loan grades, and default outcomes.
- **Debt-to-Income Analysis:** Assess how borrower debt obligations relate to repayment performance.
- **Default Risk Identification:** Identify financial and credit-related characteristics associated with higher default rates.
- **Credit Risk Scoring:** Explore suitable analytical or machine learning techniques for estimating loan default risk.
- **Data Visualization:** Present important findings through charts, graphs, and summary tables.
- Analyze loan default patterns.


## 🔍 Key Questions for Analysis

This project aims to answer the following questions:

1. What proportion of loans are fully paid, charged off, or in other repayment states?
2. How does annual income relate to loan default rates?
3. Do borrowers with lower FICO scores exhibit different repayment patterns?
4. Which loan purposes have higher observed default rates?
5. How do interest rates vary across loan grades and subgrades?
6. Is a higher debt-to-income ratio associated with a greater likelihood of default?
7. How do employment length and home ownership relate to repayment outcomes?
8. Which borrower and loan characteristics are most strongly associated with loan defaults?
9. Can historical loan information be used to build a model that estimates default risk?

## 🛠️ Tools and Technologies

The following tools and technologies can be used to complete the project:

- **Microsoft Excel:** Data preprocessing
- **SQL:** Data preprocessing
- **Python:** Data analysis and preprocessing
- **Pandas:** Data manipulation and cleaning
- **NumPy:** Numerical computations
- **Matplotlib:** Data visualization
- **Seaborn:** Statistical visualization
- **Jupyter Notebook:** Interactive analysis and documentation


## 🧹 Data Preparation

Before conducting the analysis, the dataset may require the following preprocessing steps:

1. Load the compressed CSV file into Python using Pandas.
2. Inspect the dataset's dimensions, column names, and data types.
3. Identify missing values and evaluate appropriate handling strategies.
4. Check for duplicate records and inconsistent entries.
5. Convert date fields into appropriate datetime formats.
6. Validate numerical fields, including interest rates, income, loan amounts, and credit utilization.
7. Examine categorical variables and standardize inconsistent category values where necessary.
8. Analyze the distribution of loan statuses.
9. Select relevant features for exploratory analysis and modeling.
10. Prepare the target variable and prevent data leakage before training a prediction model.

**Important:** The Kaggle publisher reports that the `int_rate` and `revol_util` columns have already had percentage symbols removed and have been converted to numeric values. Therefore, these fields should be checked before applying additional transformations.

## 🎯 Target Variable

The `loan_status` column can be used to investigate loan repayment outcomes.

For a binary loan default prediction model, the target can be derived by classifying appropriate loan statuses into two categories:

- **Default / Charged Off:** Loans recorded as charged off, subject to the project's precise default definition.
- **Fully Paid:** Loans that have been fully repaid.

Other statuses, such as Current, In Grace Period, Late, and Default, require careful consideration. They should not automatically be treated as fully paid or as confirmed defaults.

For a reliable model, define the target consistently and consider excluding loans whose final outcomes are not yet known. The exact classification rules should be documented in the analysis.

## 📈 Expected Outcomes

The project is intended to produce:

- A cleaned and analysis-ready dataset.
- Exploratory data analysis of borrower and loan characteristics.
- Visualizations showing relationships between financial variables and loan outcomes.
- Identification of factors associated with higher observed default rates.
- Summary tables comparing repayment outcomes across borrower groups.
- A documented approach to developing and evaluating a loan default prediction model, if machine learning is included.
- Insights that demonstrate how historical lending data can support credit risk analysis.

The findings should be interpreted as associations in historical data rather than proof that a particular borrower characteristic causes default.

## ⚠️ Data Limitations

1.The dataset covers historical LendingClub loans from multiple years. Lending conditions, borrower behavior, and economic circumstances may differ from those in the present day.

2.Some fields may contain substantial missing data. The treatment of missing values could affect the analysis and model performance.

3.Loans with statuses such as Current or Late may not have final repayment outcomes. Excluding these records from the primary binary classification analysis may introduce selection bias.

4.The analysis identifies associations within historical data. It cannot establish causation or guarantee future outcomes.

5.A model trained on LendingClub data may not perform equally well for other financial institutions, borrower populations, or economic periods.

6.Predictive performance alone is insufficient for lending decisions. Any practical deployment would require appropriate fairness assessments, explainability, privacy safeguards, and compliance with applicable laws and regulations.

7.The selected CSV file is large and may require substantial memory and processing time. Sampling, column selection, or chunk-based processing may be necessary.


## 📥 Dataset Access

Download the dataset from the official Kaggle dataset page:

[LendingClub Loan Data — wordsforthewise](https://www.kaggle.com/datasets/wordsforthewise/lending-club?select=accepted_2007_to_2018Q4.csv.gz)

After downloading, extract the compressed file if required and place it in the appropriate local data directory.

The complete dataset is large, so the raw CSV file is not included in this repository. Users should download it directly from Kaggle and follow the instructions in the project notebooks.

## 📜 License and Attribution


**Dataset credit:** wordsforthewise — LendingClub Loan Data, 2007–2018 Q4, Kaggle.

This repository is intended for educational, analytical, and portfolio purposes. The analysis does not constitute financial advice or an actual lending decision system.

## 👩‍💻 Project Status

**Status:** In Progress

The project covers data understanding, preprocessing, exploratory analysis, and the investigation of loan default risk. Additional stages, including predictive modeling and model evaluation, can be incorporated as the analysis progresses.
