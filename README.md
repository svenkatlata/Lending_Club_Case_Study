# Lending_Club_Case_Study

> Understanding Risk Analytics in Banking and Financial Services using Exploratory Data Analysis (EDA).

Lending Club is a **consumer finance company** which specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile.

Two **types of risks** are associated with the bank’s decision:

- If the applicant is **likely to repay the loan**, then not approving the loan results in a **loss of business** to the company.
- If the applicant is **not likely to repay the loan**, i.e. he/she is likely to default, then approving the loan may lead to a **financial loss** for the company.

The data given below contains information about past loan applicants and whether they **‘defaulted’** or not. The aim is to identify patterns which indicate if a person is likely to default, which may be used for taking actions such as denying the loan, reducing the amount of the loan, lending (to risky applicants) at a higher interest rate, etc. The following dataset contains the complete loan data for all loans issued through the time period 2007 to 2011.

[Loan Dataset](loan.csv)

In this case study, we will use EDA to understand how **consumer attributes** and **loan attributes** influence the tendency of default.

**Note: You can access the data dictionary which describes the meaning of these variables from the provided link below:**

[Data Dictionary](Data_Dictionary.xlsx)

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

- **Data Quality Issues:** During the initial phase of data analysis, several quality issues were identified, including missing values, inconsistencies in categorical variables, and outliers. These issues were addressed to ensure the accuracy and reliability of the analysis. Data integrity checks were performed to validate the consistency of variable formats and values.

- **Meaningful Interpretation of Variables:** Key variables such as loan amount, interest rate, loan term, and borrower income were carefully examined. Their relevance and impact on loan defaults were assessed, revealing that variables like loan amount, interest rate, and borrower income play crucial roles in predicting default rates.

### _Data Cleaning and Manipulation_

- **Missing Value Imputation and Outlier Treatment:** Missing values were imputed using statistical methods or domain knowledge to maintain data completeness. Outliers were identified and treated to prevent skewed results. For instance, extreme loan amounts or interest rates were examined and adjusted to ensure they did not disproportionately influence the analysis.

- **Sanity Checks and Data Redundancies:** Comprehensive sanity checks were conducted to identify and rectify data redundancies, ensuring that duplicate records or inconsistent entries were removed. This helped streamline the dataset and enhance the overall quality of the analysis.

- **Data Conversion and Manipulation:** The data was converted into a suitable format for analysis, including transforming categorical variables into numerical codes where necessary. String variables were standardized, and date variables were parsed to extract relevant temporal features, facilitating more accurate temporal analysis.

### _Data Analysis_

- **Univariate and Segmented Univariate Analysis:** Univariate analysis was performed to understand the distribution and characteristics of individual variables. Segment-wise univariate analysis was used to examine how key variables such as loan amount, interest rate, and borrower income vary across different segments, such as default and non-default cases. This revealed significant insights into which variables are strong indicators of loan default.

- **Derived Metrics and Business-Driven Insights:** Business-driven metrics, such as default rates by loan purpose or income category, were created to provide a clearer picture of loan performance. Type-driven metrics, including average loan amounts and interest rates, were also computed to assess their impact on default rates. These metrics were utilized to uncover patterns and relationships that inform business strategies.

- **Bivariate Analysis:** Bivariate analysis was conducted to explore the relationships between pairs of variables. This analysis identified critical combinations of variables that influence default rates, such as the interplay between loan amount and interest rate. Insights gained from this analysis highlighted the importance of specific variable interactions in predicting defaults.

- **Useful Insights:** Key insights include identifying high-interest rates and large loan amounts as strong predictors of default, particularly when combined with certain loan purposes or borrower profiles. Regional variations in loan issuance and default rates also provided valuable information for targeted business strategies.

- **Custom Functions:** Custom functions were developed to automate repetitive tasks, such as plotting segmented univariate analyses and aggregating data by different segments. These functions enhanced efficiency and consistency in the analysis process, allowing for more comprehensive and scalable evaluations.

This approach ensured that the data analysis was thorough and insightful, providing a robust foundation for understanding loan default drivers and informing business decisions.

## Conclusions

### Univariate and Segmented Univariate Analysis:

#### KEY INSIGHTS FOR QUANTITATIVE ATTRIBUTES

1. **Loan Amount Distribution:** The majority of loans were issued within the $5,000 to $14,000 range, with $10,000 being the most frequently issued amount.
   However, the most popular issued amount among investors was $5,000.
