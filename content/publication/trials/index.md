---
title: "Select and Trade: Towards Unified Pair Trading with Hierarchical Reinforcement Learning"
publication_types:
  - "3"
authors:
  - Weiguang Han
  - Qianqian Xie
  - Boyi Zhang
  - Min Peng
  - Yanzhao Lai
  - admin
author_notes: []
url_pdf: https://arxiv.org/abs/2301.10724
url_code: https://github.com/chancefocus/trials
url_benchmark: https://paperswithcode.com/paper/select-and-trade-towards-unified-pair-trading
publication: In *Arxiv*
publication_short: ""
abstract: "Pair trading is one of the most effective statistical arbitrage strategies which seeks a neutral profit by hedging a pair of selected assets. Existing methods generally decompose the task into two separate steps: pair selection and trading. However, the decoupling of two closely related subtasks can block information propagation and lead to limited overall performance. For pair selection, ignoring the trading performance results in the wrong assets being selected with irrelevant price movements, while the agent trained for trading can overfit to the selected assets without any historical information of other assets. To address it, in this paper, we propose a paradigm for automatic pair trading as a unified task rather than a two-step pipeline. We design a hierarchical reinforcement learning framework to jointly learn and optimize two subtasks. A high-level policy would select two assets from all possible combinations and a low-level policy would then perform a series of trading actions. Experimental results on real-world stock data demonstrate the effectiveness of our method on pair trading compared with both existing pair selection and trading methods."
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
date: 2023-03-28T06:49:52.462Z
---
