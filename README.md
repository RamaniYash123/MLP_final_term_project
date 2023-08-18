This repository contains the implementations related to the experiments of a set of publicly available datasets that are used in the time series forecasting research space.
We copy the original repo from a public repository owned by rakshitha123 we are here to provide you a link for that repository:https://github.com/rakshitha123/TSForecasting/tree/master This repo also provides a link from where you can find a database to use https://zenodo.org/communities/forecasting.  
To introduce a new dataset to a model, you need to put it in the tsf__data folder and a file must have a .tsf extension. To better understand we use a notebook provided by the parent repository and do some modifications. By following the example in utils/data_loader.R, the data in tsibble format [1] can be loaded into the R environment. It takes a similar tack to the R foreign package's arff file loading mechanism [2]. The sample in utils/data_loader.py can be used to load the data into the Python environment as a Pandas data frame.
ETS, ARIMA, Theta, TBATS, SES, and DHR-ARIMA are six local univariate forecasting models that have been developed: models/local_univariate_models.R. Apart from this we also develop one additional model of our own which is STL.
Seasonal Decomposition of Time Series (STL): By separating time series data into components like seasonality, trend, and residuals, STL allows more accurate modeling of the different components.
models/global_models.R is a global pooled regression model.
models/global_models.R is a global CatBoost model.
A feed-forward neural network and the DeepAR, N-BEATS, WaveNet, and Transformer deep learning models may be found in experiments/deep_learning_experiments.py
experiments/feature_functions.R and experiments/feature_experiments.R are programs that do feature computations for all series.
utils/error_calculator.R calculates 5 error metrics to assess projections.
In addition to the dataset used in the original repository, we introduce a new data set of vehicle trips downloaded from https://zenodo.org/communities/forecasting?page=1&size=20.This set of for-hire vehicle (FHV) firms' journeys and vehicle numbers are captured by 329 daily time series in this dataset. The first source of the dataset was fivethirtyeight.com/github/uber-tlc-foil-response. 

