Stock Forecasting with LSTM vs ARIMA
This project is part of the Data Scientist technical assessment for Mandiri Sekuritas. 
It compares two approaches for stock price forecasting: a statistical model (ARIMA) and a deep learning model (LSTM).

Project Structure
Christopher Joshua - Stock LSTM vs Arima Analysis.ipynb
Contains the full code implementation for LSTM and ARIMA-based forecasting on a selected stock.

Christopher Joshua_Mandiri Sekuritas.pptx
A concise presentation summarizing a research paper and the implementation findings. Meant for non-technical stakeholders with technical curiosity.

Objective
To review and apply a published research paper titled "An Advisor Neural Network framework using LSTM-based Informative Stock Analysis"
by Fausto Ricchiuti & Giancarlo Sperlí.

The project includes:

- A summary and critique of the paper
- A working implementation of ARIMA and LSTM models
- A comparison of their performance on short-term (7 days) and long-term (90 days) stock forecasts


Models
ARIMA: Applied as a statistical baseline for time-series forecasting.
LSTM: A shallow LSTM model was trained using past closing prices and additional indicators (RSI, MACD, MA).

Features Used
Historical Closing Prices
Relative Strength Index (RSI)
Moving Average Convergence Divergence (MACD)
Moving Average (MA)

Metrics
RMSE (Root Mean Square Error)
MAPE (Mean Absolute Percentage Error)

Key Findings
-Forecast Period	ARIMA (RMSE / MAPE)	LSTM (RMSE / MAPE)	Best Performer
 Short-Term (7d)	1.67 / 1.48%	2.60 / 2.59%	ARIMA
 Long-Term (90d)	7.86 / 6.56%	6.19 / 5.04%	LSTM
- ARIMA worked better for short-term prediction due to stability and lower complexity.
- LSTM showed advantages in capturing long-term trends, despite limited tuning.

Limitations
LSTM simplicity: Shallow model, no tuning or validation.
Missing features: Only uses closing price, ignores volume/news/sentiment.
Overfitting risk: No early stopping or regularization.
ARIMA assumption: Requires stationarity, may not hold in stocks.


Future Work
Add new features: Volume, news sentiment, etc.
Tune models: Optimize LSTM layers, dropout, window size.
Try hybrids: Combine ARIMA + LSTM or use Transformers.
Generalize: Test on more stocks especially with more volatility.
Forecast confidence: Add uncertainty bands or probabilistic models


Dependencies
Python 3.12+
Libraries: numpy, pandas, matplotlib, yfinance, statsmodels, sklearn, tensorflow
How to Run
Open Christopher Joshua - Stock LSTM vs Arima Analysis.ipynb in Jupyter Notebook.
Run all cells sequentially.
Review predictions and metrics for both models.
