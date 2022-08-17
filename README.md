# Surprise Housing
> This project aims to utilize machine learning techniques to predict the actual value of the prospective properties and decide whether to invest in them or not. Its based on a regression model that uses regularization. Linear Regression, Ridge Regression and Lasso Regression are used and compared.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Analisys](#analisys)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price.
- The company is looking at prospective properties to buy to enter the market. For the same purpose, the company has collected a [data set](train.csv) from the sale of houses in Australia. A detailed explanation of the data set can be found [here](data_description.txt)
- MISSING extra questions PDF

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->
## Analysis

During our analisys we executed a set of actions that we describe briefly bellow:

- Data inspection
- Null values handling
- Dummy variables processing
- Derived variables calculation
- Residual error analisys for numerical variables
- Correlation between dummy variables studies
- Outliers replacement
- Data cleanup

These actions allowed us to prepare the data set for Model Building.

On the model building stage:

 - the data set was split into 2 sets (independent variables and SalesPrice, what we want to predict)
 - the independent variables set was scaled
 - Training and Test sets created with a 70:30 ratio
 - Linear Regression Model was built
 - Ridge Regression Model was built
 - Lasso Regression Model was built
 - GridSearchCV for cross validation


## Conclusions
- The linear regression model is overfitting when comparing the R2 on the test and training data.
-   When we applied the regression model to the numerical variables only we got a R2 score of 78% but an huge RSS. After the residual analisys we can see that non-linearity is present on the data but we could not found derived variables (using log, exp or square) that would fit the conditions of linear regression   
- Conclusion 2 from the analysis
- Conclusion 3 from the analysis
- The best hyperparameter for Ridge Regression was 100
- The best hyperparameter for Lasso Regression was 500
- 

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- Library - Pandas 1.4.1
- Library - NumPy
- Library - Seaborn
- Library - MatplotLib

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- This project was inspired by...
- References if any...
- This project was based on [this tutorial](https://www.example.com).


## Contact
Created by [@sergiocpxfontes] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