2. **Loan Amounts and Default Status:** Borrowers who defaulted received higher loan amounts on average, with a median loan of $10,000 compared to $9,000 for those who fully paid their loans.
3. **Loan Application and Funding:** The distributions of loan applications, amounts issued, and amounts funded by investors are closely aligned. This suggests that borrowers who meet the qualifications are likely to receive the full amount they apply for.
4. **Interest Rate Distribution and Default Status:** The majority of interest rates were between 9% and 14%. The most common rate for defaults was 11.5%, whereas the most common rate for fully paid loans was 11%. There is a noticeable gap in the frequency data between 8% and 9%, indicating a potential under-utilization of this low interest rate range, because fewer defaulters chose the lower interest rates compared to those who fully repaid.
5. **Installment Distribution and Default Status:** The majority of installments ranged from $170 to $390. The most common installment amount for defaults was $275, whereas the most common installment amount for fully paid loans was $310. This could be due to differences in terms.
6. **Annual Income Distribution and Default Status:** The majority of annual incomes were between $40,000 and $79,000. The average annual income of charged-off borrowers was $57,000, whereas the average annual income for fully paid loans was $65,000.
7. **Debt-to-Income (DTI) Ratio Distribution and Default Status:** Defaults had a higher average DTI of 14% compared to 13% for fully paid loans. Most DTI ratios ranged from 8% to 18% for fully paid loans, while defaults had DTI ratios between 9% and 19%.
8. **Revolving Utilization Rate Distribution and Default Status:** Defaults had a higher average revolving utilization rate of 56% compared to 47% for fully paid loans. Most revolving utilization rates ranged from 24% to 71% for fully paid loans, while defaults had rates between 35% and 79%.
9. **Earliest Credit Line:** On average, the number of months since the earliest credit line for borrowers was roughly over 3 years (160 months).
10. **Open and Total Credit Lines:** The most common number of open credit lines was 7, and the most common number of total credit lines was 14-16.

#### OUTCOME:

Based on the Univariate and Segmented Univariate Analysis, we can conclude that the following quantitative attributes may be the numerical indicators for charged-off loans: **Loan Amount, Interest Rate, Annual Income, Debt-to-Income (DTI) Ratio, Revolving Utilization Rate**

#### KEY INSIGHTS FOR QUALITATIVE ATTRIBUTES

1. **Term:** The majority of loans had a term of 36 months(77%), i.e. 3 years, and it was common among both defaulters and fully paid borrowers.
   However, proportions differ: for fully paid borrowers, the ratio of 36-month to 60-month terms is 80:20, while for defaulters it is 60:40.
2. **Loan Grade:** Loans with Grade B were the most frequent (31%) among both defaulters and fully paid borrowers, followed by A(27%) and C(21%). - However, loans with Grades A(30%), B(31%) and C(20%) were the most popular among fully paid borrowers whereas lower grades B(26%), C(25%), D(20%) were more common among defaulters.
3. **Sub Grade:** Sub-Grades like A4, A5 and B3 were the most frequently issued.
   Defaulters tended to have loans with lower sub-grades, i.e. B3, B4, B5, C1, C2 compared to those who fully repaid their loans who had loans of sub-grades, A4, A5 and B3.
4. **Purpose:** The most common loan purpose was debt consolidation(46.5%). Borrowers using loans for this purpose had a higher likelihood of default compared to other purposes like home improvement or medical expenses. 48% defaulters and 46 fully paid borrowers specified debt consolidation as their loan purpose.
5. **Employment Length:** Most borrowers had an employment length of more than 10 years(24%). Borrowers with higher employment lengths had a higher rate of default compared to those with shorter employment durations. 27% defaulters and 23% fully paid borrowers more than 10 years of employment lengths.
6. **Income Category:** The majority of borrowers fell into the Medium income category(46%), followed by Low income category(42%). Defaulters were more likely to be in the Low income category(50%), whereas fully paid borrowers were predominantly in the Medium income category(46.5%).
7. **Home Ownership:** Most borrowers were either renters(49%) or had mortgages(43%). Defaulters were more likely to be renters(52%) compared to those who fully repaid their loans(49%).
8. **Verification Status:** Most borrowers were Not-Verified(45%). 40% defaulters were not-verified and 34% defaulters were verified, whereas 46% fully paid borrowers were not-verified and 29% were verified. This suggests that verification status may not effectively identify those who default.
9. **Region:** The majority of loans originated from the western regions such as the West(30%) and the MidWest(14%). Propertion of Loans emerging in these regions are similar for both Defaulters and Fully Paid Borrowers.
10. **Address State:** Loans were most commonly issued in states like California, (CA: 18%), New York (NY: 9.5%), Texas(TX: 7%), Florida (FL: 7%). Propertion of Loans emerging in these states are similar for both Defaulters and Fully Paid Borrowers.
11. **Inquiries in the Past 6 Months:** Borrowers with one(28%) or no(49%) inquiries in the past 6 months were most common.
    It is difficult to identify default rate patterns because 50.5% of the defaulters had no inquiries in the past 6 months.
