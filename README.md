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
![image](https://user-images.githubusercontent.com/69357406/175916122-f26e721c-3e09-486c-9594-9c3a1a404e89.png)
Based on the visualization above, I found that:
1. Houses located in `latitude 24.96 - 24.98` and `longitude 121.53-121.55` had more fluctuative price and on average higher rather than the houses in other location. 
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

Comparing the result of regression evaluation metric on each regression model (RMSE, R-Squared), I found that Random Forest Regression generated the best score on each metric. The comparison on each model will be shown below:
1. R-Squared

![image](https://user-images.githubusercontent.com/69357406/175922183-0333da20-4b7a-4186-b9ed-31b48982007b.png)

2. RMSE

![image](https://user-images.githubusercontent.com/69357406/175922226-9e37cf52-c98e-44e3-ae7b-57423add87b5.png)
<br>
Interpretation: Random Forest Regression model able explain 80,4% of the observed data and had average residual distance 0,173.
<br>

To be able to obtain more optimum model, I applied RandomSearchCV. The goal is to find optimal parameter for the model. Below listed the result:
1. R-Squared

![image](https://user-images.githubusercontent.com/69357406/175924307-3c5088f0-071d-4214-b615-581460066007.png)

2. RMSE

![image](https://user-images.githubusercontent.com/69357406/175924328-3da6f8a3-5fea-4fa7-ac99-601b74488f80.png)
<br>
Intepretation: Optimizing parameter able to increase Random Forest Regression model performance. Tuned Random Forest Regression model able to explain 82,4% of the observed data and had average residual distance 0,164
## Model Feature Importance
Intepreting from the model result, it seems that the most important feature in the model is `distance to the nearest MRT Station` followed by `latitude`,`house age`,etc. Below listed visualization that shows importance of each feature in the model:
![image](https://user-images.githubusercontent.com/69357406/175924981-83aa8f3b-223f-4098-8bf2-6795cdfaf4eb.png)


