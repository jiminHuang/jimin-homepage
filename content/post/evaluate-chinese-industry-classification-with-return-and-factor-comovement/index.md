---
title: Evaluate Chinese industry classification with return and factor comovement
date: 2021-06-30T16:35:55.841Z
summary: ""
draft: false
featured: false
authors:
  - admin
  - Qianqian Xie
  - Yanzhao Lai
  - Min Peng
  - ""
tags:
  - Computational Finance
projects:
  - the-comparison-and-analysis-of-chinese-industry-classifications-for-stocks
image:
  filename: ""
  focal_point: Smart
  preview_only: false
---
## Introduction
Industry classification is fundamental to finance research. For example, previous researches generally utilize the industry classification to exploit new anomalies in asset pricing and choose pair company in asset valuation[1]. It is also employed in analyst evaluation to compare the ability of different analysts[4,8,18]. [12] summarized papers that were published in top journals of financial and accounting areas, and reported that around 30% of researches introduced industry classification.

The reason behind the rising popularity of industry classification in the financial area is that the similarity of stocks in the same industry demonstrates the deeper correlations between companies in managing, pricing, and investment, which can effectively explain the volatility of asset prices. Chou et al. [15] found that industry can affect the factors of stocks in both rational and behavioral finance. Bustamante et al. [17] pointed out that the concentration of industry is an important factor of asset pricing. Scislaw et al. [28] demonstrated that the aggregated fundamental characteristics differ between industries, which provide opportunities to investors.

There were three major industry classifications (IC) in the Chinese stock market: The China Securities Regulatory Commission Industry Classification (CSRCIC), Shenyin Wanguo Industry Classification (SWIC). Notice that CSRCIC was modified and perfected in 2012 and SWIC updated in 2014. Therefore we would compare these three ICs after 2014. Besides, we also include researches that cluster stocks via machine learning methods.

Previous research in the Chinese stock market[2] only considered CSRCIC and GICS, neglecting the widely adopted SWIC. Moreover, they only analyze the difference in ROE and P/E, and ignore a series of important indicators such as monthly profit. Similar to methods that focus on other stock markets [33, 3, 4, 19, 20, 25, 24, 40, 41], we examine the correlations of stocks in the same industry under different ICs. For each IC, we build an equal-weight industry portfolio and regression the indicators of the portfolio to the indicators of all stocks in the industry. The adopted indicators of this research can be divided into three categories: 1) profit: referring to the relatedness of stocks in profit; 2) valuation multiples: demonstrating the correlations of stocks in value, including ROE, PB, PE, AT, and PM; 3) factors: including liquidity, momentum, quality, and dividend. We also compare their performance in component stocks of several indexes, to further investigate their effect in different markets.

The experimental results demonstrate the superiority of SWIC among ICs, and the 4-digit IC can achieve the best performance considering the number, size, and concentration of industries. Similar to previous researches, we also report that ICs based on clustering underperform existing ICs. When comparing factors in all ICs, it is shown that momentum and volatility factors are more consistent than liquidity and quality factors. For indexes, we found that CSI300 presents better performance than CSI500.

## Data
We perform experiments on Chinese stock market data between 2014 and 2020 in three different stock pools: all stocks, component stocks of CSI300, component stocks of CSI500. The industry numbers of the data are displayed below:

|        | SWIC |     |     | CSRCIC |
|--------|------|-----|-----|--------|
| digits | 2    | 4   | 6   | 2      |
| all    | 28   | 104 | 227 | 81     |
| CSI300 | 27   | 72  | 113 | 34     |
| CSI500 | 28   | 93  | 164 | 65     |

We also present the statistics of ICs:
### All stocks

|          | SWIC   |        |        | CSRCIC |
|----------|--------|--------|--------|--------|
| digits   | 2      | 4      | 6      | 2      |
| Min      | 37     | 2      | 1      | 1      |
| Max      | 412    | 248    | 145    | 429    |
| Mean     | 153.25 | 41.260 | 18.903 | 52.988 |
| Median   | 122    | 27     | 12     | 25     |
| Skewness | 1.189  | 2.487  | 3.043  | 2.705  |
| Kurtosis | 3.422  | 10.457 | 14.192 | 10.701 |

### CSI300
|          | SWIC   |        |        | CSRCIC |
|----------|--------|--------|--------|--------|
| digits   | 2      | 4      | 6      | 2      |
| Min      | 1      | 1      | 1      | 1      |
| Max      | 40     | 32     | 32     | 39     |
| Mean     | 12.074 | 4.528  | 2.885  | 6.653  |
| Median   | 10     | 3      | 2      | 4      |
| Skewness | 1.422  | 3.622  | 5.150  | 2.528  |
| Kurtosis | 4.290  | 18.386 | 33.298 | 9.369  |

### CSI500
|          | SWIC   |       |        | CSRCIC |
|----------|--------|-------|--------|--------|
| digits   | 2      | 4     | 6      | 2      |
| Min      | 3      | 1     | 1      | 1      |
| Max      | 59     | 26    | 22     | 47     |
| Mean     | 19.607 | 5.903 | 3.348  | 8.446  |
| Median   | 19     | 4     | 2      | 5      |
| Skewness | 1.288  | 1.664 | 2.640  | 2.099  |
| Kurtosis | 5.202  | 5.867 | 11.740 | 7.524  |

## Preprocess
**We will report the results in published version**