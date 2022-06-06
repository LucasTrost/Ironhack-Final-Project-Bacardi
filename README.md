# Ironhack Final-Bootcamp Project | Bacardi #

by Lucas Trost and Miguel Ángel Villoslada, June 2022

### Forecasting Sales Based on the Digital Commerce Channel ###
![Bacardi_brands_logo](https://user-images.githubusercontent.com/103429801/172137582-400a5c1e-e295-465b-8fe8-f9429792afdd.jpeg)

**Table of content**

  - Project Brief

  - Exploratory Data Analysis

  - Machine Learning Process

  - Key Take Aways



Project Brief

Scenario: We are working as data analysts for one of the largest privately held, family-owned spirits companies in the world, Bacardi. The scope of the project involves building a soundable model to predict sales based on volume. Through this work we also aim to identify trends within different countries among the most representative brands the company is producing. 


Challenge: Given the depth of the dataset, we harnessed data from external sources to ease decision taking. Temperature, Consumer Confidence, seasonality data and movement data were considered to build a model that could predict the sales for the Digital Commerce Channel and for the most populated countries in the EU. 

Further project details such as deliverables can be found here

Exploratory Data Analysis (EDA)

Tableau:
To explore the data we used, Tableau, a visualization software that allowed us understand and gain insights about the company's products, markets and other relevant information.

Feel free to explore the Tableau and/or the presentation slides

Excel:
We worked intensively in excel adding data to the initial file, Digital Commerce Pure Playeres US EUBig5. Being the EU an already relevant market we dropped from our analysis the US market. But before that  




Importing the data to SQL was no smooth sailing. Apparently the csv. file from the study was corrupted. In order to circumvent said problem, I exported the excel version of the data into Python, where I turned it into a DataFrame, and downloaded as a csv.

This seemed to work, and I was able to get started on querying. Overall I was already pretty happy with my understanding of the data, which is why I kept querying to a minimal.

For Excel query file see here

Machine Learning Process
Pre-Modeling
Besides EDA there were a few necessary steps to take, in order to ensure valid results end results The most notable steps here were:

Dropping columns
One obvious column to drop straight away, was the Unknown :1 column, which was some form of indexing included in the data. Next I decided to drop the columns: id, date, lat, long as all of these would lead to heavy overfitting.

I had no trouble dropping lat and long, as the combination of the two is very unique. Date was the only column I had some trouble with. In the end I decided that the data wasn't dense enough to justify keeping the column. In other words, date was quite unique, hence the benefit of keeping it did not outweigh the aspect of overfitting.

Dropping outliers
Through extensive work in Tableau I was quite confident with outliers. The only notable one, which seemed like bad data was the property worth ca. 500k, that had a number of 33 bedrooms. Price outliers or anything similar were kept.

Scaling
As our DataFrame had vastly differentiating number ranges, and consisted of only numerical columns, I decided it would be best to apply a MinMaxScaler() to the entire DataFrame.

Model for estimating price
Linear Regression Model
I first started with a base line Linear Regressions model. After drafting two more Candidates where I played with choosing between the highly correlating columns around the size of the property (sqft_living,sqft_living15,sqft_above, etc.) and getting no real improvement in accuracy I decided to move on to the next model.

K-Nearest-Neighbours Regression Model
The base model alone showed more promising results than the previous candidates, with an increase in accuracy and a decrease in Root Mean Squared Error (RMSE).

I noticed that yr_renovated may lead to some inaccuracies, with the model disproportionally rewarding said feature. Houses that had no renevation date received a '0' as entry in the feature.

This led to two strong opposing groups: houses with, and houses without a renovation date. A grouping beforehand (assigning a value of either 2 = freshly renovated, 1 = recently renovated, 0 = not renovated/ renovated long time ago) would fix that problem.

I still believed I was on to something with the correlation concept in the linear regressions model. Thus I experimented a bit, and dropping sqft_basement and sqft_above (which = sqft_living), the model improved yet again.

Decision Tree Regression Model
Already being fairly content with my KNN model, I only planned to briefly dip into decision trees. With the base model returning an accuracy of 64%, 8% worse than the KNN, I was more than happy to move on.

Model to determine importance of features
As already mentioned we, TheAgency, are quite the luxurious real-estate-agency. Thus we were especially interested in houses with a value equal to and greater than $650k. Here a simple pandas query did the trick.

Random Forest Regression Model
To determine feature importance one could've based their answer on a correlation matrix. We as a agency, however, have to keep our standards high, which is why I opted for a ensemble method of the Random Forest Regressor. I then ran the model through a inspection method, which gave me my final results. Screenshot 2022-05-12 at 17 47 27

take a look at my python notebook and further anotations here

Key Take Aways
Model for estimating price:
With an accuracy of 72.25% and a RSME of $195k the model is fairly accurate, but no where close for us, TheAgency, to solemnly rely on it for price determination.

Model to determine importance of features
Here the results seem alot more promising, as wee gained a clear guideline as to which features determine high prices.

Overall conclusion
I believe the two models to be of good aid for our new office in Seattle, especially the ladder. I can see us scanning the real estate market for the determined features, and calculating a rough price range, before sending out one of our agents. Because in the end, little beats the judgement and expertise of a TheAgency's agent.
