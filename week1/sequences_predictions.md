## Common patterns in time series

Trend + Seasonality + Autocorrelation + Noise

## Train validation and test sets
- fixed partitioning(train+validation, test) 
- roll forward partitioning([start with short training period and gradually increase it](https://towardsdatascience.com/time-series-nested-cross-validation-76adba623eb9))

## Time series simulation
https://github.com/https-deeplearning-ai/tensorflow-1-public/blob/main/C4/W1/ungraded_labs/C4_W1_Lab_1_time_series.ipynb

## Metrics for evaluating performance
- error = pred - actual
- mse = np.square(errors)
- rmse = np.sqrt(mse)
- mae = np.abs(errors).mean()
- mape = np.abs(errors/x_valid).mean(): this is the mean ratio between the absolute error and the absolute value, this gives an idea of the size of the errors compared to the values.

Depending on your task, you may prefer the mae or the mse. For example, if large errors are potentially dangerous and they cost you much more than smaller errors, then you may prefer the mse. But if your gain or your loss is just proportional to the size of the error, then the mae may be better.

## Moving average and differencing

## Trailing vs centered windows
Then moving averages using centered windows can be more accurate than using trailing windows. But we can't use centered windows to smooth present values since we don't know future values. However, to smooth past values we can afford to use centered windows. Okay, so now we've looked at a few statistical methods for predicting the next values in a time series.

## Simulation prediction
https://github.com/https-deeplearning-ai/tensorflow-1-public/blob/main/C4/W1/ungraded_labs/C4_W1_Lab_2_forecasting.ipynb
