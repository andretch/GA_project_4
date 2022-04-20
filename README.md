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

Observations for traps YOY  
20XX:Map layer controls checked* : 20XX Positive Traps | 20XX Negative Traps  
- Trap numbers fluctuate YOY, positions of traps also shift across years  
- This results in fluctuating measurements of mosquito populations across years, which makes it more problematic when trying to identify areas which are prone of WNV+ (if location is standardized across years, we can identify areas/clusters through tracking prior WNV positive counts in previous years).  

Observations for Coinciding Traps and Sprays  
- 2011: Map layer controls checked* : 2011 Positive Traps | 2011 Sprays  
Based on the visualization, we see only one trap location(T223) have coincided with the spraying efforts. As the spraying was conducted on 07-09-2011, lets take a look at the trap information prior to spraying date.  

2013: Map layer controls checked* : 2013 Positive Traps | 2013 Sprays  
- 2013 was a year where there were significantly more coinciding sprays with traps with coverage within the 1.3km radius of their coinciding traps. There were two areas (Garfield Park, Greater Grand Crossing) where the decision made for spraying may not have been caused by the observations made through the traps.  

![](https://github.com/andretch/GA_project_4/blob/master/images/index.html)
Figure 2: Spray Visualization

## 4. Recommendations and Conclusion  
[Return to top](#Table-of-Contents)  



## 5. Future Steps  
[Return to top](#Table-of-Contents)  
