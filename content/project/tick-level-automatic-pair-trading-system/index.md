---
title: Tick-level automatic pair trading system
subtitle: TAPTS
date: 2020-09-01T12:43:11.168Z
draft: false
featured: true
authors:
  - admin
  - Mingshi Cai
  - Xinyuan Dai
  - Jie Yang
  - Weiguang Han
tags:
  - Computational Finance
image:
  filename: 回测-交易核心.png
  focal_point: Smart
  preview_only: false
  caption: System Design(In Chinese)
---
## Motivation
It is reported that holding two different types of assets for hedging can significantly reduce the risk compared with a single asset. In real applications, fund managers also seek to control the volatility of the portfolio after opening the position. Therefore, pair trading which exploits a pair of assets and trades in different directions gains more attention in both academic and industrial areas. Generally, it consists of two phases: 1) first it should select appropriate asset pairs according to historical performance, 2) and second it will trade and determine whether it should open or close the position based on real-time data. Apart from designing algorithms for selecting and trading, it also requires a real-time automatic trading system that can receive tick-level trading data, generate trading signals and send orders without human efforts.

## Challenges
There are three major issues or features required in this system:
- Real-time data processing: it should have the capability to receive all the trading data of all stocks and index futures at tick level, namely that 4000+ points per 1.5 seconds and 300+ million points per day.
- Real-time strategy generation: it should notify the trading algorithms with historical and latest data, which should generate trading signals less than 0.5s.
- Real-time trading execution: it should send orders and update position and holding status in 0.5s.

Notice that we also should design the backtest and trading framework simultaneously to ensure that our strategy can directly switch between these two frameworks without any modifications.

## Major tasks
|      | Data           | Strategy                   | Execution               |
|------|----------------|------------------------|--------------------|
| Backtest | Historical data in hundreds of millions level | Backtest framework     | Fake matching and trading |
| Trading | Tick-level data | Trading framework | Tick-level execution system |

## Timeline
![](timeline.svg, "Timeline(In Chinese)")
