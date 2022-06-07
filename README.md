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

Bacardi provided us with Digital Commerce sales data for the US and the Big5 EU countries. 
Given the depth of the dataset, we harnessed data from external sources and apply some extra creativity to enhance our model predictions. Preparing our main dataframe required some previous cleaning. Being the EU an already relevant market we dropped from our analysis the US market. We also dropped some irrelevant columns, mainly using python.

  ### 2.2 Engineering Data

  Following to this cleaning phase we worked thoroughly in excel adding relevant features to the dataset. Our main datasources were; Bloomberg, which we used to gather consumer confidence and temperature data. We also obtanained data from the European Comission and movement data from Facebook. Ultimately we added a seasonality feature matching the seasons of the year given the seasonality nature of the demand and sales for the industry.   

  ### 2.1 Exploratory Data Analysis (EDA)

 To explore the data we used, Tableau, a visualization software that allowed us understand and gain insights about the company's products, markets and   other relevant information.

Feel free to explore the Tableau and/or the presentation slides


# 3. Statistical Modeling

hat module is Statsmodels. It is probably my favorite Python module when I need to perform statistical calculations. This library/module is based on the SciPy Python library and it is a complete module that allows the user to perform numerous operations for statistical analysis

Statistical modelling gives you the ability to asses, understand and make predictions about data

he Statsmodels package allows you to perform all these analyses

Time series analysis

Model for estimating volume
K-Nearest Neightbours




4. Machine Learning Process

Linear Regression Model
I first started with a base line Linear Regressions model. After drafting two more Candidates where I played with choosing between the highly correlating columns around the size of the property (sqft_living,sqft_living15,sqft_above, etc.) and getting no real improvement in accuracy I decided to move on to the next model.

K-Nearest-Neighbours Regression Model
The base model alone showed more promising results than the previous candidates, with an increase in accuracy and a decrease in Root Mean Squared Error (RMSE).
Pre-Modeling
Besides EDA there were a few necessary steps to take, in order to ensure valid results end results The most notable steps here were:




Scaling
As our DataFrame had vastly differentiating number ranges, and consisted of only numerical columns, I decided it would be best to apply a MinMaxScaler() to the entire DataFrame.

Model for estimating volume

Decision Tree Regression Model
Already being fairly content with my KNN model, I only planned to briefly dip into decision trees. With the base model returning an accuracy of 64%, 8% worse than the KNN, I was more than happy to move on.

Model to determine importance of features
As already mentioned we, TheAgency, are quite the luxurious real-estate-agency. Thus we were especially interested in houses with a value equal to and greater than $650k. Here a simple pandas query did the trick.

Random Forest Regression Model
To determine feature importance one could've based their answer on a correlation matrix. We as a agency, however, have to keep our standards high, which is why I opted for a ensemble method of the Random Forest Regressor. I then ran the model through a inspection method, which gave me my final results. Screenshot 2022-05-12 at 17 47 27

take a look at my python notebook and further anotations here

  
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
