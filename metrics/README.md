<h3 align="center">
  Evaluation of Model Performance
</h3>

---

####  🔍 More About Algorithms & Machine Learning Models
- Rolling Forcast ARIMA

  *A rolling forecast is required given the dependence on observations in prior time steps for differencing and the AR model. A crude way to perform this rolling forecast is to re-create the ARIMA model after each new observation is received. We manually keep track of all observations in a list called history that is seeded with the training data and to which new observations are appended each iteration.*

- XGBRegressor

  *Extreme Gradient Boosting (XGBoost) can also be used for time series forecasting, although it requires that the time series dataset be transformed into a supervised learning problem first. It also requires the use of a specialized technique for evaluating the model called walk-forward validation, as evaluating the model using k-fold cross validation would result in optimistically biased results.*

- LSTM

  *Long Short-Term Memory (LSTM) models are a type of recurrent neural network capable of learning sequences of observations. This makes them a deep learning network well suited for time series forecasting.*

  > [Univariate (uniLSTM)](../2_UnivariateForecast.ipynb)<br/>
    *Comprises a single series of observations and a model is required to learn from the series of past observations to predict the next value in the sequence.*

  > [Multivariate (multiLSTM)](../3_MultivariateForecast.ipynb)<br/>
    Where there is more than one observation for each time step, specifically, the multiple input series that has two or more parallel input time series and an output time series that is dependent on the input time series.

<br/>

<p align="center">
  <img src="https://user-images.githubusercontent.com/65748007/164270031-0799c24a-ded7-4445-9e23-c660f3ba3e6d.png" alt="Model metrics summary"/>
</p>
<p align="center">
    Generated preview of model metrics summary
</p>

---