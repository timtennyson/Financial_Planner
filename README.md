# Financial_Planner

Welcome. This application serves two purposes: to determine whether or not a credit union member has enough funds in their savings for emergencies, and also to analyze risk/reward over time for a retirement portfolio over both 30 year and 10-year time frames.

## Technologies
[Python3.7](https://www.python.org/)

[Jupyter Lab](https://jupyter.org/)

[Pandas](https://pandas.pydata.org)

[Pathlib](https://docs.python.org/3/library/pathlib.html) 

[Matplotline](https://matplotlib.org/)

[requests](https://docs.python-requests.org/en/latest/)

[json encoder](https://docs.python.org/3/library/json.html)

[MCForecastTools](https://pbpython.com/monte-carlo.html)

[dotenv](https://pypi.org/project/python-dotenv/)

###APIs

[Alpaca Trading API](https://app.alpaca.markets/brokerage/new-account/overview)

[btc_url](https://api.alternative.me/v2/ticker/Bitcoin/?convert=USD)
[eth_url](https://api.alternative.me/v2/ticker/Ethereum/?convert=USD)


## Installation guide
In order to run this application you'll need to install Python3.7 in conjunction with jupyter lab along with the libraries linked above. You'll also need to setup an account with Alpaca (linked above), get your api keys, and save them into a .env file which is hidden in the code folder along with your code. 

## Part 1)-- Emergency Funds Analysis

### 1)Collect the data
Data is collected using known inputs for the client and historical price data is gathered using an API call to the Alpaca website, and crypto prices are found using a free public API (linked above).

### 2)Prepare the Data
The raw data is organized into dataframes so that it can be used to analyze the portfolio value and weights. These are a mix of crypto assets (BTC and ETH) bonds (AGG) and the S&P 500 index ETF (SPY).

### 3)Analyze the Data
After the inputs to calculate the value of the portfolio, it is charted to show the weights of each asset class.
There is also a calculator to assess whether or not the current portfolio value is enough to serve as an "emergency fund", or the equivalent of 3-month's salary for the client.

## Part 2)-- Monte Carlo Simulation

### Prepare the simulation

Here the api data is called again to get historical performance values for the client's portfolio.

### Run the simulation

Using MCForecastTools.py, a simulation is created to assess hypothetical outcomes for the portfolio over a thirty-year period weighted at 60% stocks(SPY) to 40% bonds(AGG).
The same simulation and graphs are then run and created for a 10-year period with an 80% stocks(SPY) to 20% bond(AGG) ratio.
The cumulative of both simulations are graphed on an overlay line plot as well as a histogram to present the data graphically, and to demonstrate the potential outcomes to the client.

## Conclusions

A portfolio that is more heavily weighted (80%/20%) in stocks can produce the same return in 10 years as a portfolio that is more balanced between stocks and bonds (60%/40%) can in 30 years, however there is considerably higher risk.

## Contributors

Tim Tennyson 
<ttennyson.xyz@gmail.com>

License: Open source, free distribution/reproduction