12. **Issue Year:** Loans issued had been increase subsequently year on year between 2007 and 2011 in recent years, and year 2011 saw 20% increase in loan issuance and with it we saw a higher incidence of default (20% increase) compared to 2010.
13. **Issue Month:** The majority of loans were issued increases month-on-month every year, peaking in December. Defaults varied slightly by month, sharing a similar trend with the average.
14. **Issue Quarter:** Loans issued in the fourth quarter had a higher rate of default compared to loans issued in other quarters but similar trend is seen in the loans issued to fully paid borrowers as well.

#### OUTCOME:

Based on the Univariate and Segmented Univariate Analysis, we can conclude that the following qualitative attributes may be the categorical indicators for charged-off loans: **Term, Loan Grade, Purpose, Employment Length, Income Category, Home Ownership, Verification Status, Region**

### Bivariate Analysis

#### KEY INSIGHTS FOR RELATIONSHIPS BETWEEN NUMERICAL ATTRIBUTES

1. **Relationship between Loan Amount and Interest Rate:**
   - **Overall Correlation:** Weak positive correlation of 0.236 between loan amount and interest rate.
   - **Fully Paid Loans:** Correlation is 0.221, showing a slight trend that higher loan amounts are somewhat associated with higher interest rates.
   - **Charged Off Loans:** Correlation increases to 0.291, indicating a stronger trend where higher loan amounts are more closely associated with higher interest rates in defaulted loans.
   - **Charged Off Loans Density:** The scatterplot shows a higher density of points at the lower end of loan amounts and interest rates between 10% to 15%.
2. **Relationship between Loan Amount and Annual Income:**
   - **Overall Correlation:** Moderate positive correlation of 0.364 between loan amount and annual income.
   - **Fully Paid Loans:** Correlation is 0.366, indicating a moderate trend where higher annual incomes are somewhat associated with higher loan amounts.
   - **Charged Off Loans:** Correlation increases to 0.391, showing a stronger relationship where higher annual incomes are more closely associated with higher loan amounts in defaulted loans.
   - **Charged Off Loans Density:** The scatterplot shows a higher density of points at the lower end of both loan amounts and annual incomes.
3. **Relationship between Loan Amount and Debt-to-Income Ratio:**
   - **Overall Correlation:** Very weak positive correlation of 0.073 between loan amount and debt-to-income ratio.
   - **Fully Paid Loans:** Correlation is 0.071, showing a minimal trend where higher loan amounts are slightly associated with higher debt-to-income ratios.
   - **Charged Off Loans:** Correlation is 0.074, indicating a similar weak relationship in defaulted loans, where higher loan amounts are weakly associated with higher debt-to-income ratios.
   - **Charged Off Loans Density:** The scatterplot shows a higher density of points at the lower end of both loan amounts and DTIs between 10-20.
4. **Relationship between Loan Amount and Revolving Utilization Rate:**
   - **Overall Correlation:** Very weak positive correlation of 0.062 between loan amount and revolving credit utilization.
   - **Fully Paid Loans:** Correlation is 0.060, indicating a minimal trend where higher loan amounts are weakly associated with higher revolving credit utilization.
   - **Charged Off Loans:** Correlation is 0.047, showing a similar weak relationship in defaulted loans, where higher loan amounts are very weakly associated with higher revolving credit utilization.
   - **Charged Off Loans Density:** The scatterplot shows a higher density of points at the lower end of loan amounts and higher end of revolving utilization rates.
5. **Relationship between Interest Rate and Annual Income:**
   - **Overall Correlation:** Very weak positive correlation of 0.017 between interest rate and annual income.
   - **Fully Paid Loans:** Correlation is 0.021, indicating an extremely weak trend where higher annual incomes are weakly associated with slightly higher interest rates.
   - **Charged Off Loans:** Correlation increases to 0.104, showing a weak but somewhat stronger relationship where higher annual incomes are weakly associated with higher interest rates in defaulted loans.
   - **Charged Off Loans Density:** The scatterplot shows a higher density of points at the lower end of annual incomes and interest rates between 10%-17.5%.
