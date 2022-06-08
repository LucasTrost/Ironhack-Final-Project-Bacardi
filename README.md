# Ironhack Final-Bootcamp Project | Bacardi #

by Lucas Trost and Miguel Ángel Villoslada, June 2022

### Forecasting Sales Based on the Digital Commerce Channel ###
![Bacardi_brands_logo](https://user-images.githubusercontent.com/103429801/172137582-400a5c1e-e295-465b-8fe8-f9429792afdd.jpeg)

**Table of content**

  - Project Brief

  - Data
  
  - Statistical Modeling

  - Machine Learning

  - Conclusions


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

On our next approach to estimate volume we used machine learning models. We assesed the importance of our set of features learning their relevance and applied the K-Nearest Neighbors, Linear and Random Forest Regression Models. 
 

The k-nearest neighbors algorithm, also known as KNN or k-NN, is a non-parametric, supervised learning classifier, which uses proximity to make classifications or predictions about the grouping of an individual data point.

Model to determine importance of features

Take a look at my python notebook and further anotations here




Decision Tree Regression Model
Already being fairly content with my KNN model, I only planned to briefly dip into decision trees. With the base model returning an accuracy of 64%, 8% worse than the KNN, I was more than happy to move on.



Random Forest Regression Model
To determine feature importance one could've based their answer on a correlation matrix. We as a agency, however, have to keep our standards high, which is why I opted for a ensemble method of the Random Forest Regressor. I then ran the model through a inspection method, which gave me my final results. Screenshot 2022-05-12 at 17 47 27


______________________________________________________
  
Organization
Jupyter Notebooks for data exploration, visualization, analysis and machine learning model implementations.
Tableau Public for dynamic and presentable graphics and charts.
GitHub for repositories and data files.
Google Slides for the presentation.

Key Take Aways
Model for estimating price:
With an accuracy of 72.25% and a RSME of $195k the model is fairly accurate, but no where close for us, TheAgency, to solemnly rely on it for price determination.

Model to determine importance of features
Here the results seem alot more promising, as wee gained a clear guideline as to which features determine high prices.

Overall conclusion
I believe the two models to be of good aid for our new office in Seattle, especially the ladder. I can see us scanning the real estate market for the determined features, and calculating a rough price range, before sending out one of our agents. Because in the end, little beats the judgement and expertise of a TheAgency's agent.
