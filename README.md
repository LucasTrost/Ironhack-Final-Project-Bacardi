# Ironhack Final Project | Bacardi #

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

We are working as data analysts for one of the largest privately held, family-owned spirits companies in the world, Bacardi. The scope of the project involves building a soundable model to predict sales based on volume. 

Through this work we also aim to identify country specific trends among the company's most represented categories.
<a id='section2'></a>
# 2. Data

Bacardi provided us with Digital Commerce sales data for the US and the Big5 EU countries, which only required minimal cleaning and some forms of reformatting (dropping columns). As the files only included data concerning the fiscal years: 2020, 2021, and 2022, we harnessed data from external sources and applied some extra creativity in order to enhance our model's predictions. 

We also adjusted the scope of our project by excluding the US marlet from our analysis.

  ### 2.1 Exploratory Data Analysis (EDA)

To explore the data we used, Tableau, a visualization software that allowed us understand and gain insights about the company's products, markets and   other relevant information.

  ### Proclaimer: 
 Due to company regulations, data sets will not be published.

<a id='section3'></a>
# 3. Statistical Modeling

Our first approach to estimate volume was through statistical models. The ARIMA model predicts future values based on past volumes. Given the seasonality patterns eexisting in this particular industry, we advanced our model to capture the concept of seasonal trends, ie. SARIMA.

<a id='section4'></a>
# 4. Machine Learning Process

  ### 4.1 Data Engineering 

In order to create a solid machine learning model we worked thoroughly in excel, adding relevant features to the dataset. 

One of our main datasources was Bloomberg, which we used to gather consumer confidence and temperature data. Additionally we obtained data from the European Comission and movement data from Facebook. 

Ultimately we added a feature matching the seasons of the year given the seasonality nature of the demand and sales for the industry.   

  ### 4.1 Modeling
  
 With our expanded data set we were ready to head into the modeling process. We started by boosting our data through selecting the most important features. This we accomplished by using the feature importances method of the random forest regression. In the second step we used the same model to create our first forecast.  The data we receive from bacardi only spanned over the course of three years, thus making it hard to set up a proper train and test scenario. Because of this we decided to stabilise our model as far as possible via ###stacking###. Through this process we combined the regression models: RandomForest, K-Nearest-Neighbours and Linear Regression. 


[View our python notebook here](https://github.com/LucasTrost/Ironhack-Final-Project-Bacardi/blob/main/Python%20Notebook/Bacardi_Creating_Model.ipynb)


<a id='section5'></a>  
# 5. Tools

   Python - Jupyter Notebooks for prediction and machine learning model implementations.

   Excel -  Data engineering and pre-processing

   [Tableau Public](https://public.tableau.com/app/profile/lucas.trost/viz/Ironhack-Final-Project-Barcardi/CountryForecast) - Visualizations, analysis, Presentation (project managers)
    
   [Google Slides](https://docs.google.com/presentation/d/e/2PACX-1vSI9lEiMGfcXcfaol6NwdTXmpoC0GeTFpIdF1lDuAyEVI3LP4Z9lc5pUQTfJy9RNMmePrrJ67BvwnTn/pub?start=false&loop=false&) - Presentation template and further contents (diagrams)

   GitHub - Repositories and data files
    
   Trello Board - Agile project management

<a id='section6'></a> 
# 6. Conclusion

We believe that COVID-19 pandemic affected key trends driving the global beverage alcohol industry, especially in the e-commerce sector. The industry has proven itself to be one of the most crisis-proof consumer goods categories at a time of significant disruption. Even though consumers are very keen returning to the on-trade channels digital Commerce has emerged in strength. 



