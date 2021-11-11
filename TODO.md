# TODO for Transformer Modeling

## Existing Model Check

Check Existing Model using Time Series Data (Transformer Majority)

1. [transformer-time-series-prediction](https://github.com/oliverguhr/transformer-time-series-prediction)

   - Based on univariable data (Date & Temperature)

2. [pytorch-forecasting](https://github.com/jdb78/pytorch-forecasting)

3. [TPA-LSTM](https://github.com/shunyaoshih/TPA-LSTM)
4. [Pytorch-Transformer](https://github.com/LiamMaclean216/Pytorch-Transfomer/tree/70f170adc6f3f611fef5282523e886ae45e1e2b6)
   - [pytorch-transformer Introduction Page](https://ichi.pro/ko/pytorch-yecheug-sogae-110907224616774)
5. [flow-forecast](https://github.com/AIStream-Peelout/flow-forecast/tree/master/flood_forecast)

> **TODO: Do Test Above List**

## Reference Page

- [Using transformer on timeseries](https://discuss.pytorch.org/t/using-transformer-on-timeseries/104759)
- [Transformers for time series data](https://www.reddit.com/r/MachineLearning/comments/ckaji4/d_transformers_for_time_series_data/)
- [Attention for time series forecasting and classification](https://towardsdatascience.com/attention-for-time-series-classification-and-forecasting-261723e0006d)

## Mainly Use

1. [flow-forecast](https://github.com/AIStream-Peelout/flow-forecast/tree/master/flood_forecast)
2. Cyclical Encoding

   - A key concern when dealing with cyclical features is how we can encode the values such that it is clear to the deep learning algorithm that the features occur in cycles : significant effect on the convergence rate of the algorithm
   - the absolute difference between 22 and 23 is 1. However, when considering 23:00 and 00:00, the jump discontinuity occurs, and even though the difference is one hour, with the unencoded feature, the absolute difference in the feature is of course 23
   - [Encoding Cyclical Features for Deep Learning](https://www.avanwyk.com/encoding-cyclical-features-for-deep-learning/)
   - [Encoding Cyclical Features for Deep Learning_kaggle](https://www.kaggle.com/avanwyk/encoding-cyclical-features-for-deep-learning)

     > [J_Mention] Because of Cyclical Encoding, not making timeslot can make sense. Try Using Raw Data. But there is possibility this thoughts are wrong, based on used data in above website are hour attribute of datetime feature.

     > **[J_Conc]** 1. Try Raw data & Timeslot data after modify(Decide fill nan row or not) 2. sin & cos : year, month, day, hour, min (total 10)s
