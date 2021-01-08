# project_one



#**Choice of Data Source and Cleaning:**
We have examined multiple data sources such as Alpaca, Quandl, FXCM, Alpha Vantage, Investing.com and Yahoo Finance.

**Alpaca**
Not Selected, as No Avaliable Data from Alpaca. 
**Quandl**
Not Selected, as Missing Volume Data from Quandl.
**FXCM**
Conclusion: Not Selected, due to:
1) "tick quantity" is not volume but just an approximate for volume, and
2) need to convert the spread of bid/ask close to mid-close price.
**Alpha Vantage**
Not Selected, due to missing data for 2017.
**Investing.com**
Not Selected, due to
1) No Volume Data from Investing.
2) Extra cleaning need for Vol.
However, Investing provides other useful data which might be used for the project, such as M2 money supply of USD. But, there is a large amount of missing daily data.
**Yahoo Finance**
We have checked the data types, duplications, and missing data.  Yahoo Finance is Selected, as it provides highest data quality comparing to other sources.


#**Portfolio Optimization:**
Since these assets are not perfectly correlated. Forming a portfolio could reduce overall volatility for a defined expected return.
The efficient frontier is the set of optimal portfolios that offers the highest expected return for a same level of risk, in the other words, the optimal portfolio gives the highest Sharpe ratio. Any portfolios below the efficient frontier are sub-optimal. 
Due to the curve shape of the efficient frontier, to find the true global minima, we applied the sequential least squares programming (SLSQP) optimizer from Scipy to calculate the optimal weighting with the objective of minimizing a negative Sharpe ratio which is equivalent to maximizing a positive Sharpe ratio of the portfolio.

#**Finding:**
We have found the optimal portfolio weighting for the “Normal” 2017-2019, verse the “Epidemic” 2020, as displayed in the table.
![Optimization](Resources/images/Optimization.png)

Interestingly and firstly, under these scenarios, US Dollar futures is the least favorable asset to be included. Especially for the “Epidemic” scenario, the result suggests to avoid investing in US Dollar.
Secondly, under the “Epidemic” scenario, although the assets are more volatile, Gold and Bitcoin performed much better and the portfolio could produce a much higher Sharpe ratio (2.37) comparing to under “Normal” scenario (1.47). The reason could be that investors were seeking a more defensive approach by investing more wealth into Gold and Bitcoin to against market uncertainty and inflation.


