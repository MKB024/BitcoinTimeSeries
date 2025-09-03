# BitcoinTimeSeries

# Executive Summary

Bitcoin is a leading digital asset within the global markets. Due to its volatility and risk, investors are not confident to purchase due to the current value – there is unpredictability if the value could spike or dip at any time. Would a time series forecast model support investors making informed decisions?
Public data obtained from Kaggle was used to explore and build an ARIMA prediction model to support investors by predicting future Bitcoin closing values. Python was used to conduct data load and clean-up, Exploratory Data Analysis, model preparation and execution. This was conducted in Google Colab notebook and uploaded into Github. In conclusion, the model was not successful and requires further work to be conducted to produce better predictions for Bitcoin closing amounts. Due to the lack of confidence in the model the project has not helped resolve this problem in the final stage of the analysis. More work is required for model forecasting. 



# Introduction

Cryptocurrencies, particularly Bitcoin, have become a significant asset within the global markets. Accurate predictions of Bitcoin prices have attracted interest from investors, however there are still unpredictable and non-linear behaviours, which create uncertainty. 
The project explores the power of machine learning predictions for Bitcoin data, specifically closing amounts. Predictions are very important in the investment market, therefore conducting analysis using historical data and to confirm patterns, trends and seasonality, will support investors in their decision-making. Huang, et al (2022) conducted a time series analysis on Bitcoin data ranging from 2013 – 2022 and concluded that there was an upwards trend, however high volatility and influence of human behaviours need to be considered. 
Due to advancements in technology, the data scientist aimed to develop a model that can provide smarter, informed decisions of future Bitcoin closing amounts. 


# Data

The Bitcoin dataset was obtained from Kaggle.com in a CSV file, consisting of 8 attributes. The dataset contained Bitcoin data from 2014 to 2025. Large volume of data will support better predictions for the time series model. As the dataset was publically available, there was no personal or sensitive data to consider during the project. 
The data processing started within Excel, by removing irrelevant attributes, checking for missing data and duplication. The transformations and preparations were conducted in Excel as they were simple, as was the dataset. Key principles from the Government Data Quality Framework (2020) to ensure data is clean and ready for analysis.


Google Colab is a cloud-based product with an easy-to-use interface, to write and executive Python. Python was used to conduct data load and clean-up, Exploratory Data Analysis, model preparation and execution. 
Although data preparation was completed before the data was imported into Google Colab, data preparation and processing checks were conducted again. And finally, the notebook was uploaded to GitHub to showcase the data science project. 


# Results & Analysis

Missing Data
Missing data check was conducted as a precaution – as expected there were no missing values within the attributes (Appendix 1). 

Descriptive Statistics
Descriptive statistics check was conducted to measure central tendency and variability (Appendix 2). The view gives a quick indication of the average value in the data for each attribute, as well as the minimum and maximum.

Exploratory Data Analysis
The data scientist determined Bitcoin ‘Close’ value as the leading metric for the project. The value was plotted on a line graph to visualise trends, seasonality and anomalies.  

Figure 3 shows an upward trend over time, with many inconsistent spikes and dips. Seasonality is not present in this data, as there are no consistent patterns each year. A decomposition plot was conducted, this technique isolates the trend, seasonality and irregularities to further analyse the data (Appendix 3). As expected, there is a clear indication of an upward rise in Bitcoin close values. No seasonality was present for this data; this was supported by a Box-plot method shown in Figure 4.

 

Figure 4. Box-plot method to identify trend and seasonality. 
 
Although there is an upward trend, there was a significant drop in value between 2022 to 2024 – this could be a result of the impact after COVID-19. Big world events could impact the value of Bitcoin, such as Stock Market crashes, Politics, etc. However, social media has become a leading influence on Bitcoin and could steer the direction of the value. Over the years social media presence has popularised Cryptocurrency and has led to its success. But most importantly, the supply and demand of Bitcoin is a leading influence of the value of Bitcoin and the spikes and dips presented in Figure 3. This was supported by Jin, Liu & Zhang (2022) who conducted analysis of factors impacting Bitcoin price.  


Stationary Test
Augmented Dickey-Fuller (ADF) test was conducted as a pre-model assessment, to assess if the time series was stationary or non-stationary (Appendix 4). The p value was 0.98, therefore rejecting the null hypothesis (0.05 significance level), which suggests the time series is non-stationary. 

Lag Analysis
Autocorrelation will show the strength of a relationship between two variables, with lags. The Autocorrelation Function test (ACF) (Figure 5) shows 20 lags performed to see if there are positive or negative correlation when compared to different data points – there are strong positive autocorrelations, which indicate the values correlate with values at a subsequent time point.
Partial Autocorrelation Function test (PACF) was performed, as shown in figure 6, and found small positive and negative correlations throughout the lags – confirming trends and seasonality, and non-stationary data. 

ARIMA Model
ARIMA Model was used to forecast the potential Bitcoin value. The data was split to 80:20 for training and testing. 80% of the data was used to train the model to shape the forecasted value of Bitcoin closing amounts.  

The forecasted values have shown a significant drop in value and flat-line trend. This outcome does not provide insight information to help investors make informed decisions for Bitcoin values over time. The RSME value is high and confirms the model needs more work and decreases the reliability in the prediction (Appendix 5). 



# Recommendations

The model needs to be reassessed as the prediction does not look correct. Perhaps a SARIMA model needs to be used for this exercise as it considers seasonality. Further investigation is required. 
Once the model is refined and producing better predicted outputs, this information could be imported into Power BI to visualise and to communicate the data insights effectively. This would be an automated process and would not require further work on the model itself. This would be an effective tool to showcase the model predictions to end-users. 
The project could be advanced by including Google trend data, for instance, if there are large volume of Bitcoin searches, this means Bitcoin is in a high volatility state.


# Conclusion

In conclusion, the model was not successful and requires further work to be conducted to produce better predictions for Bitcoin closing amounts. Due to the lack of confidence in the model the project has not helped resolve this problem in the final stage of the analysis. More work is required for model forecasting. 


# References

GOV.UK. (n.d.). The Government Data Quality Framework. [online] Available at: https://www.gov.uk/government/publications/the-government-data-quality-framework. 

Huang, W., Li, Y., Zhao, Y. and Zheng, L. (2022). Time Series Analysis and Prediction on Bitcoin. 34, pp.1223–1234. doi: https://doi.org/10.54691/bcpbm.v34i.3163.  

Jin, K., Liu, X. and Zhang, W. (2022). The Analysis of Factors Affecting Bitcoin Price. BCP Business & Management, 24, pp.23–33. doi: https://doi.org/10.54691/bcpbm.v24i.1423. 



# Appendices

Appendix 1 – Missing Data Checks in Google Colab

 



Appendix 2 – Descriptive Statistics Checks in Google Colab

 



Appendix 3 – Decomposition in Google Colab

 



Appendix 4 – ADF Test in Google Colab

 



Appendix 5 – RSME Value in Google Colab

 

