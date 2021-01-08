# Traditional Currency vs Paper Currency vs Cryptocurrency – which one should we invest in? 

## Table of Contents

    * Introduction
    * Purpose of the Project
    * Hypothesis
    * Technologies
    * Choice of Data Source and Cleaning
    * Calculations
    * Analysis


## Introduction:

It was only more than a decade ago when the world was brought to its knees by what is called the Global Financial Crisis (“GFC”) brought about by the housing bubble in the United States coupled with the excessive risk-taking behaviour by the banking sector. Now, the world is facing another global recession brought on by the Covid-19 pandemic. To say that the Covid-19 induced global recession could well be worse than the GFC may not be entirely false. The stock market crash in February of 2020 through end of March is seen as quick but the recession (and in some other countries, even a depression) was more lasting. There are predictions that some countries will only bounce back by year 2025. 

The measures taken by governments around the globe to have the pandemic under control included nationwide lockdowns and border closures which impacted trade and commerce both domestically and internationally. Tourism and hospitality are industries most negatively impacted resulting to significant rise in unemployment in these sectors. Consequently, unemployment caused food insecurity and rental and mortgage defaults. Governments around the globe had to step in to respond to the crisis by legislating stimulus packages which include monetary and/or fiscal stimulus to help businesses and individuals economically impacted by the pandemic. Stimulus packages calls for increased government spending and lowering of interest rates to fill in the output gaps in the economy. One effect of lowering interest rates is that the currency becomes less attractive to foreign investments thus weakening the exchange rate of the currency. This being said, how did the Covid-19 pandemic affect the US dollar as compared to gold and cryptocurrencies like the Bitcoin? Which of these currencies have responded negatively or positively to the pandemic and therefore which should one invest in considering that another black swan event like the Covid-19 pandemic may take place again?


## Purpose of the Project: 

    1.	Identify the best performing type of currency during a “normal period” and during the “pandemic period”.  Currencies under consideration are the USD, Gold, and the     Bitcoin. 
    
    2.	Provide simulated performances for each type of currency for both a “normal period” and a “pandemic period” to yield a forecast that will help illustrate which type of currency to invest in during “normal period” and a “pandemic period”.  
    
3.	Provide a visualisation of the findings based on the analysis conducted. 


## Hypothesis:

Factor: New Covid-19 outbreaks or mutation of Covid-19 against the vaccines

Independent Variable 1: If vaccine is effective and supply is efficient in 2021

      1. Economic recovery will put pressure on Bitcoin and Gold prices
      2. USD will be attractive again

Independent Variable 2: If there is a limited supply of vaccine or efficiency is lost due to virus mutation

      1. More or prolonged quarantine time or lockdowns which will result to additional stimulus package boosting safe haven assets
      2. Pressure on the value of the USD


## Technologies

   * Python language
   * NumPy
   * Matplotlib
   * Plotly
   * Seaborn
   * Bokeh


## Choice of Data Source and Cleaning

We have examined multiple data sources such as Alpaca, Quandl, FXCM, Alpha Vantage, Investing.com and Yahoo Finance.

### Alpaca 
Not Selected, as No Avaliable Data from Alpaca.

### Quandl 
Not Selected, as Missing Volume Data from Quandl.

### FXCM 
Not Selected, due to: 

         1) "tick quantity" is not volume but just an approximate for volume, and 
         2) need to convert the spread of bid/ask close to mid-close price.

### Alpha Vantage 
Not Selected, due to missing data for 2017.

### Investing.com 
Not Selected, due to: 

         1) No Volume Data from Investing.
         2) Extra cleaning need for Vol.
         
         However, Investing provides other useful data which might be used for the project, such as M2 money supply of USD. But, there is a large amount of missing daily data.
         
### Yahoo Finance
We have checked the data types, duplications, and missing data.  Yahoo Finance is Selected, as it provides highest data quality compared to other sources.


## Calculations

   * Historical daily returns
   * Cumulative returns of all portfolios
   * Averages for "normal period" and "pandemic period"
   * Daily standard deviation of all portfolios
   * Rolling moving averages for "normal period" and "pandemic period"
   * Rolling standard deviation using a 21-day window of each portfolio
   * Correlation during the "normal period" and "pandemic period"
   * Covariance, variance and rolling Beta during the "normal period" and "pandemic period"


## Analysis

### Asset Past Performance

Conducted a Return and Risk Analysis of Pre-covid and Covid period by initially extracting data from 2017-2019 data for pre-covid and 2020 data for covid period from the concatenated dataframe.

   * As seen on the graph, bitcoin is the most volatile among the other assets during pre-covid period whereas the other assets are pretty constant. However, during Covid Period, from March 2020 to September 2020 bitcoin has been relatively less volatile compared to pre-covid period. Conversely, gold return and SP500 have been relatively more volatile than in Pre-covid Period. 
   
   * While looking at the matrix that shows the correlation between the assets; during the pre-covid period, the correlation is near 0 which indicates that there is no linear relationship between the variables. During covid period, correlation between bitcoin and other assets increased, however, it's still close to 0. However, the correlation between the dollar return and the rest of the assets decreased.
   
   * As shown in the daily standard deviation dataframe; during covid, only standard deviation for bitcoin decreases whereas rest of the assets standard deviation increases. Even in the 21 window graph, it shows that volatility of SP500 has increased comparatively to the rest of the assets whereas the volatility of bitcoin has decreased.
   
   * After adjusting the risk, it is evident that bitcoin is the best performing asset during pre-covid and covid period. During pre-covid, bitcoin had a sharp ratio of 1.2 which is considered good for investors, whereas, during covid period bitcoin sharpe ratio was 2.3 which is considered very good by investors. The worst performing asset during both periods was the dollar. Hence, looking at the bar graph, investors would be more interested in bitcoin and gold as compared to the other two.
