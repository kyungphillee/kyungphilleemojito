# kyungphilleemojito

# Korean Stock Analysis

This repository contains a Python script that provides tools for analyzing Korean stocks from the KOSPI and KOSDAQ markets. Utilizing libraries like `mojito`, `yfinance`, and `pandas`, it provides insights into Korean stock performance over the years, including the ability to calculate various stock trading strategies.

## Features

1. **Retrieve Korean Stocks**: Fetch KOSPI and KOSDAQ stock symbols, process them, and produce a single DataFrame with the most relevant columns.
2. **Beta Calculation**: Get the beta values for each stock to assess their volatility relative to the broader market.
3. **Moving Average Crossover Strategy**: Implements a basic moving average crossover trading strategy and calculates its signals.
4. **Return Calculations**: Based on the generated signals, it computes daily and cumulative returns.
5. **Portfolio Creation & Visualization**: Using the signals, a hypothetical portfolio is created and its performance is visualized over time.
6. **Trade Simulation**: Simulates trading based on the moving average crossover strategy for various stocks.
7. **Max Sharpe Ratio Portfolio**: Identifies the portfolio weights that yield the maximum Sharpe ratio.

## Dependencies

To run the code, make sure to install the following Python libraries:
- mojito
- pprint
- pandas
- yfinance
- numpy
- matplotlib
- seaborn
- datetime
- functools
- joblib

## Setup

Ensure to provide the correct API keys and account number:
```python
key = "YOUR_API_KEY"
secret = "YOUR_API_SECRET"
acc_no= "YOUR_ACCOUNT_NUMBER"
```

## Usage

To start analyzing Korean stocks:

1. Call `get_korean_stocks()` to retrieve KOSPI and KOSDAQ stock data.
2. Use `get_beta_list()` to fetch beta values for a list of stocks.
3. Simulate trades using the `trade()` function.
4. Evaluate and visualize portfolio performance using the `max_sharpe_ratio_portfolio()` function.

**Note**: Some functions utilize caching mechanisms (`lru_cache` and `joblib.Memory`) to improve the efficiency of repeated function calls.

## Contribution

Feel free to fork this repository, make changes, and create a pull request if you think your changes can improve this project.

## Disclaimer

This tool is for educational purposes only. Any trading decisions based on this tool's output should be taken with caution, and it's always recommended to consult with a financial advisor.
```

Additionally, here are some code-related notes:

- The `key`, `secret`, and `acc_no` values are hard-coded. It's a security vulnerability to expose API keys and secrets directly in the code. You should consider storing them securely and referencing them indirectly in the code.
  
- You have a `try...except` block in the `get_beta_list` function, where you handle a general `Exception` by setting `beta = 1`. This may mask potential issues that you would want to be aware of. Always handle specific exceptions, and if necessary, log or handle generic exceptions in a manner that provides visibility into any unexpected behaviors.

- It's a good practice to have unit tests for each function to ensure they're behaving as expected. Given your emphasis on efficient, readable code and unit tests, you should consider adding a suite of tests for this code.

Would you like me to create unit tests for some of the functions?
