# Time Series Forecasting

## Overview
   The purpose of this study is to forecast the Dec 2015 revenue for vendors 25 and 31. To forecast the revenue, the given dataset that contains 2 years historical data from 2013 – Oct 2015 was used. The time series model ARIMA (Autoregressive Integrated Moving Average) was used to forecast the December 2015 revenue.
### Data Analysis
- The revenue was calculated by multiplying the number of products sold by the price of the product. 
- The date in the dataset was converted to date format yyyy-mm-dd. 
- No null values were found in the dataset. 
- All product price were positive. 
- There were negative number of products sold. It was assumed that these were products that were returned. 
- The revenue data were aggregated by months. There were 12 observations per year. 
- The data is stationary after the stationarity test was done using statools adfuller.
- The data have a trend with peaks and valleys. It reaches its low points in July and accelerates rapidly up to the end of the year. 
- The revenue patterns repeat every year. 
- The 70:30 ratio was used to generate the training and test dataset.
- The parameter used for ARIMA p=1, d=0, q=1

### CHARTS
  - VENDOR 25
  
[Historical Revenue](https://github.com/fmgribbon/time_regression/blob/main/resources/Monthly_Revenue_25.PNG)

[ACF](https://github.com/fmgribbon/time_regression/blob/main/resources/ACF_vendor25.PNG)

[PACF](https://github.com/fmgribbon/time_regression/blob/main/resources/PACF_vendor25.PNG)



  - VENDOR 31
  
[Historical Revenue](https://github.com/fmgribbon/time_regression/blob/main/resources/Monthly_Revenue_31.PNG)  

[ACF](https://github.com/fmgribbon/time_regression/blob/main/resources/ACF_vendor31.PNG)

[PACF](https://github.com/fmgribbon/time_regression/blob/main/resources/PACF_vendor31.PNG)






## Results
 
  Based on the chart of the predicted and actual revenue of the test dataset. The model did not come close to the actual revenue. The model has to be improved and evaluated to increase its accuracy. The season peak in the historical data will have to be considered in improving the model. Another model within the ARIMA may be used to handle the seasonal peak in the data. 
  The ARIMA model has a lot of parameters that could be tweaked to improve the performance of the model. This analysis used the basic ARIMA model. It could be a starting point in the forecasting the revenue. The model may not be used to forecast revenue using other datasets.
 
   - VENDOR 25
   
[Predicted Revenue](https://github.com/fmgribbon/time_regression/blob/main/resources/predicted_vendor25.PNG)

[Forecasted December 2015 Revenue](https://github.com/fmgribbon/time_regression/blob/main/resources/Forecasted_vendor25.PNG)

[Mean Square Error](https://github.com/fmgribbon/time_series/blob/main/resources/mean_squared_error_vendor25.PNG)

[ARIMA Summary](https://github.com/fmgribbon/time_regression/blob/main/resources/Summary_vendor25.PNG)


 
   - VENDOR 31
   
[Predicted Revenue](https://github.com/fmgribbon/time_regression/blob/main/resources/predicted_vendor31.PNG)

[Forecasted December 2015 Revenue](https://github.com/fmgribbon/time_regression/blob/main/resources/Forecasted_vendor31.PNG)

[Mean Square Error](https://github.com/fmgribbon/time_series/blob/main/resources/mean_squared_error_vendor31.PNG)

[ARIMA Summary](https://github.com/fmgribbon/time_regression/blob/main/resources/Summary_vendor31.PNG)
