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

The estimator combines overnight, open-to-close, and range-based components:

$$
\sigma^2_{YZ} = \sigma^2_{OV} + k \cdot \sigma^2_{RS} + (1-k) \cdot \sigma^2_{C}
$$

where:

$$
\sigma^2_{OV} = \frac{1}{n} \sum_{t=1}^{n} \left( \ln \frac{O_t}{C_{t-1}} \right)^2
$$

$$
\sigma^2_{C} = \frac{1}{n} \sum_{t=1}^{n} \left( \ln \frac{C_t}{O_t} \right)^2
$$

$$
\sigma^2_{RS} = \frac{1}{n} \sum_{t=1}^{n} \left( \ln \frac{H_t}{L_t} \right)^2
$$

$$
k = \frac{0.34}{1.34 + \frac{n+1}{n-1}}
$$

with:

$$
\{O_t}: \{opening} {price} {at} {time} {(t)}
$$

$$
\{C_t}: \{closing} {price} {at} {time} {(t)}
$$

$$
\{H_t}: \{high} {price} {at} {time} {(t)}  
$$

$$
\{L_t}: \{low} {price} {at} {time} {(t)}  
$$

$$
\{n}: \{number} {of} {periods}
$$


 # Sample Output
<img width="1190" height="590" alt="image" src="https://github.com/user-attachments/assets/4ccea435-e5b2-4a7d-8fca-481fab35f37a" />

    Estimated volatility Ticker
    AMD    3.975823
    dtype: float64
 

You are welcome to use this code. Any contribution to improve this model is appreciated.
