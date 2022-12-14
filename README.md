# Loan Credit Risk Prediction
---
*Tools : Python, Google Colab, Numpy, Pandas, Scipy, Matplotlib, Seaborn, Scikit-Learn*

Data Dictionary : [Lending Club Data Dictionary](https://resources.lendingclub.com/LCDataDictionary.xlsx)

LendingClub is a financial services company headquartered in San Francisco, California. It was the first peer-to-peer lender to register its offerings as securities with the Securities and Exchange Commission, and to offer loan trading on a secondary market.

## Project Background
---
Credit risk is the possibility of a loss resulting from the borrower’s failure to repay a loan or meet contractual obligations. When a credit company receives a loan application, the company has to make a decision whether the company will accept or decline based on the applicant’s profile. For now, `Lending Club has a 12,29% bad loan` from 2007-2016. We have to increase Lending Club amount financed and decrease Lending Club bad loan status accepted by :
- Analyze client’s historical credit applications data to understanding the borrower’s behaviors.
- Develop predictive model to solve credit default issues.

## Exploratory Data Analysis
---
We have some interesting insights from the EDA, there are :

![Bad Loan Rate](https://github.com/muhhendrah/Loan-Credit-Risk-Prediction/blob/main/images/Bad%20Loan%20Rate.png)

*Key Takeaway*
- Lending Club has a 12,29% bad loan rate from 2007-2016.
<br><br>

![Borrowers Employmeny Title](https://github.com/muhhendrah/Loan-Credit-Risk-Prediction/blob/main/images/Employment%20Title.png)

*Key Takeaway*
- Most borrowers employment title are teacher, manager, and registered nurse.
<br><br>

![Loan Purpose](https://github.com/muhhendrah/Loan-Credit-Risk-Prediction/blob/main/images/Credit%20Purpose.png)

*Key Takeaway*
- Most borrowers apply loans for the purpose of debt consolidation and credit card.
<br><br>

![Relevant Credit Scorecard](https://github.com/muhhendrah/Loan-Credit-Risk-Prediction/blob/main/images/Relevant%20Credit%20Scorecard.png)

*Key Takeaway*
- Lending Club's credit scorecard still relevant, because it seems to have a natural order based on the loan status probability. Grade A has the highest probability to have a good loan status. Grade G has the lowest probability to have a good loan status.
<br><br>

![Loan Date](https://github.com/muhhendrah/Loan-Credit-Risk-Prediction/blob/main/images/Loan%20Date%20Bad%20Status.png)

*Key Takeaway*
- The earlier the loan date is, the higher the probability of a borrower to have a bad loan status.
<br><br>

![Interest Rate](https://github.com/muhhendrah/Loan-Credit-Risk-Prediction/blob/main/images/Interest%20Rate%20Bad%20Status.png)

*Key Takeaway*
- Borrowers with high-interest rates have a higher probability to have a bad loan status than those with a low-interest rate.

## Data Preprocessing
---
- Feature Engineering
- Handling Duplicate Value
- Feature Encoding
- Data Transformation
- Outlier Handling
- Feature Selection

## Modeling
---
Random Forest Model are tested with AUC-ROC and Kolmogorov-Smirnov as Evaluation Target to find the optimal value between Maximize True Positive Rate and Minimize False Positive Rate. `Turns out the optimal value goes to 83.64% AUC-ROC Score and 53.65% KS Score`. In the credit risk modeling practice, `AUC above 0.7 and KS above 0.3 are considered as a good performances`.

## Business Insights & Recommendation
---

Recommendations:
1. Use the predictive model to make a decision either accept or decline the borrower’s credit application can decrease Lending Club bad loan status accepted up to 7.73%.
2. Evaluate and do some adjustment to the interest rate. Maybe we can adjust the interest rate based on borrowers’ default risk probability.
3. We should pay more attention to borrowers' loan dates because they tend to be late in their last payments.
4. Use segmented marketing for potential new borrowers to increase finance amount based on their needs and occupations.
