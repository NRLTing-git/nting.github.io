---
layout: single
date: 2024-05-08
title: ARIMA vs LSTM vs GRU
tags: "Time Series Forecasting Nerual Network  ARIMA Prediction"
header:
    overlay_image: "assets/image/ts_bg.jpg"
---
Time Series Forecasting \| Nerual Network \|  ARIMA \| Prediction 

In this mini-project we forecast the daily consumption one month in advance of the PJM West Region: 2001-2018 (PJMW) estimated hourly energy consumption data from PJM in Megawatts
dataset which can be found [here](https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption/data)

Visualization of the data
<img src="{{ site.baseurl }}/assets/image/ts_data.jpg" alt="data">

**Results**


**ARIMA** 
<img src="{{ site.baseurl }}/assets/image/ts_ariima.jpg" alt="arima">

**LSTM** 
<img src="{{ site.baseurl }}/assets/image/ts_lstm.jpg" alt="lstm">

**GRU** 
<img src="{{ site.baseurl }}/assets/image/ts_gru.jpg" alt="gru">

Baseline 
<img src="{{ site.baseurl }}/assets/image/ts_base.jpg" alt="base">

Model Performance
<img src="{{ site.baseurl }}/assets/image/ts_mp.jpg" alt="mp">

Based on the dataframe above all validation and testing of the model were able to beat the baseline, however there are some difference on the models themselves. On validation, a hypertuned LSTM had the best validation MAE, followed by GRU then ARIMA. But in terms of the real performance which is the testing ARIMA had the lowest MAE and MAPE and it was way better compared to the hypertuned LSTM and GRU. Note that, although ARIMA were able to beat both model, it has the highest run time as well, it was 5 times slower compared to the NNs, moreover the dataset was aggregated daily, so imagine if the dataset follows its orignal format which is by hourly. Because of that, although the ARIMA performed the best and our dataset is getting larger and larger, then it would be best to choose the second choice, which has a way faster runtime, yet performing more than the baseline. In addition the performance of GRU had barely beaten the baselines that we had set up.

The hypertuning of the NNs was followed by trial and error and as well as logical guess, the choice of activation function sigmoid, was due to the fact that the data was normalized from 0 to 1 hence we want to reflect that with sigmoid, regarding swish, it is said that handle complex patterns and deep networks more effectively, since we've been eyeballing the visualization we are seeing a weak pattern, hence the choice of swish.

for the choice of 2 hidden layers, our group decided to create only up to hidden layers as not to overcomplicate, it. What we meant by overcomplicating it, is by beating the baseline with comlpex architecture where in fact, sa simple 2 layers could give us a favorable results already.

Note:
We have tried using the hourly basis dataset on the NNs and what we got was almost the same MAE and MAPE.


