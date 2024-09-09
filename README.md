# Econometrics
The notebooks that I worked on within my econometrics and data mining classes.

The .xlsx file is the main input file for the analysis. The file had it index transformed for the dates were not properly formatted.

## Evidence 1 Regression Models
The study aimed to predict the number of soft drink cases Coca-Cola needs to produce to meet the demand in the Guadalajara Metropolitan Area using regression models. The process involved several steps:  
1._Exploratory Data Analysis (EDA):_ The dataset was analyzed to identify missing values, review the data structure, and apply transformations, such as logarithmic transformation of sales and lag variables. Histograms and scatter plots were used to visualize data distribution and relationships.  
2. _Hypotheses Formulation_: Hypotheses were developed to test key variables' relationships, such as the positive impact of lagged sales and maximum temperature on current sales and the negative impact of inflation rate.  
3. _Regression Models:_
  * Base Linear Model: Initially included variables such as inflation rate, exchange rate, and unemployment rate but showed multicollinearity and heteroscedasticity issues.
  * Multiple Linear Regression (MLR): Focused on log-transformed sales, lagged sales, ITAEE growth, and log inflation rate, achieving lower RMSE with no multicollinearity.
  * Polynomial Regression: Added squared terms for variables like max temperature, further improving RMSE and identifying significant variables but with multicollinearity present.
  * Regularization Techniques (LASSO and Ridge): Used to refine variable selection and reduce overfitting. Both methods yielded competitive results with Ridge being slightly better in terms of RMSE.

4. _Model Selection:_ RMSE values were compared among models, with Polynomial Regression identified as the best model due to its balance of fit and interpretability.

5. _Key Findings:_
  * Lagged Sales Impact: There is a strong positive relationship between lagged sales and current sales, supporting the hypothesis that past sales are a strong predictor of current demand.
  * Temperature Effect: Maximum temperature positively impacts sales, indicating that higher temperatures drive higher demand for soft drinks, with squared temperature capturing non-linear effects.
  * _Inflation Impact_: The inflation rate had a mixed impact but generally showed expected relationships when logged, emphasizing the need for stable economic conditions to sustain demand.


## Evidence 2 Time Series Models
The objective is to determine the number of cases of Coca-Cola needed to satisfy the demand in the Guadalajara Metropolitan area. This involves forecasting sales based on historical data.
1. _Initial Data Exploration:_ Decomposition the sales time series into its constituent components—trend, seasonality, and residuals—to analyze how each component affects the overall data. 

2. _Stationarity and Autocorrelation Analysis:_ Augmented Dickey-Fuller, Ljung-Box test and autocorrelation plots.
3. _Transformation and Differencing:_ To address non-stationarity and autocorrelation, apply a natural logarithm transformation and differencing to the sales data.
4. _Model Selection and Fitting:_ Fit various time series models (ARMA, ARIMA, SARIMA, VAR) to the transformed sales data. Use criteria like the Akaike Information Criterion (AIC) to select the best-fitting model.
5. _Forecasting:_ Use the selected SARIMA model to forecast future sales for the next 5 periods. Convert the forecasted values from the log scale back to the original sales scale.
6. _Key Findings:_
   * Best for forecasting with the lowest AIC
   * Significant influence of temperature on sales according to VAR
   * Temperature positively impacts sales; adjust strategies accordingly
   * Inflation has no significant impact on sales
   * Overall prediction of an upward trend on sales
