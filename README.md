## Stock-Predictor
stock predictor

```
curl \
--header "Content-Type: application/json" \
--request POST \
--data '{"ticker":"MSFT", "days":7}' \
http://35.93.74.139:8000/predict

```

## EC2 Stock Predictor
![Stock Predictor on EC2](https://drive.google.com/file/d/18h--rV0TeLofoSwbMVHZQgYhyxnY8w5a/view?usp=share_link)

## Algorithm Understanding

* How does the Prophet Algorithm differ from an LSTM?

The Prophet algorithm and LSTM (Long Short-Term Memory) are two different types of models used in time-series forecasting.

Prophet is a model developed by Facebook that uses a statistical approach called additive modeling to forecast time-series data. It decomposes the time-series into trend, seasonality, and other components using a generalized additive model (GAM), and then models each component separately. Prophet is designed to handle seasonality that changes over time, outliers, and missing data. It is a fast and easy-to-use model that can provide accurate forecasts for a wide range of time-series data.

LSTM, on the other hand, is a type of recurrent neural network (RNN) that is commonly used in deep learning for sequence modeling and time-series forecasting. LSTMs are designed to handle long-term dependencies in sequential data by using a memory cell and three gating mechanisms (input gate, forget gate, and output gate) that control the flow of information in the model. LSTMs can be trained to learn complex patterns in time-series data, including nonlinear relationships and temporal dependencies.

The main differences between Prophet and LSTM are:

Model Architecture: Prophet uses a statistical approach based on GAM, while LSTM uses a neural network architecture that involves recurrent layers.

Training: Prophet is a non-parametric model that can be trained quickly with default hyperparameters, while LSTM requires more time and effort to train with optimal hyperparameters.

Interpretability: Prophet provides transparent and interpretable results based on the additive model components, while LSTM can be less transparent and more difficult to interpret due to its complex architecture.

Use Cases: Prophet is well-suited for forecasting time-series data with seasonality, holidays, and trend changes, while LSTM can be used for a wide range of time-series forecasting tasks, including sequence prediction, anomaly detection, and natural language processing.

In summary, Prophet is a fast and easy-to-use statistical model that can provide accurate forecasts for time-series data with seasonality, while LSTM is a more powerful and flexible model that can learn complex patterns in time-series data but requires more computational resources and expertise to use effectively. The choice between these models depends on the specific needs of the forecasting task at hand.

* Why does an LSTM have poor performance against ARIMA and Profit for Time Series?

LSTM (Long Short-Term Memory) is a type of recurrent neural network (RNN) that is commonly used for time-series forecasting. While LSTM is a powerful model that can learn complex patterns in time-series data, it can sometimes have poorer performance compared to traditional time-series models such as ARIMA and Prophet.

Here are some reasons why LSTM may have poorer performance:

Training data: LSTM requires a large amount of training data to learn patterns in the time-series data. If the amount of available data is limited, LSTM may not be able to learn the underlying patterns effectively, leading to poorer performance compared to simpler models like ARIMA or Prophet.

Hyperparameter tuning: LSTM has many hyperparameters that need to be tuned to optimize its performance. If these hyperparameters are not tuned properly, the model may overfit or underfit the data, resulting in poorer performance.

Complex architecture: LSTM is a complex model with many parameters, making it prone to overfitting. In contrast, traditional time-series models like ARIMA and Prophet have simpler architectures that are less prone to overfitting.

Interpretability: LSTM is a black-box model that can be difficult to interpret. In contrast, traditional time-series models like ARIMA and Prophet provide transparent and interpretable results based on their model components.

Time-series characteristics: Finally, the performance of LSTM depends on the characteristics of the time-series data. If the data has strong seasonality or trend, traditional models like ARIMA or Prophet may perform better. LSTM is better suited for learning complex temporal dependencies in the data.

In summary, while LSTM is a powerful model that can learn complex patterns in time-series data, it may have poorer performance compared to traditional time-series models like ARIMA or Prophet in certain scenarios. It is important to consider the amount and quality of training data, hyperparameter tuning, model complexity, interpretability, and time-series characteristics when selecting a model for time-series forecasting.

## Interview Readiness
* What is exponential smoothing and why is it used in Time Series Forecasting?

Exponential smoothing is a time-series forecasting method that is used to produce a smoothed version of a time series by recursively applying a weighted average of past observations. It is called "exponential" smoothing because the weights assigned to past observations decay exponentially as the observations get older.

Exponential smoothing works by taking a weighted average of past observations, where the weights assigned to each observation decrease exponentially as we move further back in time. This means that recent observations are given more weight than older ones, reflecting the assumption that more recent data points are more relevant to predicting future values.

There are several variations of exponential smoothing, including simple exponential smoothing, Holt's linear exponential smoothing, and Holt-Winters' exponential smoothing. These variations differ in how they incorporate trend and seasonality into the smoothing process.

Exponential smoothing is widely used in time-series forecasting because it is a simple and flexible method that can be easily adapted to a wide range of time-series data. It is particularly useful for data that exhibit a high degree of randomness or short-term fluctuations, as it can smooth out these fluctuations and produce a more stable forecast.

Some advantages of exponential smoothing include:

It is easy to understand and implement, requiring only a few parameters to be specified.
It can handle time-series data with changing trends and seasonality.
It can produce forecasts quickly and efficiently, making it suitable for real-time applications.
It can be easily combined with other forecasting methods, such as ARIMA and Prophet, to improve forecast accuracy.
Overall, exponential smoothing is a powerful tool in the time-series forecasting toolkit, offering a simple yet effective way to produce accurate and reliable forecasts for a wide range of time-series data.

## Interview Readiness
* What is stationarity? What is seasonality? Why Is Stationarity Important in Time Series Forecasting?

Stationarity is a statistical property of time-series data where the statistical properties of the data do not change over time. Specifically, a time series is said to be stationary if its mean, variance, and autocovariance are constant over time. In other words, the data has a constant level, a constant variability, and no trends or seasonality.

Seasonality is a pattern that repeats itself over fixed intervals of time, such as daily, weekly, monthly, or yearly. For example, retail sales may have a seasonal pattern that peaks during the holiday season or a flu outbreak may have a seasonal pattern that peaks during the winter months.

In time-series forecasting, stationarity is important because it is a key assumption of many statistical models used for forecasting, such as ARIMA and SARIMA models. These models assume that the statistical properties of the time series are constant over time, and they use this assumption to make predictions about future values.

When a time series is not stationary, it can be difficult to make accurate predictions using these models. For example, if a time series has a trend or seasonality, the model may mistakenly interpret this as a pattern in the data that needs to be accounted for in the forecast, leading to inaccurate predictions.

To make a time series stationary, we can use techniques like differencing, logarithmic transformation, and detrending to remove trends and seasonal patterns from the data. Once a time series has been made stationary, it can be more accurately modeled using statistical techniques that assume stationarity.

In summary, stationarity is an important property of time-series data for forecasting because it allows us to use statistical models that assume constant statistical properties over time. Seasonality is a common pattern in time-series data that can make a time series non-stationary, but can be removed using techniques like differencing and detrending. By making a time series stationary, we can improve the accuracy of our forecasts and make more informed decisions based on the predictions

## Interview Readiness

* How is seasonality different from cyclicality? Fill in the blanks:
Seasonality and cyclicality are both patterns that can be observed in time-series data, but they differ in their frequency and duration.

Seasonality is a pattern that repeats itself over fixed intervals of time, such as daily, weekly, monthly, or yearly. For example, retail sales may have a seasonal pattern that peaks during the holiday season, or a flu outbreak may have a seasonal pattern that peaks during the winter months. Seasonality is typically caused by external factors like weather, holidays, or cultural events, and is often predictable and regular.

Cyclicality, on the other hand, is a pattern that repeats itself over irregular intervals of time, without any fixed pattern. Cyclicality is often caused by internal factors like business cycles, economic cycles, or political cycles, and is often unpredictable and irregular in duration and amplitude.

While seasonality is typically removed from time-series data before modeling, cyclicality is often incorporated into models to help capture the underlying patterns in the data. For example, some time-series models, such as the autoregressive integrated moving average (ARIMA) model, include a cyclic component to capture the cyclical patterns in the data.

In summary, seasonality and cyclicality are both patterns that can be observed in time-series data, but they differ in their frequency, predictability, and duration. Seasonality is a pattern that repeats itself over fixed intervals of time and is often predictable, while cyclicality is a pattern that repeats itself over irregular intervals of time and is often unpredictable.


* Seasonality___ is predictable, whereas cyclicality___ is not.



