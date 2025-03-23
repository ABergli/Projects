# Air Quality Prediction Project

This project involves analyzing air quality data collected from a chemical multi-sensor device in a polluted area of an Italian city. The dataset contains hourly averaged measurements recorded between March 2004 and February 2005. These measurements provide insights into air pollution levels over time.

## Project Overview
- **Dataset:** Includes 9358 hourly observations with sensor readings for air quality metrics.
- **Key Sensors Used:** Carbon Monoxide (CO), Nitrogen Dioxide (NO2), and Relative Humidity (RH).
- **Purpose:** To analyze the data and make short-term predictions for air quality using advanced modeling techniques.

## Steps Involved
1. **Understanding the Data**  
   - Explored the dataset to understand its structure and checked correlations between variables.

2. **Data Preparation**  
   - Preprocessed the data to handle missing values and ensured stationarity of time series.

3. **Modeling and Prediction**  
   - Used two approaches for predictive modeling:
     - **ARIMA Model:** Applied for univariate time series prediction.
     - **LSTM Model:** Leveraged deep learning for multivariate time series prediction.
   - Compared the results from both models to identify the most effective prediction approach.

4. **Results and Insights**  
   - Visualized the outcomes, presented concrete numbers, and critically evaluated the predictions.

## Tools and Methods
This project utilized Python and its libraries for data analysis and modeling:
- Data preprocessing: Pandas, NumPy
- Statistical analysis: KPSS and ADF tests
- Predictive modeling: ARIMA and LSTM (using TensorFlow/Keras)

## Outcome
By understanding air quality trends, this project provides valuable predictions for pollutant levels. The insights can assist in urban planning and pollution management efforts. The comparison between ARIMA and LSTM models highlights the effectiveness of each approach in handling time series data.




