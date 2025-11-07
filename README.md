Retail Sales Forecasting (Historical Retail Dataset) – Step by Step

Environment setup

Installed and imported required libraries: Pandas, NumPy, Matplotlib, Seaborn for analysis and plotting.

Installed time series and ML libraries such as statsmodels, prophet, xgboost, TensorFlow/Keras for LSTM.

Data loading

Loaded the historical retail dataset from CSV.

Previewed the first rows to understand fields like YEAR, MONTH, SUPPLIER, ITEM CODE, ITEM DESCRIPTION, ITEM TYPE, RETAIL SALES, RETAIL TRANSFERS, WAREHOUSE SALES.

Initial exploration (EDA)

Used df.info() and df.describe() to check data types, missing values and basic statistics.

Plotted a correlation heatmap to see relationships between numerical features.

Drew a line chart of RETAIL SALES over time to see trends and seasonality.

Data preprocessing

Encoded categorical columns (SUPPLIER, ITEM DESCRIPTION, ITEM TYPE) using LabelEncoder so models can read them.

Converted ITEM CODE to numeric and handled errors.

Dropped rows with missing or non numeric values.

Selected features: YEAR, MONTH, SUPPLIER, ITEM CODE, ITEM DESCRIPTION, ITEM TYPE.

Set RETAIL SALES as the target.

Train test split and scaling

Split the data into training and testing sets (80 percent train, 20 percent test).

Standardised numeric features using StandardScaler to improve model performance.

Classical ML modelling

Trained three regression models:

Linear Regression

Decision Tree Regressor

XGBoost Regressor

Predicted sales on the test set.

Calculated error metrics (MAE, MSE) and compared the models.

Plotted actual vs predicted lines to see how close the models were.

Time series forecasting

Aggregated the data by YEAR and MONTH to create a monthly time series.

Created a proper datetime index.

Built an ARIMA model to forecast future retail sales.

Built a Prophet model to forecast 12 more months and visualised trend and seasonality.

Deep learning model (LSTM)

Reshaped the scaled data to 3D format for LSTM.

Built an LSTM network with dropout to reduce overfitting.

Trained for several epochs to learn sales patterns.

Evaluated predictions using MSE and compared with other models.

Model comparison

Collected all model results in a single dataframe.

Plotted a bar chart to compare errors across Linear Regression, Decision Tree, XGBoost and LSTM.

Observed which models worked better for structured features and which worked better for time series.

Business interpretation

Used forecasts to support inventory planning and replenishment.

Identified periods of higher sales so stock can be increased.

Showed that time series models like Prophet and ARIMA help in month ahead planning while ML models help when more product level features are used.
