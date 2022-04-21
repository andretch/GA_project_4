## Table of Contents
1. [Problem Statement](#1-Problem-Statement)  
2. [Executive Summary](#2-Executive-Summary)
3. [EDA Preview](#3-EDA-Preview)
4. [Recommendations and Conclusion](#4-Recommendations-and-Conclusion)  
5. [Future Steps](#5-Future-Steps)


## 1. Problem Statement
[Return to top](#Table-of-Contents)

- Using given data, generate a model to predict outbreaks of West Nile Virus to help the City of Chicago better allocate resources towards preventing transmission of WNV.  

- Develop and choose a suitable model between:  
	- Logistic Regression  
	- K Nearest Neighbours  
	- Decision tree  
	- Random Forest  
	- AdaBoost  

- Stakeholders:
    - Primary stakeholders: City of Chicago and the Chicago Department of Public Health (CDPH)  
    - Secondary stakeholders: General public for awareness


## 2. Executive Summary  
[Return to top](#Table-of-Contents)  

Following the Data Science workflow:  
- Data Cleaning  
- Pre-Processing  
- EDA  
- Feature Engineering  
- Modeling  
	- Logistic Regression  
	- K Nearest Neighbours  
	- Decision tree  
	- Random Forest  
	- AdaBoost  

AdaBoost was evaluated to be the best predictor model with a recall score of 0.901   

## 3. EDA Preview  
[Return to top](#Table-of-Contents)  

![](https://github.com/andretch/GA_project_4/blob/master/images/traps.gif)  
Figure 1: Traps Visualization

## 4. Recommendations and Conclusion  
[Return to top](#Table-of-Contents)  

**Recommendations**  
Based on the AdaBoostClassifier predictions and it's identified feature importances, here are our recommendations:  

- Identify corresponding traps with lat,long values and commence spraying in a radius of 1.3km around these traps a month in advance prior, with attention given to maintain spray intervals of not longer than two weeks.  
- Positive traps which have another trap in it's vincinity of 1.3km should also be sprayed due to the flight ranged previously researched (referenced in combined EDA notebook) on WNV carrying species (Restuans/ Pipiens).  
- Better trap laying procedures (Standardized trap locations)  
It was observed during the EDA process that trap locations are seldom similar across years, which might hinder proper identification of areas prone to WNV (consecutive years of WNV+ during peak seasons).  
- Provision of data in increased quality and quantities  
Data provided for our model to be trained on were only for months to be peak season, it would be better to provide the full range of data for an entire year. Should traps no be tested during winter months, methods can be used to impute the values of these traps ( 0 or mean for past/present year) to better account for the variability of weather data for a given trap.  


**Conclusion**  
In this project, we cleaned and explored the traps, spray and weather data of Chicago to learn about how each of them plays a part with regards to the mosquito population in Chicago and its relationship to the presence of West Nile Virus(Wnv). Using learned relationships during EDA and visualizations, using the data science process we also used a selection of classifiers to predict potential positive traps to serve as a guide for timely effective allocation of resources.  

The classsification model we trained gave us a decent ROC-AUC score of ~0.778, and very good recall score of ~0.901. We also learned about possible pitfalls when our scores can be seem optimistic but not necessarily predict well on future data when the look ahead bias is introduced.  

In the cost-benefit analysis(CBA) we also explored the quantification of cost when a positive trap misclassified as negative as well as a negative trap misclassfied as positive. Additionally, the CBA also covered the breakeven point in terms of number of WNV cases prevent as a result of spraying for cost justification. We also covered the intangible aspects of the WNV such as the grief and disruption in brings to patients. The potential of WNV to bring about severe life-threathening diseases/risk of permanent disability also highlights the importance of prevention rather than cure as every life lost/ severely disrupted due to WNV is one too many.  
 
https://www.cdc.gov/westnile/prevention/index.html  

## 5. Future Steps  
[Return to top](#Table-of-Contents)  

As mentioned in the CBA, in order to identify which traps to prioritise spraying, we would need more information based on the actual estimates of population density by neighbourhood or district to better estimate the number of people covered by a trap radius of 1.3km, as opposed to the entire population count of Chicago over the area of Chicago.
Since WNV is spread through vectors like mosquitoes and other animals like bird and horses, we can also flag parks, stables and ranches as potential harbours of WNV+, traps placed near sites such animals which are flagged positive can give an indication as to whether animals are carrying the virus.
We can also look to identify the unidentified species of mosquitoes as there might be new species which are capable of carrying the virus in future.
