# Telecom-Marketing-Campaign-Analysis

## Problem Statement
The latest marketing campaign conducted by our telecommunications company has yielded disappointing results, with a mere 11.26% subscription conversion rate. In tackling this issue, we leveraged advanced data analytics and machine learning techniques to to uncover demographic and behavioral patterns that enhance subscription rates and refine the marketing approaches.

1.	Which specific customer attributes (e.g., age, job type, marital status) most strongly predict responsiveness to marketing campaigns?
2.	How do social and economic contexts influence the responsiveness of different customer segments to marketing campaigns?
3.	Can we identify patterns or trends in the timing or type of communication (e.g., email, phone calls) that correlate with increased customer responsiveness?

## Methodology
### Data Preparation
The raw dataset comprised 41,180 current customer entries with 21 variables covering demographics, social, economic context, and campaign interactions. Cleaning steps involved:

•	Handling Missing Values: 'Unknown' values were treated as missing and excluded.

•	Handling Outliers: Significant outliers in 'age', 'duration', and 'campaign' were addressed using the IQR method.

•	Standardizing and Transforming Data: Logarithmic transformation was applied to 'duration' and 'campaign', while StandardScaler standardized 'age' and other context features.

•	Encoding Categorical Variables: One-hot encoding via pandas get_dummies was employed, resulting in a final dataset of 26,322 entries ready for modeling.

### Data Modelling
Feature selection methods including Chi-square, Wrapper Method, and Permutation were used alongside exploratory data analysis for optimal feature selection. Machine learning models utilized encompassed:

•	Parametric Models: Logistic Regression

•	Non-parametric Models: Decision Trees, Random Forests, K-Nearest Neighbors

Preprocessing addressed imbalances in the target variable (11% yes - 89% no) through techniques like under-sampling and maintaining balanced train/validation/test sets. Maximum likelihood estimation and Bayesian estimation were applied to tune model parameters and hyperparameters. Model performance was assessed based on AUC and F1-Score metrics, with a focus on the minority group.

## Result
The Decision Tree model, employing an 80-20 under-sampling strategy, proved most effective with the highest F1 score, indicating a balanced performance between precision and recall. This model is recommended for deployment due to its ability to manage both type I and type II errors in our imbalanced dataset.
![image](https://github.com/user-attachments/assets/d72cd676-011c-4266-ba5c-c0e14ecfeadb)

### Customer Attributes Predicting Responsiveness
Our models highlight age as a critical demographic feature. Specifically, younger (under 20) and older (above 60) age groups show approximately a 40% subscription rate (Appendix 1). For the upcoming marketing campaign, the company should consider tailoring its outreach to these age groups, potentially increasing overall subscription rates by catering more precisely to these demographics.

### Influence of Social and Economic Contexts
The Euribor 3-month rate has a significant negative impact on subscription rates, underscoring the need to align marketing efforts with broader economic conditions. It is advisable to scale back on expenditure during periods of economic downturn, where higher Euribor rates correlate with lower subscription likelihood.

### Patterns or Trends in Communication
Analysis of the campaign months reveals that May, despite being the peak period for marketing activities, coincides with the lowest subscription rates. Conversely, the months of March, September, October, and December show higher receptiveness to term deposits. Future campaigns should, therefore, pivot towards these months to maximize effectiveness. 
Additionally, the data suggest that maintaining ongoing communication with previously contacted customers enhances subscription rates, and that mobile communication tends to be more effective than other methods.

## Strategic Recommendations
•	Segment Focus: Concentrate marketing efforts on the most responsive demographic segments, particularly the younger and older age groups.

•	Economic Adjustment: Adapt marketing strategies in response to national economic conditions to optimize campaign timing and budget allocation.

•	Communication Optimization: Increase focus on months with historically higher engagement and continue to engage customers who have been contacted in past campaigns. Prefer mobile communication to increase reach and effectiveness.
