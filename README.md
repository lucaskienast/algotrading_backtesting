# Algotrading Backtesting
In this project, I built a fairly realistic backtester that uses the Barra data. The backtester performs portfolio optimization that includes transaction costs, and I implemented it with computational efficiency in mind, to allow for a reasonably fast backtest. I also used performance attribution to identify the major drivers of the portfolio's profit-and-loss (PnL).

## Installation
Use `git clone` to get a copy of this repository.
```
$ git clone https://github.com/lucaskienast/algotrading_random_forest_enhanced_alpha.git
$ cd algotrading_random_forest_enhanced_alpha
```

## Method
- load preprocessed Barra data from `pickle` files
- shift daily returns data
- winsorize to clip our values to a minimum and maximum range
- compute factor exposures using an OLS regression of factor and regular returns
- choose alpha factors
- merge previous portfolio holdings
- filter stock universe for companies with market value of over 1 billion dollars
- get matrix of risk factor exposures
- calculate specific variance
- get factor covariance matrix
- implement transaction costs
- get matrix of alpha factor exposures
- implement objective function and gradient
- run optimization
- put everything together and build trade list
- run backtest
- perform profit-and-loss (PnL) attribution
- build portfolio characteristics
- 

## Results
PnL mostly attributed to alpha factors and very little to risk factors. Gross market value of portfolio very volatile, but increasing.
