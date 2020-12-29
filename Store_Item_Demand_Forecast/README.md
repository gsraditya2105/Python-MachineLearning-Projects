
## STORE ITEM DEMAND FORECASTING

![Wait Lets Understand](https://github.com/gsraditya2105/Python-MachineLearning-Projects/blob/main/Store_Item_Demand_Forecast/store.jpg?raw=true)

This project was created  to forecast the item sales from each store in the dataset
The data is resampled to monthly wise before processing 

![month_day_moreitemssold](https://github.com/gsraditya2105/Python-MachineLearning-Projects/blob/main/Store_Item_Demand_Forecast/Images/Picture1.png?raw=true)

![enter image description here](https://github.com/gsraditya2105/Python-MachineLearning-Projects/blob/main/Store_Item_Demand_Forecast/Images/Picture2.png?raw=true)

More Number of Item sales from each store are observed 
	 - In the month of July
	 - on Thursday

Item sales from store-1 plot for all the 50 items
![enter image description here](https://github.com/gsraditya2105/Python-MachineLearning-Projects/blob/main/Store_Item_Demand_Forecast/Images/Picture3.png?raw=true)

Analysis is performed on one of the item from a store and build models and choose the best 
The best model is applied to all the remaining items from all the stores

Store-1 Item-1 sales graph
![enter image description here](https://github.com/gsraditya2105/Python-MachineLearning-Projects/blob/main/Store_Item_Demand_Forecast/Images/Picture4.png?raw=true)

we see trend and seasonality exists in the data from visualization 

**Decomposition and Stationarity check:**
![enter image description here](https://github.com/gsraditya2105/Python-MachineLearning-Projects/blob/main/Store_Item_Demand_Forecast/Images/Picture5.JPG?raw=true)

when time series is decomposed we clearly see a trend and seasonality component 
1. constant Mean - No
2. constant Variance - Slightly Yes
3. Auto covariance is independent of time - *ADF Test* - True  *KPSS Test* - False

Trend and seasonality from the time series is removed using first differencing and seasonal differencing 
![enter image description here](https://github.com/gsraditya2105/Python-MachineLearning-Projects/blob/main/Store_Item_Demand_Forecast/Images/Picture6.JPG?raw=true)

 1. constant Mean - Slightly yes
 2. constant Variance - Yes
 3. Auto covariance is independent of time - *ADF Test* - True  *KPSS Test* - True

**Models:**

Using stationary time-series , tried to forecast using the models

 1. AR
 2. ARMA
 3. Holts -Winter Exponential Smoothing
 
 ![enter image description here](https://github.com/gsraditya2105/Python-MachineLearning-Projects/blob/main/Store_Item_Demand_Forecast/Images/Picture8.png?raw=true)
Holts-Winter model has the less RMSE compared to other models 

so using Holts -Winter model forecasted 1 year sales prediction for all the items in all the stores 

**Sample:**
![enter image description here](https://github.com/gsraditya2105/Python-MachineLearning-Projects/blob/main/Store_Item_Demand_Forecast/Images/Picture9.JPG?raw=true)

To checkout my notebook, please click [here](https://github.com/gsraditya2105/Python-MachineLearning-Projects/blob/main/Store_Item_Demand_Forecast/ML_2_Store_Data_Forecast.ipynb)


