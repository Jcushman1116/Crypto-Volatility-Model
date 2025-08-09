# Crypto Volatility Model

This repository contains code and resources to analyze and model the volatility of major cryptocurrencies, specifically Bitcoin (BTC) and Ethereum (ETH). The analysis includes data collection, cleaning, visualization, and statistical modeling, focusing on time series volatility models such as ARCH and GARCH.

## Features

- **Data Acquisition:** Downloads daily historical price and volume data for BTC and ETH using `yfinance`.
- **Preprocessing:** Cleans and prepares data, computes returns, log returns, and their squared values.
- **Visualization:** Plots returns, log returns, and volatility measures for both BTC and ETH.
- **Stationarity Testing:** Applies Augmented Dickey-Fuller (ADF) tests to check for stationarity of returns and volatility series.
- **ARCH Effect Testing:** Uses the ARCH Lagrange Multiplier test to detect conditional heteroskedasticity.
- **Modeling:** Prepares the data for volatility modeling with ARCH/GARCH models, focusing on data series that meet necessary statistical assumptions.

## Getting Started

### Prerequisites

- Python 3
- Install the required dependencies:
  ```bash
  pip install pandas numpy matplotlib statsmodels arch scikit-learn yfinance seaborn
  ```

### Usage

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Jcushman1116/Crypto-Volatility-Model.git
   cd Crypto-Volatility-Model
   ```

2. **Run the Jupyter Notebook:**
   ```bash
   jupyter notebook Crypto_Vol_model.ipynb
   ```
   Follow the notebook cells step-by-step to reproduce the data exploration and analysis.

## Project Structure

- `Crypto_Vol_model.ipynb`: Main Jupyter notebook containing the full workflow from data download to statistical testing and exploratory data analysis.
- `README.md`: This file.

## Methodology

1. **Data Collection:** Daily OHLCV data for BTC and ETH are retrieved from Yahoo Finance.
2. **Data Cleaning:** Missing values are backfilled. New columns for returns, log returns, and their squares are computed.
3. **Visualization:** Several plots are generated to visualize returns and volatility.
4. **Statistical Testing:**
    - Stationarity of the returns and volatility is checked using ADF tests.
    - ARCH LM tests are performed to check for the presence of ARCH effects.
5. **Model Selection:** Based on the results of the statistical tests, appropriate series are selected for ARCH/GARCH modeling.

## Notes

- The analysis focuses on the most recent 1.5 years of data to better reflect current market behavior.
- The results indicate that BTC series are suitable for ARCH/GARCH modeling, while ETH series may not meet the necessary assumptions.
- This project is for educational and research purposes and should not be construed as financial advice.

## Author

- [Jcushman1116](https://github.com/Jcushman1116)

## Acknowledgements

- [yfinance](https://github.com/ranaroussi/yfinance)
- [statsmodels](https://www.statsmodels.org/)
- [ARCH package](https://github.com/bashtage/arch)
- [scikit-learn](https://scikit-learn.org/)
