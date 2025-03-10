# Stock Market Prediction using Machine Learning

## Overview
This project aims to predict the next day's closing price of Apple's stock using historical stock data. The project covers the entire workflow from data loading and exploratory analysis to feature engineering, model training, and evaluation using Linear Regression. With a strong baseline performance, this project lays a solid foundation for future work involving advanced machine learning and deep learning models.

## Dataset
The dataset used is Apple's historical stock data, which includes the following columns:
- **Date**: The trading date.
- **Open**: The opening price of the stock.
- **High**: The highest price reached during the trading day.
- **Low**: The lowest price reached during the trading day.
- **Close**: The closing price of the stock.
- **Adj Close**: The adjusted closing price (adjusted for dividends and splits).
- **Volume**: The number of shares traded.

## Project Structure
The notebook is organized into these key sections:

1. **Data Loading & Exploratory Data Analysis (EDA)**
   - Load the dataset and inspect its structure.
   - Plot the closing price to analyze trends.
   - Check for missing values.

2. **Feature Engineering**
   - **Technical Indicators:**
     - **Simple Moving Average (SMA):** 20-day average of the closing price.
     - **Exponential Moving Average (EMA):** 20-day weighted average emphasizing recent prices.
     - **Relative Strength Index (RSI):** 20-day momentum oscillator indicating overbought/oversold conditions.
   - **Date Features:**
     - Extract Year, Month, and Day from the Date column.
   - Additional engineered features (if any).

3. **Target Creation**
   - Create a continuous target variable representing the next day's closing price by shifting the 'Close' column by -1.
   - Remove the last row with a missing target.

4. **Train-Test Splitting**
   - Split the dataset chronologically (70% training, 30% testing) to mimic a real-world scenario.

5. **Model Training & Evaluation**
   - Train a Linear Regression model.
   - Evaluate performance using:
     - **Mean Absolute Error (MAE):** 2.30
     - **Mean Squared Error (MSE):** 10.46
     - **R² Score:** 0.9510
   - Visualize actual vs. predicted closing prices.
      ![Screenshot of model](C:\Users\Nitin\OneDrive\Desktop\ssb.png)
6. **Conclusion & Future Work**
   - Summarize the performance and key findings.
   - Outline potential future enhancements, including exploring advanced models like Random Forest and XGBoost.
     
## Performance Metrics
- **Mean Absolute Error (MAE):** 2.30  
  *On average, the predictions deviate from the actual closing price by about \$2.30.*
- **Mean Squared Error (MSE):** 10.46  
- **R² Score:** 0.9510  
  *Approximately 95% of the variance in the closing price is explained by the model.*

## How to Run the Project

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/Nitinbrock/Stock-Market-Prediction-using-ML.git
   cd Stock-Market-Prediction
2. **Install Required Libraries:**
    ```bash
   pip install numpy pandas matplotlib seaborn ta scikit-learn
4. **Launch the Notebook:**
    ```bash
   jupyter notebook stock_prediction.ipynb
