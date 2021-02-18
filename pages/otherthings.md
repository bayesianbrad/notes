---
title: Otherthings
---

## ## [Beginner’s Guide to Quantitative Trading II: Developing Automated Trading Systems](https://medium.com/auquan/beginners-guide-to-quantitative-trading-ii-developing-automated-trading-systems-4c967e544f34)
### **What are core-components of a trading systems**
#### #FeedHandler Data
#### #OMS (order management system) aka Broker
#### #PMS (#position management system)
#### #PLProfitLoss
#### #Otherthings
##### Adding Indicators / Analyzers (you may not need them if you for example work on pure bid/ask prices)
##### Charting (whether real-time or only for the backtesting results)
##### Collection of real-time data (although it's a lot better to rely on a reliable data source)
##### ****Start slow by being able to backtest something****:
###### 1. Read a csv file
###### 2. Loop over the data
###### 3. Pass each bar to a Simple Moving Average that calculates the last value
###### 4. Pass each bar to the trading logic (which will rely on a Simple Moving Average to make decisions)
###### 5. Issue an order if needed be (start with a Market order)
###### 5.1 Work first with a wrong approach: use the current close for the matching
###### **You can then**:
###### 2.1 Add a broker which sees if any order is pending and try to match it
###### 5.1 Instead of matching the order, pass it with a call (queue, socket or what you want) to the broker, for the next iteration
###### #backtesting As inspiration (or simply to use any of them) you can have a look at this list of [[Softwaretools]] Open Source #Python frameworks:
####### [backtrader](https://www.backtrader.com) (Disclaimer: author here
####### [PyAlgoTrade](https://github.com/gbeced/pyalgotrade)
####### [Zipline](https://github.com/quantopian/zipline)
####### [pybacktest](https://github.com/ematvey/pybacktest)
####### [prophet](https://github.com/Emsu/prophet)
####### [quant](https://github.com/maihde/quant)
####### [tia Toolkit for integration and analysis](https://github.com/bpsmith/tia)
####### [QuantSoftware Toolkit](http://wiki.quantsoftware.org/index.php?title=QuantSoftware_ToolKit)