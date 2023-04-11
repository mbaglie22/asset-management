# Asset Management
This Github repository contains the solution to the "Portfolio Theory and Performance Analysis" assignment. The assignment involves two parts: equal risk-contribution portfolios and performance analysis. The first part focuses on constructing and backtesting portfolios with equal risk contribution weights, while the second part involves analyzing the performance of the Berkshire Hathaway portfolio and computing alpha, tracking error, and information ratios relative to the CAPM and Fama-French three factor benchmarks over different time periods. The code is written in Python, using popular data science libraries such as NumPy, Pandas, and SciPy. The repository includes a Jupyter notebook with the detailed solution and necessary data files.


## Performance Analysis

**1.6 Does high risk contribution of an asset necessarily correspond to high volatility for the same asset? Why?**

All of the constituents of the portfolio do not contribute equally to risk. 
For instance, if an investor would like to have a less risky portfolio, he won't have much impact by reducing the weight in the Telecom industry. This is because is not from that industry that volatility is coming from. The volatility of the portfolio is coming more from the Games, Cool, or Steel industry.

The plot helps us clearly state what are the individual contributions of these industries in risk, given the same weights. However, since constituents of the portfolio are all connected by covariance, volatility is flawed as a measure of risk. While it is true that a more volatile stock or bond exposes the owner to a wider range of possible outcomes (risk), it does not necessarily affect the likelihood of those outcomes. 

All in all, high risk contributions, in this case, correspond to high volatility, even if we should think that in the long-term,  risk contribution doesn't necessarily correspond to volatility. This is also because the risk is the probability that an investment will result in permanent or long-lasting loss of value, while volatility gives certain information about the dispersion of returns around the mean and is more useful in the short term. 
<img width="779" alt="image" src="https://user-images.githubusercontent.com/125969089/231177547-c19963ec-64f7-4523-bb32-9f6089d9ae74.png">


**1. 7 Interpret the results of ERC**
Given a targeted risk, we can adjust weights in order to have equal risk contribution (or almost) from each of the constituents. Stocks in industries with historically higher price volatilities are assigned lower portfolio weights with the goal that each stock will contribute an equal amount of estimated risk to the portfolio. Equal risk contribution principle and equal weight strategies coincide in the case industries have the same volatility. When, instead, individual risks differ, the weights differ as well. In this case, we now have assigned different weights in order to have the same risk contributions from all the constituents in the market. 

In the equal weights strategy (previous plot), we divide our wealth equally, resulting in different risk contributions whereas in the equal risk contributions we equalize the individual risk components. 
<img width="837" alt="image" src="https://user-images.githubusercontent.com/125969089/231177436-6384f558-f971-485e-bc66-b00e9246f271.png">


**1.10 Plot the four series of cumulated returns, and comment on the different performances of these three strategies.**
By plotting the returns of the four different strategies, we can see that the equal-weight strategy has more or less the same fluctuations as the equal risk contribution one. They both are more volatile than GMV and MSR, but at the same time, the returns are higher over time, compared to the other two strategies. 
The fundamental principle of ERC is to equalize risk contribution across the constituents of the portfolio. On the other hand, the global minimum variance portfolio allocates a given budget among n financial assets such that the risk for the rate of expected portfolio return is minimized. A Global Minimum Variance portfolio seeks to minimize the overall volatility of the portfolio and in fact, it is less volatile than the EW portfolio. 
However, by changing the estimation window, we should expect the Maximum Sharpe Ratio to be more stable, since we expect fewer fluctuations of the market. If the same changes happen, GMV becomes a little bit less volatile. The Sharpe ratio adjusts a portfolio's past performance—or expected future performance—for the excess risk that was taken by the investor. Maximum Sharpe Ratio strategy's performance brings overall negative returns over time. 
