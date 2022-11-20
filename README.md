# QRT-Stock-Return-Prediction

<b> finding_lagging_stocks.ipynb </b> Shows the dynamic time warping (DTW) between an individual stock, and the mean of all stocks in the same sector (on the same date). The idea is that individual stocks 'lag' behind the market. We had planned to identify how far certain stocks lag behind the market, and then use this as an additional feature for our model. Adapted from: https://tech.gorilla.co/how-can-we-quantify-similarity-between-time-series-ed1d0b633ca0

![similarity_between_time_series_ron](https://user-images.githubusercontent.com/63469131/202898250-c98d5834-9025-473c-ab49-35459aef2ea4.png)

<b> transformers.ipynb </b> Applies transformers, but couldn't finish running in time for the hackathon.

<b> knn.ipynb </b> Is more exploratory analysis. We used a latent factor model to learn the features of sectors in the dataset. So far, the accuracy is quite low.

<b> Reg ML Algo Testing.ipynb </b> Contains our code for creating the benchmark submission. 

Upon analysing relationships between any statistical correlation between these two features, we discovered there was some correlation with regards to the average volume to the average return within a particular sector/industry. There was laggy behaviour which implied that the volume traded was a good indicator with regards to which direction a stock would move and some link to how much it would move. However upon training, we discovered that the significance of these features was poor (even after feature engineering in multiple ways also attempting to offset the data in order i.e shift by 1 day). Therefore we decided to avoid using Volume to avoid any overfitting and improve generalisation on our validation sets
