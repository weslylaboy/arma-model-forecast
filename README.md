### Building and Evaluating ARMA Models

The main task here is to pick a time series of interest, fit an ARMA model to it, make a basic forecast, and then assess how well it performs by analyzing the errors. It’s also a good idea to experiment with a few different combinations of
$p$ and $q$, since ACF and PACF plots are only rough guides. Running a small grid search often helps find better parameter values.


For this exercise, I worked with the [Rossmann Store Sales](https://www.kaggle.com/c/rossmann-store-sales) competition from Kaggle, which focuses on forecasting daily sales for a large retail chain.

------

**Further Extensions**

- SARIMA models that extend the ARMA model to include seasonal components.  Statsmodels contains a `SARIMAX` model that will accomplish this. Introduction from docs [here](https://www.statsmodels.org/dev/examples/notebooks/generated/statespace_sarimax_stata.html). 
- ARIMAX and SARIMAX models allow you to include external (exogenous) variables as part of the model. The Rossmann dataset provides plenty of potential features for this, and Statsmodels makes it straightforward to include them
- Feature Engineering with Time Series.  If you are presented with a basic time series like the sunspots data or airline data without exogenous features, these can be engineered from the series itself.  There are many approaches, but one library that can help is called `tsfresh` docs [here](https://tsfresh.readthedocs.io/en/latest/).