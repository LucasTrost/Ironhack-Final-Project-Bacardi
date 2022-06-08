# Ironhack Final-Bootcamp Project | Bacardi #

by Lucas Trost and Miguel Ángel Villoslada, June 2022

### Forecasting Sales Based on the Digital Commerce Channel ###
![Bacardi_brands_logo](https://user-images.githubusercontent.com/103429801/172137582-400a5c1e-e295-465b-8fe8-f9429792afdd.jpeg)

**Table of content**

  - [Project Brief](#section1)

  - [Data](#section2)
  
  - [Statistical Modeling](#section3)

  - [Machine Learning](#section4)

  - [Tools](#section5)
  
  - [Conclusion](#section6)
  
<a id='section1'></a>
# 1. Project Brief

We are working as data analysts for one of the largest privately held, family-owned spirits companies in the world, Bacardi. The scope of the project involves building a soundable model to predict sales based on volume. Through this work we also aim to identify trends within different countries among the most representative brands the company is producing. 

<a id='section2'></a>
# 2. Data

Bacardi provided us with Digital Commerce sales data for the US and the Big5 EU countries. We are 
Given the depth of the dataset, we harnessed data from external sources and apply some extra creativity to enhance our model predictions. Preparing our main dataframe required some previous cleaning. Being the EU an already relevant market we dropped from our analysis the US market. We also dropped some irrelevant columns, mainly using python.

  ### 2.1 Data Engineering 

  Following to this cleaning phase we worked thoroughly in excel adding relevant features to the dataset. Our main datasources were; Bloomberg, which we used to gather consumer confidence and temperature data. We also obtanained data from the European Comission and movement data from Facebook. Ultimately we added a seasonality feature matching the seasons of the year given the seasonality nature of the demand and sales for the industry.   

  ### 2.2 Exploratory Data Analysis (EDA)

 To explore the data we used, Tableau, a visualization software that allowed us understand and gain insights about the company's products, markets and   other relevant information.

<a id='section3'></a>
# 3. Statistical Modeling

Our first approach to estimate volume was through statistical models. The ARIMA model predicts future values based on past volumes. Given the seasonality patterns eexisting in this particular industry, we advanced our model to capture the concept of seasonal trends, ie. SARIMA.

[Take a look at the python notebook here](https://github.com/LucasTrost/Ironhack-Final-Project-Bacardi/blob/main/Python%20Notebook/Bacardi_Creating_Model.ipynb)

<a id='section4'></a>
# 4. Machine Learning Process

On our next approach to estimate volume we used machine learning models. For the first estimate we used random forest model with all the features included in the dataset. On a second iteration and using a bootstrap method of this model we assesed what variables were relevant to include in the 
a stack multiple model. By doing so we aimed to achieve the highest accuracy. Regression models used were: RandomForest, K-Nearest-Neighbours and Linear Regression models. 

[Take a look at the python notebook here](https://github.com/LucasTrost/Ironhack-Final-Project-Bacardi/blob/main/Python%20Notebook/Bacardi_Creating_Model.ipynb)

<a id='section5'></a>  
# 5.Tools

    Python - Jupyter Notebooks for prediction and machine learning model implementations.

    Excel for data engineering and pre-processing

    Tableau Public for visualization and analysis. Used also for the presentation (graphics)

    Google Slides for presentation template and contents

    GitHub for repositories and data files

<a id='section6'></a> 
# 6. Conclusion

We believe that COVID-19 pandemic affected key trends driving the global beverage alcohol industry. The industry has proven itself to be one of the most crisis-proof consumer goods categories at a time of significant disruption. Even though consumers are very keen returning to the on-trade channels digital Commerce has emerged in strength. 

Here are the key trends driving the beverage alcohol market landscape for Bacardi:

Premium brands have gained protagonism for our EU Big5 market. This indicates a consumption habit change on its own means. 


