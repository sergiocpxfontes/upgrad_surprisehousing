# Surprise Housing
> This project aims to utilize machine learning techniques to predict the actual value of the prospective properties and decide whether to invest in them or not. Its based on a regression model that uses regularization. Linear Regression, Ridge Regression and Lasso Regression are used and compared.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Analisys](#analisys)
* [Conclusions](#conclusions)
* [Final Notes](#final-notes)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price.
- The company is looking at prospective properties to buy to enter the market. For the same purpose, the company has collected a [data set](train.csv) from the sale of houses in Australia. A detailed explanation of the data set can be found [here](data_description.txt)
- The subjective questions PDF file can be found [here](SubjectiveQuestions.pdf)

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->
## Analysis

During our analisys we executed a set of actions that we describe briefly bellow:

- Data inspection.
- Null values handling.
- Dummy variables processing.
- Derived variables calculation.
- Residual error analisys for numerical variables.
- Correlation between dummy variables studies.
- Outliers replacement.
- Data cleanup.

These actions allowed us to prepare the data set for Model Building.

On the model building stage:

 - the data set was split into 2 sets (independent variables and SalesPrice, what we want to predict).
 - The independent variables set was scaled.
 - Training and Test sets created with a 70:30 ratio.
 - Linear Regression Model was built.
 - Ridge Regression Model was built.
 - Lasso Regression Model was built.
 - GridSearchCV for cross validation.

On the [Jupyter notebook file](housing_market.ipynb) you will find all the above mentioned actions and the calculations used to present the [conclusions](#conclusions) and [final notes](#final-notes).

## Conclusions
- The linear regression model is overfitting when comparing the R2 on the test and training data.
 - When we applied the regression model to the numerical variables only we got a R2 score of 78% but an huge RSS. After the residual analisys we can see that non-linearity is present on the data but we could not found derived variables (using log, exp or square) that would fit the conditions of linear regression.
 - The dummy variables handling resulted in a dataset of 290 columns and after correlation analisys using heatmaps it was possible to reduce the the data set to 267.   
- The Ridge regression model resulted in R2 scores of 94% and 68% on training and test data respectivly.
 - The optimal value of alpha for Ridge Regression was 100 (based on the values considered and present on the jupyter notebook file).
- The Lasso regression model resulted in R2 scores of 94% and 47% on training and test data respectivly. 
 - The optimal value of alpha for Lasso Regression was 500 (based on the values considered and present on the jupyter notebook file).
- GrLivArea, OverallQuality, YearBuilt and PoolQC_Gd seem to have a big impact on the price:
 - GrLivArea (Above grade (ground) living area square feet) has a positive impact;
 - OverallQuality (Rates the overall material and finish of the house) when above 5 (average) as positive impact when bellow as a negative impact
 - YearBuilt has a positive impact;
 - PoolQC strangely seems to have a negative impact on the price. 

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->
## Final Notes

The conclusions mentioned on the previous section result of what was observer but:

- Its clear that the models are overfititng, the degradation of the R2 scores from trainig to test data and the values of the RSS confirms it:
 - The best model its the one that reduces the RSS and this was not the case.
- It will be necessary to review again the independent variables identify colinearity and determine witch ones don't bring any added value to the models.
- A possible way to start would bee to look at the variables where the Lasso Regression determined coefiecient of 0 value.
- Outliers need to be better identified and handled.

## Technologies Used
- Library - Pandas 1.4.1
- Library - NumPy
- Library - Seaborn
- Library - MatplotLib

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Contact
Created by [@sergiocpxfontes] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
