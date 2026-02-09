### Building and Evaluating ARMA Models

The main task here is to pick a time series of interest, fit an ARMA model to it, make a basic forecast, and then assess 
how well it performs by analyzing the errors. It’s also a good idea to experiment with a few different combinations of
$p$ and $q$, since ACF and PACF plots are only rough guides. Running a small grid search often helps find better parameter values.


For this exercise, I worked with the [Production and sale of cement bags](https://indicadores.pr/dataset/f1b1d002-5958-431a-abfe-539ce3814018/resource/806d9de9-c2ee-4506-b6fc-ed2990a54561/download/datos_cemento.csv),
which contains monthly data on the production and sales of 94 lb sacks of cement in Puerto Rico.

------

**Further Extensions**

- SARIMA models that extend the ARMA model to include seasonal components.  Statsmodels contains a `SARIMAX` model that 
will achieve this. Introduction from docs [here](https://www.statsmodels.org/dev/examples/notebooks/generated/statespace_sarimax_stata.html). 

- ARIMAX and SARIMAX models allow you to include external (exogenous) variables as part of the model. If you have access
to exogenous features that are relevant to the time series, these can be included in the model and may improve forecasts.  
For example, if you are modeling sales of a product, you might include advertising spend as an exogenous variable. 
If you are modeling energy consumption, you might include temperature as an exogenous variable.  
Statsmodels has `ARIMAX` and `SARIMAX` models that allow for this.

- Feature Engineering with Time Series.  If you are presented with a basic time series like the sunspots data or airline
data without exogenous features, these can be engineered from the series itself.  There are many approaches, but one 
library that can help is called `tsfresh` docs [here](https://tsfresh.readthedocs.io/en/latest/).