# Portfolio Optimization and Trading Strategies

This project focuses on implementing and analyzing various trading strategies using machine learning models and financial indicators. The strategies are applied to a portfolio of assets, including Bitcoin (BTC) - A Digital Currency, SPY (S&P 500 ETF), TLT (iShares 20+ Year Treasury Bond ETF) and Cash. The aim is to optimize portfolio allocation and maximize returns while managing risk. We extracted intraday data with a frequency of 30 minutes from the Bloomberg Terminal in order to explore potential intraday trading strategies. For BTC, 30 minutes intra-day data is available 24/7 throughout the year while for SPY and TLT, 30 minutes intra-day data is only available during US Market Hours. The list of assets in the portfolio and their intra-day closing prices from January 1, 2024 to 1 April 2025 can be found in **data/pricing_data.xlsx**. 

The portfolio performance will be evaluated during two periods: January to February 2025 (validation period, where trading algorithms updates are allowed) and March 2025 (the test period). 

We evaluated our portfolio performance with the following metrics:
1) Total Returns
2) Sharpe Ratio
3) Maximum Drawdown
4) Win Rate
5) Annual Volatility
6) Drawdown Patterns
7) Number of Trades

For our portfolio strategies, we relied on the following assumptions:
1) We do not allow for short selling.
2) There is no interest on the cash held on hand.
3) We use **close** prices for each asset class.
4) We impose 3bps in commission fees whenever we trade SPY or TLT and impose 5bps in commission fees whenever we trade BTC.

Our final trading strategy that we employed for the test period was **Random Forest with technical indicators**.

## Results in Test Period
| Metric        | Portfolio Performance    | 
|--------------|--------|
| Annual Return   | 374.13%   | 
| Return (Test Period)   | 14.6%   | 
| Sharpe Ratio | 5.13 | 
| Max Drawdown | -7.2%  | 
| Win Rate | 52.71%  | 
| Annual Volatility | 29.52%  | 
| Drawdown Patterns | 31  | 
| Number of Trades | 590  | 

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
1) src folder: Contains Jupyter Notebooks for our trading strategy.

2) data folder: Contains historical pricing data from January 2024 to 1 Apr 2025 for BTC, SPY, and TLT in the xlsx file named as **pricing_data.xlsx** as well as other processed data that contains results of our portfolio strategy.

In these folders, there are also archive folders. These contains results and codes of strategies that we tested but were not chosen as our ultimate trading strategy for our test period.

This project is an assignment from a NUS course - DSE4211: Digital Currencies.

Authors: Brandon, Jessica, Kelly, Kai Lin, Niyun

Special Thanks to Prof Chen Ying and Dr Dabin Wang for their guidance.

Last Updated: 19 April 2025
