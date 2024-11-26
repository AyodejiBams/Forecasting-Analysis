# Unemployment Rate Forecasting

## Project Description
This project explores time series forecasting techniques applied to the unemployment rate in the United States. It incorporates multiple models, including the **Holt-Winters Model**, **ARIMA**, and a mock **VAR (Vector Autoregression)** model, to analyze historical trends and predict future unemployment rates. The analysis compares the models based on their performance and evaluates their forecasting accuracy.

---

## Part B: Holt-Winters Model

### **1. Forecast Analysis**
- The forecast predicts unemployment rates over the next **12 months**, aligning with historical trends.
- The model accounts for both **seasonal** and **trend components** in the time series data.

### **2. Holt-Winters Model Parameters**
- **Smoothing Level:** 0.867 (approx)
- **Smoothing Trend:** 0.276 (approx)
- **Smoothing Seasonal:** 0.0
- **Initial Level:** 4.94 (approx)
- **Initial Trend:** -0.111 (approx)
- **Initial Seasons:** Array of values for each month
- These parameters were **automatically optimized** during the model fitting process.

### **3. Forecast and Prediction Interval**
- The forecasted unemployment rates for the next 12 months are visualized in the graph.
- **Note:** The basic Holt-Winters model does not calculate prediction intervals. Advanced implementations can provide this feature.

---

## Part C: ARIMA Model

- The ARIMA model was explored as a time series forecasting method. Its detailed analysis and results were used to compare performance with the Holt-Winters model.

---

## Part D: VAR Model (Mock Analysis)

### **1. Vector Autoregression Overview**
The VAR model is typically designed to analyze interdependencies between multiple time series. It provides insights into how each variable is influenced by:
- Its own past values
- The past values of other variables in the system

### **2. Current Setup and Limitations**
- **Single Variable Limitation:** The analysis focused solely on the unemployment rate. Due to tool limitations, the Federal Funds rate was not incorporated.
- **Mock VAR Forecast:** The provided visualization represents a **mock analysis** and does not reflect a true VAR model.

### **3. Theoretical Insights**
- **Economic Theory:** According to the **Phillips Curve**, there is often an inverse relationship between unemployment and inflation. Central banks, through tools like the Federal Funds rate, can influence inflation, indirectly impacting unemployment rates.
- The analysis, however, does not empirically confirm or explore this relationship.

---

## Part E: Models Comparison

### **1. RMSE and MAE Calculations**
| **Model**         | **RMSE**   | **MAE**    |
|--------------------|------------|------------|
| Holt-Winters       | 2.444939   | 2.189461   |
| ARIMA             | 0.998446   | 0.782566   |

### **2. Model Comparison and Justification**
- The **ARIMA model** outperforms the Holt-Winters model with significantly lower **RMSE** and **MAE** values.
- **Conclusion:** ARIMA is more reliable for this dataset and forecasting horizon.

---

## Key Takeaways
- **Holt-Winters Model:** Effective for capturing trends and seasonality, but lacks the precision of ARIMA for this dataset.
- **ARIMA Model:** Provides higher accuracy, making it the preferred choice for unemployment rate forecasting.
- **VAR Model (Mock):** Highlights the theoretical relationship between unemployment and other macroeconomic variables but requires further exploration with appropriate tools.

---

## Acknowledgments
- **Dataset Source:** Historical unemployment rate data
- **Tools Used:** Python, Tableau, and other time series libraries
