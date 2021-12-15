# Flight-fare-prediction


<img width="800" alt="Screen Shot 2021-12-13 at 11 08 16 AM" src="https://user-images.githubusercontent.com/80868520/145847989-2c26a878-6afa-4839-8942-3adcdc15c46f.png">

## Introduction:

The number of people who travel by plane has risen dramatically in recent years. 
Prices change constantly owing to various situations, making it difficult for airlines to maintain pricing. 
As a result, we'll attempt to fix the problem via machine learning. This can assist airlines in determining what costs they can sustain. 
It can also assist clients to predict flight fares and making travel plans appropriately.

## Dataset:

Kaggle was used to obtain the dataset.There are 10683 records in total, with 11 different attributes such as source, destination, airline, total stops, and duration. The fare was predicted using machine learning regression techniques.

## Exploratory Data Analysis:

In this [notebook]( https://github.com/Sujitha-Sunkara/Flight-fare-prediction/blob/main/Fare%20prediction-%20EDA.ipynb),I perform basic exploratory data analysis on the dataset in order to gain a better knowledge of it. Matplotlib and seaborn are two Python packages that are used. I talked about the following topics:
- Understanding the facts as a whole
- Visualizing the trends to analyze each of the factors and their interactions.
- With the help of existing features, I created a few new features and visualized them.

## Data Analysis:
### Univariate Analysis:
<img width="500" alt="Screen Shot 2021-12-13 at 2 20 11 PM" src="https://user-images.githubusercontent.com/80868520/145874872-e0a3cd70-5c31-4689-ac88-d869b7784572.png"><img width="500" alt="Screen Shot 2021-12-13 at 2 20 27 PM" src="https://user-images.githubusercontent.com/80868520/145874905-31599364-4dc5-4407-aa7f-a432fea194b4.png">

From different Univariate analysis, it been observed that 
- Jet Airways has the highest number of flights
- More flights originate from Delhi, which is followed by Kolkata and least in chennai
- The bulk of flights arrive in Cochin as their final destination.
- Most of the flights has one stop.
- more passengers travelled in the month of may followed by june. This is due to that mostly many people planned their vacations in summer.

<img width="500" alt="Screen Shot 2021-12-13 at 2 20 55 PM" src="https://user-images.githubusercontent.com/80868520/145874940-772ae0d5-ff1c-437c-a1fd-6914f58ecd18.png">
Majority if the flighhts fare lie in range of 3000 to 18000
### Bivariate Analysis :
<img width="500" alt="Screen Shot 2021-12-13 at 2 21 24 PM" src="https://user-images.githubusercontent.com/80868520/145874974-260f3459-7d45-4d1b-b2cf-5866ebb07940.png"><img width="500" alt="Screen Shot 2021-12-13 at 2 21 43 PM" src="https://user-images.githubusercontent.com/80868520/145875011-fb42d2d4-c19f-4a38-a201-dbb1d6f3cdc9.png"><img width="500" alt="Screen Shot 2021-12-13 at 2 21 53 PM" src="https://user-images.githubusercontent.com/80868520/145875054-c0f0f2d2-2b86-4df4-b419-1b6c1786aa86.png">
- The price of JetAirway Bussiness is high compared to other airlines.
- The mean price for a flight is greatest in the Delhi source, but there are several outliers in the Bangalore source where the price is larger than 60000.
- There is a positive correlation between the number of stops and price , Price go high when the total stops increases.
<img width="791" alt="Screen Shot 2021-12-13 at 2 58 19 PM" src="https://user-images.githubusercontent.com/80868520/145879794-dbd318cb-7b74-4e57-ab8d-de2de957296a.png">
The flights in the early morning time has highest price

### Flights count from source to destination:
<img width="834" alt="Screen Shot 2021-12-13 at 2 59 01 PM" src="https://user-images.githubusercontent.com/80868520/145879889-cbe044e6-4d04-442b-8ec6-7156d1880707.png">
### Top 10 Costliest routes

Route	Price
44	BOM → DED → DEL → HYD	24115.000000
51	BOM → JDH → DEL → HYD	23867.000000
58	BOM → VNS → DEL → HYD	23528.000000
57	BOM → UDR → DEL → HYD	22950.000000
38	BOM → BDQ → DEL → HYD	22792.500000
107	DEL → DED → BOM → COK	19539.500000
115	DEL → IXU → BOM → COK	19381.333333
52	BOM → JDH → JAI → DEL → HYD	18293.000000
50	BOM → JAI → DEL → HYD	17926.000000
14	BLR → CCU → BBI → HYD → VGA → DEL	17686.000000
### source and destination that takes the longest?
<img width="286" alt="Screen Shot 2021-12-13 at 2 58 08 PM" src="https://user-images.githubusercontent.com/80868520/145879867-abea575a-8e7a-4d54-b64c-1cd696aa34c6.png">

## Feature Engineering and Preprocessing :
In this [notebook](https://github.com/Sujitha-Sunkara/Flight-fare-prediction/blob/main/Fare%20prediction%20-%20Feature%20Engineering.ipynb) , 
- For the categorical features, created dummy variables.
- Removed Outliers in target variable and performed Boxcox transformation for price variable.
<img width="1068" alt="Screen Shot 2021-12-13 at 4 18 06 PM" src="https://user-images.githubusercontent.com/80868520/145890372-d8513547-26ff-4ec1-8d59-3e9b2a345acc.png">
## Regression Models :
Created models, which were then evaluated in this [notebook]( https://github.com/Sujitha-Sunkara/Flight-fare-prediction/blob/main/Flight%20prediction%20model.ipynb) ,
- The data is split into two sections: training and validation. I use the training set to find the model and then the validation set to test it on unknown data.
- Regression Machine learning models were used and seected best model which have lowest MAE , MSE, RMSE and high R2 score . Dcision Tree model were performd good in training and not in validation , where Random forest model performed best in both training and validation data . 
- Hyperparameter tuning were performed on the Random Forest model and test it on unknown data.
## Model Findings :
Regression models performance 
------Performance of Training data--------
<img width="788" alt="Screen Shot 2021-12-13 at 4 29 04 PM" src="https://user-images.githubusercontent.com/80868520/145891755-c8951f27-0db8-44fb-aa1a-accd19c9de09.png">
------Performance of validation data--------
<img width="715" alt="Screen Shot 2021-12-13 at 4 29 59 PM" src="https://user-images.githubusercontent.com/80868520/145891906-3f9af37d-227b-4510-9502-0e9682224810.png">

After hyperparametertyuning the Random forest regression and fitting with best params , the results are:
MAE: 734.6088


MSE: 2132548.6219


RMSE: 1460.3248


R2 score: 0.88


Which explains 88% of the data fits the model.



