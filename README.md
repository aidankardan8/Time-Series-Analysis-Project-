# **Time Series Analysis Project: Forecasting US CPI**

### **Overview**
This repository contains my Time Series Analysis project, focusing on forecasting the **Consumer Price Index (CPI) for All Urban Consumers: All Items in U.S. (US CPI)**. The data, sourced from **FRED**, spans from **January 1947 to February 2024**. The goal of the project is to apply statistical and time series analysis techniques to this real-world economic data in order to build predictive models and gain insights into future CPI trends.

### **Project Objectives**
- **Data Cleaning & Preprocessing**: Address formatting issues and prepare the data for analysis, ensuring time series integrity.
- **Regression Analysis**: Explore potential functional forms that best describe the relationship between CPI and time.
- **Classical Decomposition**: Separate the CPI data into **trend**, **seasonality**, and **noise** components to determine the best-fit model—additive or multiplicative.
- **Time Series Techniques**: Apply detrending, differencing, and polynomial fitting to capture the underlying structure of the data.
- **Model Forecasting**: Use various statistical and machine learning models, including moving averages, exponential smoothing, Holt-Winters, and Meta’s Prophet forecasting system, to forecast future CPI.

### **Methodology**
1. **Data Cleaning & Preprocessing**:
   - Cleaned the time series data and addressed any formatting inconsistencies.
   - Created a new, structured dataframe for use in regression and forecasting models.

2. **Regression Analysis**:
   - Conducted exploratory regression analysis to identify potential functional forms, such as polynomial regressions of order 2-3, that best fit the CPI data over time.
   - Used **prediction techniques** to forecast future CPI values based on regression models.

3. **Classical Decomposition**:
   - Decomposed the time series data into **trend**, **seasonality**, and **noise** components using **additive** and **multiplicative** models.
   - Analyzed the results to determine the superiority of the **multiplicative model** due to its better handling of residual noise and heteroskedasticity.

4. **Detrending & Differencing**:
   - Applied **detrending** and **differencing** techniques to better understand the underlying data structure and detect any non-stationarity.
   - Found that a polynomial of order 2-3 was the best fit for capturing the trend in the CPI data.

5. **Transformations**:
   - Performed **Box-Cox** and **log transformations** to stabilize variance and justify the use of a multiplicative model.
   - Log transformation showed that the underlying trend is likely exponential, as the data became almost flat (detrended) after the transformation.

6. **Moving Average Methods**:
   - Used various **moving average techniques**, including the **Spencer Filter**, **Exponential Smoothing**, and **Holt-Winters Method**, to smooth the data and produce more robust forecasts.
   - Forecasted future CPI values using **Holt-Winters** and **Exponential Smoothing** methods.

7. **Advanced Forecasting**:
   - Implemented **Meta's Prophet forecasting system**, which accounts for both trend and seasonality, providing another layer of predictive analysis.

### **Key Findings**
- The data exhibits a **non-linear relationship** between CPI and time, with a **multiplicative model** being the best fit due to better handling of residual noise.
- Polynomial regression of **order 2-3** was effective in capturing the trend component.
- **Seasonality** was observed, and lagged differencing confirmed annual periodicity in CPI.
- Both **Meta’s Prophet** and **Holt-Winters** methods produced reliable forecasts, as they account for both seasonality and trend.

### **Conclusion**
This project highlights the complexity of CPI as an economic indicator. While the predictive models provide valuable insights into CPI data trends, the inherent uncertainty in economic forecasting means that these predictions should be used cautiously. The **multiplicative model**, along with **Holt-Winters** and **Meta’s Prophet** methods, proved to be strong approaches for understanding CPI trends and producing forecasts.

### **Future Work**
Future improvements to this project will involve:
- Exploring **ARIMA** and **GARCH** models for volatility and further refinement of trend forecasts.
- Implementing **ensemble methods** to combine multiple models for enhanced predictive accuracy.
- Applying **machine learning techniques** to explore non-linear relationships in the data.

### **Contact**
If you have any questions or would like to discuss this project further, feel free to reach out to me at [aidan.kardan@wustl.edu](mailto:aidan.kardan@wustl.edu).






