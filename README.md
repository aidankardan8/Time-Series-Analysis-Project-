# Time-Series-Analysis-Project-

This is a repository for my Time Series Analysis Project in R. This project aims to forecast US CPI using data from FRED. The data in the csv file represents the “Consumer Price Index for All Urban Consumers: All Items in U.S.” from January 1947 to February 2024. This data will guide the models created for the forecasts.

The goal of this project is to use statistical concepts learned in a Time Series Analysis course and apply it to real-world data, with the objective of ultimately forecasting future data.

Initially, there was a need to clean the data and deal with formatting issues that sometimes arise when dealing with time series data. 

After creating the new dataframe, I conducted regression analysis techniques to get an idea of what kind of function could potentially fit the data well. 
Then I used prediction techniques to forecast future CPI using regression analysis. 

Next, I used classical decomposition techniques to get trend, seasonality, and noise graphs for the data to determine whether an additive or multiplicative model was best fit. 

To investigate the data further, I used detrending and differencing techniques. The result was the a polynomial of order 2-3 seemed to be the best fit for the trend. 

Taking a deeper dive into seasonality, I used seasonal lagged differencing for different time intervals to try and make a conclusion about whether or not CPI exhibits annual seasonality. 

In addition, I took a look at transforming the data, to further justify the choice of a multiplicative model as well, I used Box-Cox and Simple log transformations. After transforming the data into a simple log model, the underlying trend was almost flat/detrended, likely showing a exponentially proportional growth rate. 

This supported the conclusion presented by the decomposition, which is that the residual noise of the multiplicative model is more random and does not have increasing variance over time compared to the additive model.

Furthermore, I moved onto using Moving Average Methods, like the Spencer Filter, Exponential Smoothing, Holt’s Linear Trend Method, & Holt-Winters Method. Then, I forecasted CPI data using Holt-Winters and Exponential Smoothing. 

Finally, I conducted forecasting using Meta's Prophet forecasting system. 

**Conclusion**
Through regression analysis, decomposition of time series, differencing, detrending, and Box-Cox & Simple Log Transformations, it is clear that CPI data with respect to time resembles a non-linear relationship.
Based on the findings, there seems to be a exponential relationship, with a polynomial of order 2-3, describing the complex trend between CPI and time. Furthermore, it is clear that the model used for time series analysis of CPI data should be multiplicative as the residuals from the additive model are heteroskedastic, and the multiplicative model handles the noise better.
Through forecasting using regression techniques, moving average methods, and Meta’s Prophet forecasting system, valuable insights about CPI data can be made. Forecasting with regression techniques has advantages of simplicity, but it is a parametric method of estimation so there is a function that the CPI data needs to ultimately fit, which may not necessarily be the case with such a large economic indicator.
Forecasting with moving average methods smooths the data, and emphasizes the underlying trend, in addition, the Holt-Winters Method accounts for seasonality and trend, so these predictions are likely more justifiable than the regression predictions. Forecasting with Meta’s Prophet forecasting system also accounts for seasonality and trend, and therefore seem justifiable as well.
Thus, it is not unreasonable to consider Meta’s Prophet forecasting system and Holt-Winters method as valuable insights and information in efforts to predict future CPI, as their respective predictive powers seem justifiable.

Overall, because of the complexity of CPI as a economic indicator, there is a lot of uncertainty that can influence CPI data, so in reality the predictive power of these forecasts is likely not to be great, but they provide good insights into CPI data and how to further go about analyzing time series data.

Thank you for taking the time to look at my time series analysis project. Please feel free to reach out to me at a.a.ashrafi@wustl.edu with any questions or inquiries.







