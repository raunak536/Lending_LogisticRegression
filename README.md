# Problem Statement

Given a set of attributes for an Individual, we need to determine if a credit line should be extended to them. If so, what should the repayment terms be in business recommendations? 

# Insights : 
- 20% of loans disbursed become delinquent
- Geography is the strongest predictor of someone becoming delinquent 
    - Pincode's last 2 digits which signify sectional area is the strongest predictor to be precise
    - 16, 37 and 66 have 100% delinquency rate
    - 08, 51 and 95 have 0% delinquency rate
- We built Logistic Regression model with ROC AUC of 90%, PR AUC of 78% and F1 score of 62%
- Median loan amount for : 
    - Delinquents : 14k
    - Non delinquents : 12k
- 60 month loans (30% delinquent) are twice as risky as 36 month loans (15% delinquent)

# Recommendations : 
- The lending organization should appoint people with high domain knowledge to investigate the reasons behind the high predictive power in pincode. Especially in regions where delinquency is 100%. And for the shorter term the organization to not lend to people from these highly delinquent pincodes.
- If the lending organization further needs to improve its model performance (especially precision) it should look into increasing better datasets like credit bureau records (for eg CIBIL). 
- The lending organization can also build 2 models for the 2 loan terms it offers (36 months, 60 months) because the delinquency for the 5 year loan terms is twice as much as the 3 year loan terms 