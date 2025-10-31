# Drift-Independent-Volatility-Estimation-Based-on-High-Low-Open-and-Close-Prices
# geometric-brownian-motion
Volatility is important as it determines the risk an investor is taking when investing, it gives confidence to the investor, as many investors are already reluctant when it comes to option contracts due to the many unpredictable factors that affect the price. It is for this reason that the prediction of volatility plays a very important role in the pricing of option contracts. In this project, we will consider the Yang-Zhang volatility estimator to estimate the volatility of an underlying variable using Python.

Yang-Zhang volatility estimator is a drift-independent volatility estimator that combines the overnight volatility, the open-to-close volatility, and the close-to-close volatility into one unbiased, efficient measure.

The following model dynamically calls stock prices from the yahoo finance.


# Positional Arguments
    ticker = Ticker symbol for the stock
    history_period = The time period in days you want to look back


# Call eg:
    yf.download(tickers='AMD',start= "1980-01-01")

    Output
        tmp/ipython-input-496447581.py:1: FutureWarning: YF.download() has changed argument auto_adjust default to True
  df = yf.download(tickers='AMD',start= "1980-01-01")
[*********************100%***********************]  1 of 1 completed.

# Yang-Zhang volatility estimator
            plt.figure(figsize=(12, 6))
            plt.plot(df.index, yz_vol, label="Yang-Zhang Volatility", color="blue")
            plt.title("Estimated Volatility Over Time")
            plt.xlabel("Date")
            plt.ylabel("Volatility (Standard Deviation)")
            plt.grid(True)
            plt.legend()
            plt.tight_layout()
            plt.show()
 # Sample Output
<img width="1189" height="590" alt="download" src="https://github.com/user-attachments/assets/c37163dd-9562-46d3-b25a-0c2d167be641" />

 

You are welcome to use this code. Any contribution to improve this model is appreciated.
