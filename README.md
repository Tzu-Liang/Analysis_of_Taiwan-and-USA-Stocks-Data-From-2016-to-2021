# Analysis of Taiwan and USA Stocks Data From 2016 to 2021
- Remember to change the theme to default light
- This project is under [Tzu-Liang Hsu](https://github.com/Tzu-Liang) and [Pin-Teng Lin](https://github.com/Pentiumlin)
## Introduction

### Raw Dataset
The data we collected in this article is from [Yahoo Finance](https://finance.yahoo.com/) and also was uploaded to [Kaggle community (Taiwan and USA Stocks Data From 2016 to 2021)](https://www.kaggle.com/pentiumlin/taiwan-and-usa-stocks-data). In addition, we took two types of incorporations both in Taiwan and the US for examples (exchange-traded fund (ETF) and technology stocks ). For the sake of precise predictions, we proposed here two schemes for analyzing stock price by two types of data pre-processing: the first type is using close price to predict close price; the other one is using stock market indices to predict close price. Finally, we split the raw data into training, validation, and testing datasets in proportion to 7 : 2 : 1.

### Normalization
- In the first type, we used [MinMaxScaler](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MinMaxScaler.html) functions shown below to compute the minimum and maximum in the trainning set used for later scaling because we only know the informaion in the tranning set. After obtainning the minimum and maximum, we can transform the training, validation, and testing datasets depending on the scaler from the training set. 
<div align=center>
<img src="https://latex.codecogs.com/svg.image?x_{scaled}&space;=&space;\frac{x-x_{min}}{x_{max}-x_{min}}" title="x_{scaled} = \frac{x-x_{min}}{x_{max}-x_{min}}" />
<div align=left>

- In the second type,

## Results
### Machine Learning Workflow
<div align=center>
<img src="https://github.com/Tzu-Liang/Analysis_of_Taiwan-and-USA-Stocks-Data-From-2016-to-2021/blob/main/workflow.jpg" alt="Workflow" width="500" height="600">
<div align=left>

### Models
- LSTM (Long Short-Term Memory) is good at dealing with the stock price data since it is in the form of time series and sequential form. Hence, we took its advatanges to build a regressor whose structure and results of are shown below. The root mean errors of the testing data from all of the incorporations are up to scratch. Also, the code of this regressor is available [here](https://github.com/Tzu-Liang/Analysis_of_Taiwan-and-USA-Stocks-Data-From-2016-to-2021/blob/main/lstm-stocks-prediction.ipynb).
<div align=center>
<img src="https://github.com/Tzu-Liang/Analysis_of_Taiwan-and-USA-Stocks-Data-From-2016-to-2021/blob/main/0050.png" alt="Workflow" width="600" height="350">
  
<img src="https://github.com/Tzu-Liang/Analysis_of_Taiwan-and-USA-Stocks-Data-From-2016-to-2021/blob/main/SPY.png" alt="Workflow" width="600" height="350">
  
<img src="https://github.com/Tzu-Liang/Analysis_of_Taiwan-and-USA-Stocks-Data-From-2016-to-2021/blob/main/TSMC.png" alt="Workflow" width="600" height="350">
  
<img src="https://github.com/Tzu-Liang/Analysis_of_Taiwan-and-USA-Stocks-Data-From-2016-to-2021/blob/main/INTC.png" alt="Workflow" width="600" height="350">
<div align=left> 
  

- XGBoost for Regression is an efficient implementation of gradient boosting, and also can be used for time series forecasting as long as time series datasets are transformed into supervised learning problem.

## Reference
[1] [Ghosh, P., Neufeld, A., & Sahoo, J.K. (2020). Forecasting directional movements of stock prices for intraday trading using LSTM and random forests. ArXiv, abs/2004.10178.](https://arxiv.org/abs/2004.10178)  


## Related Websites
[1] [How to Use XGBoost for Time Series Forecasting](https://machinelearningmastery.com/xgboost-for-time-series-forecasting/)  
[2] [XGBoost for stock trend & prices prediction](https://www.kaggle.com/mtszkw/xgboost-for-stock-trend-prices-prediction)

