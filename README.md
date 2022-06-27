# Predicting-House-Price-using-Regression-Method
# Customer_Segmentation_Online_Marketplace
**Important Note: Because the excel file size is too huge, to access the original dataset, please download it through link source below**
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
<br>

**(Note: We will do RFM Analysis and combine it with predictive algorithm to achive in depth insight)**

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

## Conclusion
By looking through regression evaluation metric (R-Squared and RMSE), 

