---
title: Building a trading system
---

## **Examples of systems built in python:**
### [PyAlgoTrade](https://github.com/gbeced/pyalgotrade)
### [ccxt: Cryptocurrency exchange trader. Fully fledged system](https://github.com/ccxt/ccxt)
### [vnpy - Docs in Chinese but can be translated. This seems like a fully fledged platform](https://www.vnpy.com/docs/cn/index.html) and github [link](https://www.vnpy.com/docs/cn/index.html)
### [backtrader  - mianly for trying things out. Lacks trading functionality](https://github.com/mementum/backtrader)
#### Some nice examples here: https://www.backtrader.com/home/helloalgotrading/
### [Lean engine: An open source algorithmic trading enegine built for east strategy research, backtesting and live trading - written in C# and integrates with common ata providers. Supports algos written in #Python 3.6](https://github.com/QuantConnect/Lean)
## **Blog posts**
###### [tia Toolkit for integration and analysis](https://github.com/bpsmith/tia)
####### [QuantSoftware Toolkit](http://wiki.quantsoftware.org/index.php?title=QuantSoftware_ToolKit)
### [Beginner’s Guide to Quantitative Trading II: Developing Automated Trading Systems](https://medium.com/auquan/beginners-guide-to-quantitative-trading-ii-developing-automated-trading-systems-4c967e544f34)
#### **What are core-components of a trading systems**
##### #FeedHandler Data
##### #OMS (order management system) aka Broker
##### #PMS (#position management system)
##### #PLProfitLoss
##### #Otherthings
###### Adding Indicators / Analyzers (you may not need them if you for example work on pure bid/ask prices)
###### Charting (whether real-time or only for the backtesting results)
###### Collection of real-time data (although it's a lot better to rely on a reliable data source)
###### ****Start slow by being able to backtest something****:
####### 1. Read a csv file
####### 2. Loop over the data
####### 3. Pass each bar to a Simple Moving Average that calculates the last value
####### 4. Pass each bar to the trading logic (which will rely on a Simple Moving Average to make decisions)
####### #backtesting As inspiration (or simply to use any of them) you can have a look at this list of [[Softwaretools]] Open Source #Python frameworks:
######## [backtrader](https://www.backtrader.com) (Disclaimer: author here
######## [PyAlgoTrade](https://github.com/gbeced/pyalgotrade)
######## [Zipline](https://github.com/quantopian/zipline)
######## [pybacktest](https://github.com/ematvey/pybacktest)
######## [prophet](https://github.com/Emsu/prophet)
######## [quant](https://github.com/maihde/quant)
######## [tia Toolkit for integration and analysis](https://github.com/bpsmith/tia)
######## [QuantSoftware Toolkit](http://wiki.quantsoftware.org/index.php?title=QuantSoftware_ToolKit)
### **What [[strategies]] will I use**
#### [[Medium strategies]]
#### [[Long Strategies]]
#### [[Machinelearning]]
#####
:PROPERTIES:
:todo: 1610961039186
:END:
---
title: welfairy
---

## We need to get tsechu to a better mental place. How are we going to do it, by giving her something to do.
##### We can use the welfairy.com domain
###### DONE Use Amplify
:PROPERTIES:
:done: 1610972914123
:END:
###### DONE transfer domain to AWS
:PROPERTIES:
:doing: 1610972898918
:done: 1612098704441
:END:
###### DOING add mxnet protocals create email on zoho
:PROPERTIES:
:doing: 1610972905921
:END:
###### DONE Add template page
:PROPERTIES:
:doing: 1610972909919
:done: 1612129651135
:END:
##### Lets create a journal for mental health using logseq! We will host our own logseq and you can write notes everyday.
##### Analyze notes to find the semanic meaning - are they happy, sad, etc
###### look at longer term and periodically, how, semantically is their mood changing
##### TODO Work through tis python flask + bootstrap tutorial to set up authentication with google. https://www.mattbutton.com/2019/01/05/google-authentication-with-python-and-flask/
:PROPERTIES:
:todo: 1612129676346
:END:
#####
#####
