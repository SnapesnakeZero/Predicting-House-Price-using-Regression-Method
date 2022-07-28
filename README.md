# Predicting-House-Price-using-Regression-Method
## Background & Objective
**Background**: 
<br>
According through the source, it was said that the data set is collected from public dataset of Ministry of Interior during the period of June 2012 to May 2013 from two district in Taipei City, and two districts in New Taipei City, totalling four circles of supply and demand. Hence, there were four dataset. These data set will be combined into one data set.  
<br>**Objective**:
<br>
* Find insight about Taipei real estate industry in the span of data collected
* Finding factor that affect incease or decrease of house price per unit in Taipei
* Predict house price using independent variable that already identified in the journal 
## Problem Statement
**Goal**:
* Getting insight about Taipei real estate industry in the span of data collected
* Create a model that able accurately predicted house price using previously identified independent variable
<br>

**Research Question**:
<br>
* Is increase in the number of convienience store means that there will an increase in house price per unit?
* Does access to MRT stations make house price per unit increase? 
* Is there a location that had higher average price compare to other location?
* Does house age make house price per unit decrease?
* Does house price per unit increase over time?
<br>

**Expected Outcome**:
<br>
* Insights about the current market state in Taipei real estate industry
* Identified factor that affect increase or decrease of house price per unit in Taipei
* Predictive model that able to predict house price


## Data Source
The data was taken from Real estate valuation data set source from UCI Machine Learning Library: 
<br>
https://archive.ics.uci.edu/ml/datasets/Real+estate+valuation+data+set
<br>
<br>
It was mention in UCI Machine Learning Library that the data was taken for the purpose of research and was publish in Journal called Applied Soft Computing. Below attached citation pertaining the research:
<br>
<b>I-Cheng Yeh, Tzu-Kuang Hsu, Building real estate valuation models with comparative approach through case-based reasoning, Applied Soft Computing, Volume 65, 2018, Pages 260-271, ISSN 1568-4946, https://doi.org/10.1016/j.asoc.2018.01.029.</b>

## Data Dictionary
The dataset contain one csv file called `Real estate valuation data set.xlsx`. The data set contain 7 feature/column. Below will be mentioned the feature that included in the data set:
* `Transaction date` 
* `house age`
* `distance to the nearest MRT Station`
* `number of convienience stores`
* `latitude`
* `longitude`
* `house price of unit area`

## Analysis Result
![image](https://user-images.githubusercontent.com/69357406/181522189-35ead791-e154-486d-a140-d83ce1dd8ece.png)
![image](https://user-images.githubusercontent.com/69357406/181522256-e4c16729-5bb1-4ea7-9292-0ed7380d3506.png)

Based on the visualization above, I found that:
1. From the geospatial map, we know that majority of house recorded in the data base is located in populated district. But there were quite number of house that located in the non populated district. Houses located in non populated district has `house price per unit area` that were cheaper than Houses located in populated district.
2. The higher the number of convienience store means the higher the house price
3. In general, the closer distance between MRT station and houses means increase house price
4. In general, there were no spesific pattern that indicate correlation between house price and house age. But the visualization shows there were certain tendencies that consumer aftering house that age approx 10-15 years old. The reason is there were spike increase in house price that had age around 10-15 years old
5. In general, there were certain increase in houses price overtime. It is suspected that the reason why this happened is that there was an increase in inflation

## Model Result
For recap, to predict `house price per unit` I applied 6 different regression model that listed below:
1. Linear Regression
2. L1 Regularization (Lasso Regression)
3. L2 Regularization (Ridge Regression)
4. Elastic Net
5. XGB Regression
6. Random Forest Regression

Comparing the result of regression evaluation metric on each regression model (RMSE, R-Squared), I found that Linear regression generated the best score on each metric. Followed closedly by Random Forest Regression Model and Ridge Regression Model. The comparison on each model will be shown below:
1. R-Squared

![image](https://user-images.githubusercontent.com/69357406/181525330-35cbd157-233d-42f7-aee3-8e0ad3ba3b23.png)


2. RMSE

![image](https://user-images.githubusercontent.com/69357406/181525435-704cc173-fdc5-4e93-a381-81a7efa352d9.png)
<br>
Interpretation: 
* Random Forest Regression model able explain 68,9% of the observed data and had average residual distance 0,2183.
* Linear Regression model able to explain 72,7% of the observed data and had average residual distance 0,204
* Ridge Regression model able to explain 71,2% of the observed data and had average residual distance 0,210
<br>

To be able to obtain more optimum model, I applied RandomSearchCV. The goal is to find optimal parameter for the model. Below listed the result:
1. R-Squared

![image](https://user-images.githubusercontent.com/69357406/181527467-9ad0246d-36da-4feb-b89d-0eab254044c1.png)

2. RMSE

![image](https://user-images.githubusercontent.com/69357406/181527370-c6de4e98-2117-456f-a696-40b55e8d760e.png)
<br>
Intepretation: It seems that after optimizing the parameter I still getting result that shows that Linear Model is the best model for modelling the data. 




