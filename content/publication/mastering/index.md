---
title: "Mastering Pair Trading with Risk-Aware Recurrent Reinforcement Learning"
publication_types:
  - "1"
authors:
  - Weiguang Han
  - admin
  - Qianqian Xie
  - Boyi Zhang
  - Yanzhao Lai
  - Min Peng
author_notes: []
pdf: https://arxiv.org/pdf/2304.00364
publication: In *Arxiv*
publication_short: ""
abstract: "Although pair trading is the simplest hedging strategy for an investor to eliminate market risk, it is still a great challenge for reinforcement learning (RL) methods to perform pair trading as human expertise. It requires RL methods to make thousands of correct actions that nevertheless have no obvious relations to the overall trading profit, and to reason over infinite states of the time-varying market most of which have never appeared in history. However, existing RL methods ignore the temporal connections between asset price movements and the risk of the performed trading. These lead to frequent tradings with high transaction costs and potential losses, which barely reach the human expertise level of trading. Therefore, we introduce CREDIT, a risk-aware agent capable of learning to exploit long-term trading opportunities in pair trading similar to a human expert. CREDIT is the first to apply bidirectional GRU along with the temporal attention mechanism to fully consider the temporal correlations embedded in the states, which allows CREDIT to capture long-term patterns of the price movements of two assets to earn higher profit. We also design the risk-aware reward inspired by the economic theory, that models both the profit and risk of the tradings during the trading period. It helps our agent to master pair trading with a robust trading preference that avoids risky trading with possible high returns and losses. Experiments show that it outperforms existing reinforcement learning methods in pair trading and achieves a significant profit over five years of U.S. stock data."
draft: false
featured: true
tags:
  - neural network
  - reinforcement learning
  - pair trading
  - computational finance
projects: []
image:
  filename: ""
  focal_point: Smart
  preview_only: false
summary: ""
date: 2023-04-01T06:49:52.462Z
---
