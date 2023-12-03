# NASDAQ-Unveiled-Strategies-for-Predicting-Closing-Auctions
 Files and details for diverse models predicting Nasdaq's closing auction uncross values

In partnership with the market maker Optiver, Kaggle is hosting a competition focused on predicting the short term price movements in the closing auction for NASDAQ companies. For our final project, we would like to try to create a competitive model in this competition.

**The Problem**

Every business day, markets host an ‘auction’ in the last 10 minutes of trading (usually, from 3:50-4:00 pm EST). Market participants submit orders into the auction consisting of ‘bids’–a price that the market participant would like to buy a stock at–and ‘asks’–a price that a stockholder would wish to sell a stock at. Naturally, ask prices tend to be higher than bid prices, as those willing to sell the stock want to get a higher price for their sale then those wishing to buy. This means that matching ask and bids (which corresponds to a completed trade) is an optimization problem: finding the final closing price (the market must decide on a single price by the end of the auction) that maximizes the number of trades which occur. Such a price is called the ‘uncross’ price, and market participants can attempt to predict the uncross price at close.
 
The problem of optimizing the cross-price is baked into the larger problem of predicting the short term movements of the cross-price throughout the auction. As orders come in during the 10 minutes the auction is open, market makers will continually work on the problem of finding the best auction price in order to decide if/how they should enter the auction. 
 
**The Data**

The data provided by Kaggle is historical data of the daily closing auction order books for over 200 different stocks. The rows of the data give a glimpse of the current values in the book for a given time. Columns include current number of bids, current number of asks, the current reference price, the bid-ask imbalance (the number of unmatched orders at the reference price), as well as other statistics which characterize these core figures. There are 5 million rows in the Kaggle data and these rows are uniquely indexed by a combination of date, stock ID, and time (bucketed by the second).
 
**Potential Models**

The problem of predicting the close price is a time series problem, and so we expect to find the best results with models that work well with time series data. Cursory research on this topic suggests that XGBoost as well as various Neural Net architectures provide the most competitive outcomes for time series problems.
 
We have reason to believe that data preprocessing could play a large role in forming accurate predictions. Countless financial models have been made that try to predict movements in the stock market, and many metrics have been invented for guessing the short term price movements of a stock. Many of these models and indicators do not work, but some are able to transform the data in a meaningful way so that additional insight can be gleaned from the largely random walks of stock prices. 
 
**Business Application**

This problem has obvious implications for market makers and stock market participants, but the more general problem of predicting time series data is a problem inherent to many industries. By engaging with this problem, we hope to gain valuable transferable skills to other domains as well. 

**Reference**
[1]https://towardsdatascience.com/forecasting-stock-prices-using-xgboost-a-detailed-walk-through-7817c1ff536a

[2] https://dl.acm.org/doi/pdf/10.1145/3573834.3573837

