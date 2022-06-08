# Ironhack Final-Bootcamp Project | Bacardi #

by Lucas Trost and Miguel Ángel Villoslada, June 2022

### Forecasting Sales Based on the Digital Commerce Channel ###
![Bacardi_brands_logo](https://user-images.githubusercontent.com/103429801/172137582-400a5c1e-e295-465b-8fe8-f9429792afdd.jpeg)

**Table of content**

  - Project Brief

  - Data
  
  - Statistical Modeling

  - Machine Learning

  - Tools and Organisation
  
  - Conclusion
  

# 1. Project Brief

We are working as data analysts for one of the largest privately held, family-owned spirits companies in the world, Bacardi. The scope of the project involves building a soundable model to predict sales based on volume. Through this work we also aim to identify trends within different countries among the most representative brands the company is producing. 

# 2. Data

Bacardi provided us with Digital Commerce sales data for the US and the Big5 EU countries. We are 
Given the depth of the dataset, we harnessed data from external sources and apply some extra creativity to enhance our model predictions. Preparing our main dataframe required some previous cleaning. Being the EU an already relevant market we dropped from our analysis the US market. We also dropped some irrelevant columns, mainly using python.

  ### 2.1 Data Engineering 

  Following to this cleaning phase we worked thoroughly in excel adding relevant features to the dataset. Our main datasources were; Bloomberg, which we used to gather consumer confidence and temperature data. We also obtanained data from the European Comission and movement data from Facebook. Ultimately we added a seasonality feature matching the seasons of the year given the seasonality nature of the demand and sales for the industry.   

  ### 2.2 Exploratory Data Analysis (EDA)

 To explore the data we used, Tableau, a visualization software that allowed us understand and gain insights about the company's products, markets and   other relevant information.


# 3. Statistical Modeling

Our first approach to estimate volume was through statistical models. The ARIMA model predicts future values based on past volumes. Given the seasonality patterns eexisting in this particular industry, we advanced our model to capture the concept of seasonal trends, ie. SARIMA.


# 4. Machine Learning Process

On our next approach to estimate volume we used machine learning models. For the first estimate we used random forest model with all the features included in the dataset. On a second iteration and using a bootstrap method of this model we assesed what variables were relevant to include in the 
a stack multiple model. By doing so we aimed to achieve the highest accuracy. Regression models used were: RandomForest, K-Nearest-Neighbours and Linear Regression models. 

Take a look at the python notebook and further anotations here[https://github.com/LucasTrost/Ironhack-Final-Project-Bacardi/blob/main/Python%20Notebook/Bacardi_Creating_Model.ipynb]


  
# 5.Tools and Organization

Python - Jupyter Notebooks for prediction and machine learning model implementations.
Tableau Public and Google Slides for visualization and analysis, dynamic and presentable graphics and charts.
Excel 
Google Slides for the presentation.
GitHub for repositories and data files.


# 6. Conclusion

I believe the two models to be of good aid for our new office in Seattle, especially the ladder. I can see us scanning the real estate market for the determined features, and calculating a rough price range, before sending out one of our agents. Because in the end, little beats the judgement and expertise of a TheAgency's agent.


