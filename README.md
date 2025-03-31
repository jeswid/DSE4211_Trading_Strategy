# Portfolio Optimization and Trading Strategies

This project focuses on implementing and analyzing various trading strategies using machine learning models and financial indicators. The strategies are applied to a portfolio of assets, including Bitcoin (BTC) - A Digital Currency, SPY (S&P 500 ETF), TLT (iShares 20+ Year Treasury Bond ETF) and Cash. The aim is to optimize portfolio allocation and maximize returns while managing risk. We work with intraday data with a frequency of 30 minutes in order to explore potential intraday trading strategies. For BTC, 30 minutes intra-day data is available 24/7 throughout the year while for SPY and TLT, 30 minutes intra-day data is only available during US Market Hours. The list of assets in the portfolio and their intra-day closing prices from January 1, 2024 to 28 March 2025 can be found in **data/pricing_data.xlsx**. 

The portfolio performance will be evaluated during two periods: January to February 2025 (validation period, where trading algorithms updates are allowed) and 28 March 2025 (the test period). 

We evaluated our portfolio performance with the following metrics:
1) Total Returns
2) Maximum Drawdown

For our portfolio strategies, we relied on the following assumptions:
1) We do not allow for short selling.
2) There is no interest on the cash held on hand.
3) We use **close** prices for each asset class.
4) We impose 3bps in commission fees whenever we trade SPY or TLT and impose 5bps in commission fees whenever we trade BTC. 

## Guide to the Repository
To use the code, clone the repository with Git:
```
git clone https://github.com/jeswid/DSE4211_Trading_Strategy.git
```
Alternatively, download the repository as a ZIP file and extract it.

**Prerequisites**
Ensure you have Python installed along with the required libraries. Install dependencies using:
```
pip install -r requirements.txt
```

**Repository Structure** 
1) src folder: Contains Jupyter Notebooks for data processing, feature engineering, model training, and backtesting.

2) data folder: Contains historical pricing data from January 2024 to 28 March 2025 for BTC, SPY, and TLT in the xlsx file named as **pricing_data.xlsx** as well as other processed data that contains results of our portfolio strategy. 

This project is an assignment from a NUS course - DSE4211: Digital Currencies.

Authors: Brandon, Jessica, Kelly, Kai Lin, Niyun

Special Thanks to Prof Chen Ying and Dr Dabin Wang for their guidance.

Last Updated: 5 April 2025