6. **Relationship between Interest Rate and Debt-to-Income Ratio:**
   - **Overall Correlation:** Weak positive correlation of 0.105 between interest rate and debt-to-income ratio.
   - **Fully Paid Loans:** Correlation is 0.110, indicating a weak trend where higher debt-to-income ratios are slightly associated with higher interest rates.
   - **Charged Off Loans:** Correlation drops to 0.023, showing a very weak relationship where higher debt-to-income ratios have almost no association with higher interest rates in defaulted loans.
   - **Charged Off Loans Density:** The scatterplot shows a higher density of points at the central tendancy for both interest rates and DTIs.
7. **Relationship between Interest Rate and Revolving Utilization Rate:**
   - **Overall Correlation:** Moderate positive correlation of 0.476 between interest rate and revolving credit utilization.
   - **Fully Paid Loans:** Correlation is 0.483, indicating a moderate trend where higher revolving credit utilization is associated with higher interest rates.
   - **Charged Off Loans:** Correlation is 0.375, showing a slightly weaker but still moderate relationship where higher revolving credit utilization is associated with higher interest rates in defaulted loans.
   - **Charged Off Loans Density:** The scatterplot shows a higher density of points at the higher end of revolving utilization rates and mid-range interest rates (10%-17.5%).
8. **Relationship between Annual Income and Debt-to-Income Ratio:**
   - **Overall Correlation:** Weak negative correlation of -0.122 between annual income and debt-to-income ratio.
   - **Fully Paid Loans:** Correlation is -0.126, indicating a slight inverse relationship where higher annual income is weakly associated with lower debt-to-income ratios.
   - **Charged Off Loans:** Correlation is -0.073, showing an even weaker inverse relationship where higher annual income has a very minimal association with lower debt-to-income ratios in defaulted loans.
   - **Charged Off Loans Density:** The scatterplot shows a higher density of points at the lower end of annual incomes and mid-ranged DTIs(10-20).
9. **Relationship between Annual Income and Revolving Utilization Rate:**
   - **Overall Correlation:** Very weak positive correlation of 0.035 between annual income and revolving credit utilization, indicating minimal relationship.
   - **Fully Paid Loans:** Correlation is 0.035, showing a very slight positive relationship where higher annual income has a negligible association with higher revolving credit utilization.
   - **Charged Off Loans:** Correlation is 0.087, suggesting a weak positive relationship where higher annual income is weakly associated with higher revolving credit utilization in defaulted loans.
   - **Charged Off Loans Density:** The scatterplot shows a higher density of points at the lower end of annual incomes and higher ends of revolving utilization rates.
10. **Relationship between Debt-to-Income Ratio and Revolving Utilization Rate:**

- **Overall Correlation:** 0.279, indicating a moderate positive correlation between debt-to-income ratio and revolving utilization.
- **Fully Paid Loans:** Correlation is 0.285, suggesting a slightly stronger positive relationship where higher debt-to-income ratio is moderately associated with higher revolving utilization in fully paid loans.
- **Charged Off Loans:** Correlation is 0.226, showing a weaker positive relationship compared to fully paid loans, where higher debt-to-income ratios are weakly associated with higher revolving credit utilization in defaulted loans.
- **Charged Off Loans Density:** The scatterplot shows a higher density of points at the higher ends of both DTIs and revolving utilization rates.

#### OUTCOME:

Based on the Bivariate Correlation of Numerical Variables with Loan_Status, we can conclude that the following quantitative attributes may be the numerical indicators for charged-off loans: **Loan Amount, Interest Rate, Annual Income, Debt-to-Income (DTI) Ratio, Revolving Utilization Rate**

#### KEY INSIGHTS FOR BIVARIATE ANALYSIS OF CATEGORICAL ATTRIBUTES BY LOAN_STATUS

