---
title: OMS
---

## ## OMS (order management system) aka Broker. You'll need at least a semi intelligent way of handling your orders after signal generation. It could be as simple as deciding whether to use a market or limit order, handling order cancellations to pretty much as complex as you could possibly think.
##### you need your own internal data decoupled from the actual API of any broker, to be able to support more than one (and switch amongst them)
##### A block managing your strategy. I.e: passing the data and notifications from the broker to your logic, so that the logic can actually act and do things (buy, sell, reverse ...)