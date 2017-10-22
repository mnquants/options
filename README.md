# Options

## Resources
1. [Options Pricing: Black-Scholes Model - Investopedia](http://www.investopedia.com/university/options-pricing/black-scholes-model.asp)

## General Black-Scholes
blackScholes.R - prices put or call option with General Black-Scholes formula.
```
# test

install.packages("quantmod")
library(quantmod)

# NVDA price
getSymbols("NVDA", src="google")
# 1 year worth of closed prices
price <- NVDA$NVDA.Close["2016-09-26::"]

# assumes risk-free rate of 0.0123
blackScholes(priceTS = price, type = "c", strike = 180.00, days = 1, 
             rf = 0.0123, carryCost = 0.0)
```
