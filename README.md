Telecom Customer Churn Analysis

#### 1. Dataset Overview
The dataset consists of 7,043 entries and 21 features, covering various customer details, including demographics, service subscriptions, account information, and churn status.

##### Key Features:

Customer Demographics: gender, SeniorCitizen, Partner, Dependents

Service Details: PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies

Account Information: Contract, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges

Target Variable: Churn (Yes/No)

#### 2. Data Preprocessing and Cleaning

Missing Values: Only the TotalCharges column had 11 missing values, which were replaced with 0 after converting to numeric format.

Data Types: Corrected data types for TotalCharges to ensure compatibility in analysis.

#### 3. Exploratory Data Analysis
##### 3.1 Univariate Analysis

Customer Tenure:

    The average tenure is 32.37 months, ranging from 0 to 72 months.
    25% of customers have tenures of 9 months or less, indicating a potential for early churn.
    Monthly Charges:
    The average monthly charge is $64.76, with charges ranging from $18.25 to $118.75.
    The median monthly charge of $70.35 suggests many customers are on mid to high-tier plans.
    
Churn Distribution:
    26.5% of customers have churned (Yes: 1,869 customers), while 73.5% (No: 5,174 customers) are retained.
3.2 Service Subscription Insights:

Phone Service:

    6,361 customers have a phone service, while 682 do not.
    Among those with phone service, 53.3% prefer single lines (3,390 customers), compared to 46.7% with multiple lines (2,971 customers).
Internet Service:
    Fiber optic is the most popular service, with 3,096 users, followed by DSL with 2,421 users.
    1,526 customers do not use any internet service, presenting an opportunity for market expansion.
Security and Backup Services:
    Online Security: Only 2,019 customers have opted for this, indicating room for upselling since 3,498 do not use it.
    Online Backup: Slightly higher adoption at 2,429 customers, but still 3,088 do not use it.
Payment Method Insights:
    The majority of churn occurs with electronic check payments (57% churn rate), highlighting a potential issue with this method. In contrast, customers using automatic payments (bank transfer or credit card) have significantly lower churn rates.
    
##### 4. Bivariate Analysis

Tenure and Churn:
    Customers with shorter tenures (less than 12 months) have higher churn rates, indicating early-stage retention challenges.
    
Contract Type and Churn:
    Month-to-month contracts exhibit the highest churn rates (43% churn), while two-year contracts have the lowest (3% churn), showing customer commitment is linked to contract duration.
    
Monthly Charges and Churn:
    Higher monthly charges are correlated with increased churn. Customers paying above $70 per month are more likely to leave.
    
Payment Method and Churn:
    Customers paying via electronic check have a significantly higher churn rate (45%), suggesting issues related to this payment method.
    
##### 5. Multivariate Analysis
Correlation Analysis:
    TotalCharges and tenure have a strong positive correlation (0.83), as expected due to longer tenures accumulating higher total charges.
    MonthlyCharges has a moderate correlation with TotalCharges (0.65), reflecting diverse service packages chosen by customers.
    
Churn Rate Analysis with Categorical Features:
    Contract Type and Payment Method: Month-to-month contracts with electronic check payments exhibit the highest churn rates.
    Internet Service and Tech Support: Fiber optic users without tech support have the highest churn, suggesting the need for better customer support.
    
Feature Combination Analysis:
    A heatmap analysis shows that Fiber Optic users with no Tech Support are at the highest risk of churn.
    Customers on month-to-month contracts with Paperless Billing and Electronic Check Payment show the highest propensity to churn.
    
#### 6. Conclusions
Churn Drivers:
High monthly charges, short tenure, flexible contracts (month-to-month), and specific payment methods (electronic check) are primary churn drivers.
Actionable Steps:
Implement targeted retention campaigns for short-tenure customers and those on high-tier plans.
Educate customers about the advantages of secure and backup services, which may enhance satisfaction and retention.
This analysis provides a comprehensive view of factors influencing customer churn and offers actionable strategies to reduce churn rates and enhance customer satisfaction.
