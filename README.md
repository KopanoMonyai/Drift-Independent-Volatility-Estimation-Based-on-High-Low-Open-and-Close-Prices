# Drift Independent Volatility Estimation Based on High Low Open and Close Prices

Volatility is important as it determines the risk an investor is taking when investing, it gives confidence to the investor, as many investors are already reluctant when it comes to option contracts due to the many unpredictable factors that affect the price. It is for this reason that the prediction of volatility plays a very important role in the risk assessment, or pricing of option contracts e.t.c. In this project, we will consider the Yang-Zhang volatility estimator to estimate the volatility of an underlying variable using Python.

Yang-Zhang volatility estimator is a drift-independent volatility estimator that combines the overnight volatility, the open-to-close volatility, and the close-to-close volatility into one unbiased, efficient measure.

The following model dynamically calls stock prices from the yahoo finance.


# Positional Arguments

    ticker = Ticker symbol for the stock
    start = The beginning time period
    end = The end time period


# Call:

    ticker = 'AMD'
    start = "1980-01-01"
    end = "2025-01-01"
    df = yf.download(tickers= ticker,start=start, end=end)
    
    Output
        tmp/ipython-input-496447581.py:1: FutureWarning: YF.download() has changed argument auto_adjust default to True
        df = yf.download(tickers='AMD',start= "1980-01-01")
        [*********************100%***********************]  1 of 1 completed.

# Yang-Zhang volatility estimator
![PbijZ](https://github.com/user-attachments/assets/5185bd54-bacc-44c4-a3cc-e5a336e67c20)


 # Sample Output
<img width="1189" height="590" alt="download (1)" src="https://github.com/user-attachments/assets/8588cba5-84e4-432b-8fe3-ad2e81ad51c3" />

    Estimated volatility Ticker
    AMD    3.975823
    dtype: float64
 

You are welcome to use this code. Any contribution to improve this model is appreciated.