1. **Term:** Borrowers with Charged Off Loans predominantly had 36 months term by count and 60 months term by percentage.
2. **Grade:** Borrowers with Charged Off Loans mostly took B, C, D Graded loans by count and E, F, G Graded Loans by percentage.
3. **Home Ownership:** Borrowers with Charged Off Loans most likely lived in Rented houses by count and other categories by percentage but variation is very slight.
4. **Verification Status:** Borrowers with Charged Off Loans were most likely Not Verified by count and Verified by percentage but variation is very slight.
5. **Employment Length:** Borrowers with Charged Off Loans had an employment length of more than 10+ years by count and is uniform across all ages by percentage.
6. **Purpose:** Borrowers with Charged Off Loans mostly specified Debt Consolidation by count and Small-Business by percentage.
7. **Region:** Borrowers with Charged Off Loans most likely belonged to the West Region by count but is almost uniform across all regions by percentage.
8. **Income Category:** Borrowers with Charged Off Loans mostly belongs to the Low Income Category by both count and percentages.
9. **Inquiries Last 6 Months:** Borrowers with Charged Off Loans most likely had no inquiries by count and 3 inquiries by percentages, but there is only slight variation across the dataset.
10. **Issue Year, Issue Month, and Issue Quarter:** Borrowers with Charged Off Loans in general increased year-on-year, with slight variations over months and quarters by count. And by percentages, there is only slight variations in loans in years, quarters and months.

#### OUTCOME:

Based on the Bivariate Correlation of Categorical Variables with Loan_Status, we can conclude that the following qualitative attributes may be the categorical indicators for charged-off loans: **Term, Grade, Purpose, Income Category**

### KEY INSIGHTS FOR RELATIONSHIPS BETWEEN NUMERICAL DRIVERS AND CATEGORICAL DRIVERS OF DEFAULT

For Charged Off Loans, following trends were observed:

1. **Loan Amount vs. Categorical Variables:**
   - **Term:** Boxplots and violin plots show a higher median loan amount for longer-term loans (' 60 months') compared to shorter-term loans (' 36 months'). The distribution for longer-term loans is also more spread out.
   - **Grade:** Higher loan amounts are generally associated with lower grades ('E' to 'G'). Violin plots indicate that 'G' grades tend to have higher loan amounts, with a wide distribution in higher grades.
   - **Purpose:** Boxplots reveal that loan amounts do not vary significantly based on the loan purpose. Loans for 'credit card', 'debt consolidation', 'home improvement' and 'small business' show higher median amounts compared to others.
   - **Income Category:** The loan amount increases with the income category. Higher income categories show a higher median loan amount, with broader distribution in the 'High' income category.
2. **Interest Rate vs. Categorical Variables:**
   - **Term:** Interest rates are higher for long-term loans ('60 months') compared to shorted-term loans ('36 months'). The distribution is similar for both the term.
   - **Grade:** Interest rates are higher for lower grades. For instance, 'G' grades tend to have higher interest rates compared to 'A' grades.
   - **Purpose:** Different loan purposes have varied interest rates. Loans for 'house' and 'small business' have higher interest rates compared to other loans.
   - **Income Category:** Interest rates is almost similar for all income categories.
3. **Annual Income vs. Categorical Variables:**
   - **Term, Grade, Purpose:** Annual income shows no significant trend in central tendency and distribution with respect to Term, Grade and Purpose.
   - **Income Category:** The annual income increases with the income category. 'High' income category shows the highest annual income with the most significant variability. This mainly because the Income_category is a derivative of Annual Incomes.
4. **Debt-to-Income Ratio vs. Categorical Variables:**
   - **Term, Grade, Purpose:** DTI ratios show no significant trend in central tendency and distribution with respect to Term, Grade and Purpose.
   - **Income Category:** DTI ratios are higher in lower income categories. 'Low' income category shows higher median DTI ratios compared to 'High' income category.
5. **Revolving Utilization vs. Categorical Variables:**
   - **Term:** Revolving utilization is similar for both ' 36 months' loans and ' 60 months'.
   - **Grade:** Lower grades exhibit higher revolving utilization. 'F' grade borrowers, followed by G, tend to have higher utilization compared to all the other grade - borrowers, but 'G' grades have a wider distribution.
   - **Purpose:** Revolving utilization varies with loan purpose. 'Credit card' loans have a higher revolving utilization compared to 'debt consolidation' loans.
   - **Income Category:** Higher income categories show higher revolving utilization. The 'Low' income category generally exhibits wider distribution compared to 'High' income.

#### OUTCOME:

Based on the Bivariate Correlation of Numerical Variables vs Categorical Variables, we can conclude that for Charged Off Loans:

- **Loan Amount is positively correlated to Term, Grade and Income Category**
- **Interest Rate is strongly correlated to Term and Grade**
- **Annual Income is only correlated to Income Category which is expected**
- **DTI is weakly correlated to Income Category**
- **Revolving Utilization Rate is correlated to Grade and Income Category**

