# US-HOME-PRICES-DATA-SCIENCE

Welcome to our "Exploring US Home Price Trends" project! We're diving into data to figure out what has been influencing home prices in the United States over the last 20 years. Using data and advanced techniques, we want to build a model that helps us understand how different factors relate to home prices. 

# The Tools & Libraries used for this Project :

- Programming Languages: Python
- Data Analysis Libraries: NumPy, pandas, matplotlib, seaborn
- Machine Learning Libraries: scikit-learn
- Data Visualization: Matplotlib, Seaborn
- Version Control: Git, GitHub
- Jupyter Notebooks for data exploration and analysis
  
# DATA COLLECTED:

The S&P Case-Shiller U.S. Home Prices Index is influenced by various economic and demographic factors. Among the options you've listed, the main key factors that impact the S&P Case-Shiller U.S. Home Prices Index include:

1. POPTHM (Population)
   - Changes in the population size and demographics can impact the demand for housing, subsequently influencing home prices.

2. GDP (Gross Domestic Product)
   - The overall economic performance, as measured by GDP, can affect consumer confidence, income levels, and housing demand, all of which impact home prices.

3. MORTGAGE RATE
   - Fluctuations in mortgage rates affect affordability, which in turn influences the demand for housing and housing prices.

4. HOUSING STARTS (HOUST)
   - The number of new housing units under construction reflects current and future supply in the housing market, impacting home prices.

5. MEDIAN SALES PRICE (MSPUS)
   - This directly reflects changes in the prices of homes sold within the market and serves as an indicator of market conditions.

6. HOMEOWNERSHIP RATE (RSAHORUSQ1565)
   - Changes in the homeownership rate can influence the balance of supply and demand in the housing market, impacting home prices.

7. UNRATE (Unemployment Rate)
   - Employment and income levels impact the ability and willingness of individuals to purchase homes, thus affecting home prices.

These key factors play significant roles in influencing the S&P Case-Shiller U.S. Home Prices Index and are important considerations for understanding the dynamics of the housing market.
# Feature Selection:
In our analysis, we found certain important characteristics that are closely related to the S&P Case-Shiller Home Price Index.   
US HOME PRICE INDEX        1.000000
MEDIAN SALES PRICE         0.816619
GROSS DEMOSTRIC PRODUCT    0.741920
POPULATION                 0.536711
HOUSING STARTS             0.418920
MORTGAGE RATE             -0.004776
HOMEOWNERSHIP RATE        -0.145760
UNEMP RATE                -0.519985
 When a correlation value is positive, it means there is a direct relationship with home prices, while negative values indicate an inverse relationship. Features with higher absolute correlation values have a bigger impact on home prices.
 
# Model Selection & Cross_Validation:

In this project, we used the Lasso regression model to address significant collinearity within the dataset. The Lasso model employs L1 regularization to handle collinearity, promoting sparsity in feature coefficients.

To enhance the Lasso model's performance and determine the best regularization hyperparameter (alpha), we conducted cross-validation.

The optimal alpha value was found to be 0.0001. 
During cross-validation, the R-squared scores for different folds were as follows:

Fold 1: 0.9384        
Fold 2: -0.0281
Fold 3: 0.9457
Fold 4: 0.7558
Fold 5: 0.8689
![download](https://github.com/Samineni-Jayaprakash/US-HOME-PRICES-DATA-SCIENCE/assets/144466020/7d086f29-66c0-4eaf-9d3b-2672a6a6d41b)
* mean R_squared:0.6961
* standard deviation on R_squared:0.3685
  
# BEST FEATURES WITH NON_ZERO_COEFFICIENTS:

Our Lasso regression model identified certain features with non-zero coefficients:

 Feature	          Coefficient
HOMEOWNERSHIP RATE	  0.073474
HOUSING STARTS	      0.053351
MEDIAN SALES PRICE	  0.091066
MORTGAGE RATE	        0.022082
POPULATION	          0.114393
UNEMP RATE	         -0.031504

signifying their impact on predicting home prices.
Positive coefficients indicate a direct relationship with home prices, while negative coefficients suggest an inverse relationship.

# FEATURES WITH ZERO_COEFFICIENTS :

In our analysis, we found that one features had coefficients of 0.0,
Feature	                  Coefficient
GROSS DEMOSTRIC PRODUCT	   -0.0
this features  do not have a significant impact on the prediction of home prices in our model.

# SOURCE
https://fred.stlouisfrd.org/
