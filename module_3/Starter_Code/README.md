#Assignment utilizes Pandas dataframes. 

##Data collection was done from the bitstamp.csv and coinbase.csv files, which contain the values of bitcoin
###Both files run from 2018-01-01 to 2018-03-31

##Data preparation included dropping 'NaN' values and duplicates, as well as using str.replace to remove the '$' to create floats. Then only closing price was considered for the analysis phase.

##Analysis included overlayed line charts that compared prices between exchanges. Summary data was used to help determine profitablility of each trade within one day and one month periods.
###Using data from specific days in early, middle, and late stages in the interval, arbitrage spreads were calculated and then used to get spread returns, which was needed to calculate profit per day. This was then used to get the total sum of profits and the cumulative sum of profits.
