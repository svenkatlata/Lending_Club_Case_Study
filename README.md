# Lending_Club_Case_Study

> Understanding Risk Analytics in Banking and Financial Services using Exploratory Data Analysis (EDA).

Lending Club is a **consumer finance company** which specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile.

Two **types of risks** are associated with the bank’s decision:

- If the applicant is **likely to repay the loan**, then not approving the loan results in a **loss of business** to the company.
- If the applicant is **not likely to repay the loan**, i.e. he/she is likely to default, then approving the loan may lead to a **financial loss** for the company.

The data given below contains information about past loan applicants and whether they **‘defaulted’** or not. The aim is to identify patterns which indicate if a person is likely to default, which may be used for taking actions such as denying the loan, reducing the amount of the loan, lending (to risky applicants) at a higher interest rate, etc. The following dataset contains the complete loan data for all loans issued through the time period 2007 to 2011.

[Loan Dataset](data/loan.csv)

In this case study, we will use EDA to understand how **consumer attributes** and **loan attributes** influence the tendency of default.

**Note: You can access the data dictionary which describes the meaning of these variables from the provided link below:**

[Data Dictionary](data/Data_Dictionary.xlsx)

## Table of Contents

- [General Info](#general-information)
- [Conclusions](#conclusions)
- [Technologies Used](#technologies-used)
- [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information

The **Objectives** of this case study are to:

1. Understand EDA techniques in the context of banking and financial services.
2. Develop a basic understanding of risk analytics.
3. Learning how data is used to minimize lending risks.

### _Problem Statement_

- Like most other lending companies, not approving the loan to **‘potential’** applicants and lending loans to **‘risky’** applicants are the largest sources of financial loss (called **credit loss**).

- We analyzed the loan data for all loans issued through the time period **2007 to 2011** by the Lending Club Company.

- Our goal was to understand the **driving factors** behind loan default.

- In this case study, we used Exploratory Data Analysis (EDA) to identify patterns and understand how **consumer attributes** and **loan attributes** influence the tendency of default.

- The company can utilise this knowledge for its **portfolio** and **risk assessment**.

### _Business Understanding_

When a person applies for a loan, there are two types of decisions that could be taken by the company:

1. **Loan accepted**: If the company approves the loan, there are 3 possible scenarios described below:

   1. **Fully paid**: Applicant has fully paid the loan (the principal and the interest rate)
   2. **Current**: Applicant is in the process of paying the instalments, i.e. the tenure of the loan is not yet completed. These candidates are not labelled as 'defaulted'.
   3. **Charged-off**: Applicant has not paid the instalments in due time for a long period of time, i.e. he/she has defaulted on the loan

2. **Loan rejected**: The company had rejected the loan (because the candidate does not meet their requirements etc.). Since the loan was rejected, there is no transactional history of those applicants with the company and so this data is not available with the company (and thus in this dataset)

### _Data Understanding_

- data quality issues?
- meaningful interpretation of variables?

### _Data Cleaning and Manipulation_

- missing value imputation, outlier treatment, sanity checks and other kinds of data redundancies, etc.?
- data is converted to a suitable and convenient format?
- Strings and Dates manipulation?

### _Data analysis_

- Univariate and segmented univariate analysis, at least the 5 important driver variables (i.e. variables which are strong indicators of default) ?
- Business-driven, type-driven and data-driven derived metrics are created for the important variables and utilised for analysis?
- Bivariate analysis, identify the important combinations of driver variables, business or analytical insights?
- most useful insights?
- Custom functions are used to perform repetitive tasks?

## Conclusions

(coming soon...)

- Conclusion 1 from the analysis
- Conclusion 2 from the analysis
- Conclusion 3 from the analysis
- Conclusion 4 from the analysis

## Technologies Used

Data Cleaning and Manipulation, and Exploratory Data Analysis using:

- Python - version 3.11.5
- NumPy - version 1.26.4
- Pandas - version 2.2.2

Data Visualization using:

- Matplotlib - version 3.8.4
- Seaborn - version 0.13.2

## Acknowledgements

**This is a Group Case Study done as a part of Executive PG Programme in AI & ML from IIIT, Bangalore by upGrad.**

_Batch: ML C65_

**_References_**

- [Classification based credit risk analysis: The case of Lending Club](https://www.researchgate.net/publication/364513584_Classification_based_credit_risk_analysis_The_case_of_Lending_Club)
- [Towards Repayment Prediction in Peer-to-Peer Social Lending Using Deep Learning](https://www.researchgate.net/publication/345389806_Towards_Repayment_Prediction_in_Peer-to-Peer_Social_Lending_Using_Deep_Learning)
- [Lending Club Data Analysis](https://www.researchgate.net/publication/340395124_Project_Lending_Club_Data_Analysis)
- [Personal Loan Eligibility: Criteria You Need to Know Before You Apply](https://www.lendingclub.com/resource-center/personal-loan/personal-loan-eligibility-criteria-you-need-to-know-before-you-apply)
- [What to Do If You’re Declined a Personal Loan](https://www.lendingclub.com/resource-center/personal-loan/what-to-do-if-you-are-declined-a-personal-loan)
- [What Is Debt Consolidation?](https://www.lendingclub.com/resource-center/personal-loan/what-is-debt-consolidation)

## Contact

Reach out to the creators on,

- [Venkat Lata](https://github.com/svenkatlata)

- [Sunil Bhairi](https://github.com/SunilBhairi/)