### Multivariate Analysis

#### KEY INSIGHTS FOR RELATIONSHIPS BETWEEN NUMERICAL DRIVERS AND CATEGORICAL DRIVERS OF DEFAULT

1. **Feature Similarity:**
   - For Fully Paid loans, loan amount, funded amount, funded amount by investors, and total principal received, exhibit strong correlations with each other. However, for Charged Off loans, the total principal received graph shows irregularities. This indicates that people usually get funding for the amount they apply for and most of the time it is the investors who are lending the money and not the company. However, the invested amount is not always retrieved as it gets Charged Off for several reasons.
   - The interest rate stands out as less correlated with loan amount, funded amount, funded amount by investors, and total principal received, suggesting it behaves independently from the amount and repayment metrics.
2. **Annual Income vs. Other Columns:**
   - **High Revolving Utilization:** Applicants with high annual income are more likely to default when their revolving utilization rate is between 80% and 100%.
   - **Home Ownership:** Defaults are more common among high-income applicants with a mortgage.
   - **Loan Purpose:** High-income defaulters often take loans for home improvement, renewable energy, or housing.
   - **Verification Status:** High-income defaulters are frequently those with verified verification status.
   - **Loan Grade:** Defaults are associated with high-income applicants who have a Grade G loan.
   - **Sub Grade:** High-income defaulters often have a Sub Grade of G4.
   - **Loan Amount:** High-income applicants default more often when the loan amount is between $25,000 and $30,000.
   - **Geographic Location:** High-income defaults are observed for loans applied in Arkansas.
3. **Loan Amount vs. Other Columns:**
   - **Home Ownership Status:** High loan amounts are linked to defaults when the home ownership status is unspecified.
   - **Loan Purpose:** Defaults occur more frequently with high loan amounts for purposes such as small business and housing.
   - **Verification Status:** High loan amounts are associated with defaults when the verification status is verified.
   - **Loan Grade:** Defaults are common among high loan amounts with Grade G.
   - **Sub Grade:** High loan amounts are tied to defaults when the Sub Grade is G4.
   - **Interest Rates:** Defaults are prevalent for high loan amounts with interest rates between 21% and 24%.
   - **Geographic Location:** High loan amounts lead to defaults more frequently in Wyoming.
4. \*\*Understanding the Demographic of the people whose loans were Charged Off:
   - **Variations in Loan Amounts:** The largest charged-off loans were given to individuals in the High Income category who took loans of Grade F for 'Major Purchases' or 'Other' purposes. The Loan Amounts were most likely smaller for the purpose of 'Renewable Energy' across all grades and income categories.
   - **Variations in Annual Income:** The highest annual incomes among charged-off loan recipients were associated with those who had mortgages, took Grade F loans, and had 8-9 years of employment. The Annual incomes were most likely smallest for those whose home ownership status was 'Other'.
   - **Variations in Interest Rates:** The highest interest rates among charged-off loan recipients were most commonly associated with Grade F and G loans, spanning all income categories, and were linked to various loan purposes. Exceptions in purpose include moving, vacation, education, and renewable energy, where the interest rates were lowest for Grades F and G.
   - **Variations in DTI ratios:** DTI ratios vary widely among individuals with charged-off loans. The highest DTI ratio was observed for borrowers with 2 years of employment, a high income category, and loans taken for major purchases.
   - **Variations in Revol_Util:** The Revolving Utilization Rate, a key indicator, highlights potential misuse of the Lending Club platform. High rates are linked to low-income individuals with less than one year of employment and 'Other' home ownership. In contrast, those with longer employment and varied home ownership show lower utilization rates.

#### OUTCOME:

Based on the Multivariate Analysis, we can conclude that for Charged Off Loans:

- **Revolving Utilization Rate is the most important indicator of Default behaviour.**
- The other Key Indicators include, Loan Amount, Interest Rate, Annual Income, DTI, Term, Grade, Purpose, Employment Length, Income Category, Verification Status, Home Ownership, Sub Grade and Address State

## Technologies Used

Data Cleaning and Manipulation, and Exploratory Data Analysis using:

- Python - version 3.11.5
- NumPy - version 1.26.4
- Pandas - version 2.2.2

Data Visualization using:

- Matplotlib - version 3.8.4
- Seaborn - version 0.13.2
- Plotly - version 5.22.0

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
