---
title: FeedHandler
---

## ## #FeedHandler Data : You'll need a way to properly handle live market data, this isn't trivial especially if your strategy is latency dependent
##### For backtesting you can do with files, pulling data from databases and if you wish you can fetch from HTTP resources.
##### For actual trading you have to take into account that the streaming data will have to be handled in background threads and passed over to other components in a system standard form. Don't forget backfilling if you need to warm up data calculations.
##### In both cases and planning ahead for connecting to several systems, you need your own internal representation and convert from the external sources to your own, to make sure that the internals are not source dependent.