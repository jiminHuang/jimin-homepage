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

## Reference
[1] Bhojraj, S., & Lee, C. M. C. (2002). Who is my peer? A valuation-based approach to the selection of comparable firms. *Journal of Accounting Research*, *40*(2), 407–439. https://doi.org/10.1111/1475-679X.00054
﻿

[2] 杨朝军, 郭鹏飞, & 焦涛. (2004). 中国上市公司行业分类标准的理论与实证研究. 科学学与科学技术管理, *1*.
﻿

[3] Bhojraj, S., Lee, C. M. C., & Oler, D. (2005). What’s My Line? A Comparison of Industry Classification Schemes for Capital Market Research. *SSRN Electronic Journal*. https://doi.org/10.2139/ssrn.356840
﻿

[4] Boni, L., & Womack, K. L. (2006). Analysts, industries, and price momentum. *Journal of Financial and Quantitative Analysis*, *41*(1), 85–109. https://doi.org/10.1017/S002210900000243X
﻿

[5] Chan, L. K. C., Lakonishok, J., & Swaminathan, B. (2007). Industry classifications and return comovement. *Financial Analysts Journal*, *63*(6), 56–70. https://doi.org/10.2469/faj.v63.n6.4927
﻿

[6] Conover, C. M., Jensen, G. R., Johnson, R. R., & Mercer, J. M. (2008). Sector Rotation and Monetary Conditions. *The Journal of Investing*, *17*(1), 34–46. https://doi.org/10.3905/joi.2008.701955
﻿

[7] Fairfield, P. M., Ramnath, S., & Yohn, T. L. (2009). Do industry-level analyses improve forecasts of financial performance. *Journal of Accounting Research*, *47*(1), 147–178. https://doi.org/10.1111/j.1475-679X.2008.00313.x
﻿

[8] Kadan, O., Madureira, L., Wang, R., & Zach, T. (2010). *Industry Recommendations: Characteristics, Investment Value, and Relation to Firm Recommendations*. *July*, 1–47.
﻿

[9] Charitou, M. (2010). Does industrial financial analysis affect stock returns? International empirical evidence. *Investment Management and Financial Innovations*, *7*(3), 115–124.
﻿

[10] hu, N., Liu, L., Shin, H., & Zhang, J. (2010). Who are your peers?: An empirical investigation of the matched sample comparison analysis. *International Journal of Accounting & Information Management*, *18*(2), 140–155. https://doi.org/10.1108/18347641011048129
﻿

[11] Weiner, C. (2011). The Impact of Industry Classification Schemes on Financial Research. *SSRN Electronic Journal*, 1–48. https://doi.org/10.2139/ssrn.871173
﻿

[12] Erdorf, S., & Heinrichs, N. (2011). Co-movement of revenue: Structural changes in the business cycle. *Financial Markets and Portfolio Management*, *25*(4), 411–433. https://doi.org/10.1007/s11408-011-0168-8
﻿

[13] Lyocsa, S., & Vyrost, T. (2011). Industry Classification: Review, Hurdles and Methodologies. *SSRN Electronic Journal*. https://doi.org/10.2139/ssrn.1480563
﻿

[14] Doeswijk, R., & Vliet, P. van. (2011). Global Tactical Sector Allocation: A Quantitative Approach. *The Journal of Portfolio Management*, *38*(1), 29–47. https://doi.org/10.3905/jpm.2011.38.1.029
﻿

[15] Chou, P. H., Ho, P. H., & Ko, K. C. (2012). Do industries matter in explaining stock returns and asset-pricing anomalies? *Journal of Banking and Finance*, *36*(2), 355–370. https://doi.org/10.1016/j.jbankfin.2011.07.016
﻿

[16] Bustamante, M. C., & Donangelo, A. (2012). Product Market Competition and Industry Returns. *SSRN Electronic Journal*, *510*, 1–68. https://doi.org/10.2139/ssrn.2173985
﻿

[17] Yong, S. L., & Ingham, H. (2012). *The Impact of Different Industrial Classification Schemes on Firm Performance : An IVs Analysis*. *3*(9), 120–132.
﻿

[18] Kadan, O., Madureira, L., Wang, R., & Zach, T. (2012). Analysts’ industry expertise. *Journal of Accounting and Economics*, *54*(2–3), 95–120. https://doi.org/10.1016/j.jacceco.2012.05.002
﻿

[19] Hrazdil, K., & Zhang, R. (2012). The importance of industry classification in estimating concentration ratios. *Economics Letters*, *114*(2), 224–227. https://doi.org/10.1016/j.econlet.2011.10.001
﻿

[20] Hrazdil, K., & Scott, T. (2013). The role of industry classification in estimating discretionary accruals. *Review of Quantitative Finance and Accounting*, *40*(1), 15–39. https://doi.org/10.1007/s11156-011-0268-6
﻿

[21] Kim, K. J., Lee, C., & Tiras, S. L. (2013). The effects of adjusting the residual income model for industry and firm-specific factors when predicting future abnormal returns. *Asia-Pacific Journal of Financial Studies*, *42*(3), 373–402. https://doi.org/10.1111/ajfs.12018
﻿

[22] Hrazdil, K., Trottier, K., & Zhang, R. (2013). A comparison of industry classification schemes: A large sample study. *Economics Letters*, *118*(1), 77–80. https://doi.org/10.1016/j.econlet.2012.09.022
﻿

[23] Gay, S., & Karger, E. (2014). Patent Citations and Stock Performance: Constructing a Dynamic Industry Classification. *SSRN Electronic Journal*, 1–46. https://doi.org/10.2139/ssrn.2496414
﻿

[24] Lamponi, D. (2014). Is industry classification useful to predict U.S. Stock price co-movements? *Journal of Wealth Management*, *17*(1), 71–77. https://doi.org/10.3905/jwm.2014.17.1.071
﻿

[25] Hrazdil, K., Trottier, K., & Zhang, R. (2014). An intra- and inter-industry evaluation of three classification schemes common in capital market research. *Applied Economics*, *46*(17), 2021–2033. https://doi.org/10.1080/00036846.2014.892200
﻿

[26] Dou, P. Y., Gallagher, D. R., Schneider, D., & Walter, T. S. (2014). Cross-region and cross-sector asset allocation with regimes. *Accounting and Finance*, *54*(3), 809–846. https://doi.org/10.1111/acfi.12017
﻿

[27] Chen, C. M., & Chang, Y. F. (2015). Visualizing the clustering of financial networks and profitability of stocks. *Journal of Complex Networks*, *3*(2), 303–318. https://doi.org/10.1093/comnet/cnu019
﻿

[28] Scislaw, K. E. (2015). The value premium within and across GICS industry sectors in a pre-financial collapse sample. *Cogent Economics and Finance*, *3*(1), 1–18. https://doi.org/10.1080/23322039.2015.1045214
﻿

[29] Chong, J., & Phillips, G. M. (2015). Sector Rotation with Macroeconomic Factors. *The Journal of Wealth Management*, *18*(1), 54–68. https://doi.org/10.3905/jwm.2015.18.1.054
﻿

[30] Yaros, J. R., & Imieliński, T. (2015). Data-driven methods for equity similarity prediction. *Quantitative Finance*, *15*(10), 1657–1681. https://doi.org/10.1080/14697688.2015.1071079
﻿

[31] Li, N. (2015). Who Are My Peers? Labor Market Peer Firms Through Employees’ Internet Co-Search Patterns. *Ssrn*, *January 2014*. https://doi.org/10.2139/ssrn.2558271
﻿

[32] Yang, H., Lee, H. J., Cho, S., & Cho, E. (2016). Automatic classification of securities using hierarchical clustering of the 10-Ks. *Proceedings - 2016 IEEE International Conference on Big Data, Big Data 2016*, 3936–3943. https://doi.org/10.1109/BigData.2016.7841069
﻿

[33] Phillips, R. L., & Ormsby, R. (2016). Industry classification schemes: An analysis and review. *Journal of Business and Finance Librarianship*, *21*(1), 1–25. https://doi.org/10.1080/08963568.2015.1110229
﻿

[34] Overgaard Knudsen, J., Kold, S., & Plenborg, T. (2017). Stick to the fundamentals and discover your peers. *Financial Analysts Journal*, *73*(3), 85–105. https://doi.org/10.2469/faj.v73.n3.5
﻿

[35] Hughen, J. C., & Strauss, J. (2017). Portfolio Allocations Using Fundamental Ratios: Are Profitability Measures More Effective in Selecting Firms and Sectors? *The Journal of Portfolio Management*, *43*(3), 87–101. https://doi.org/10.3905/jpm.2017.43.3.087
﻿

[36] Kuo, C. Y. (2017). Is the accuracy of stock value forecasting relevant to industry factors or firm-specific factors? An empirical study of the Ohlson model. *Review of Quantitative Finance and Accounting*, *49*(1), 195–225. https://doi.org/10.1007/s11156-016-0587-8
﻿

[37] Bruzda, J. (2017). Real and complex wavelets in asset classification: An application to the US stock market. *Finance Research Letters*, *21*, 115–125. https://doi.org/10.1016/j.frl.2017.02.004
﻿

[38] Wang, J., Brooks, R., Lu, X., & Holzhauer, H. M. (2017). Sector Momentum. *The Journal of Investing*, *26*(2), 48–60. https://doi.org/10.3905/joi.2017.26.2.048
﻿

[39] Briere, M., & Szafarz, A. (2017). Factors vs. Sectors in Asset Allocation: Stronger Together? *SSRN Electronic Journal*, 1–24. https://doi.org/10.2139/ssrn.2965346
﻿

[40] Chung, D. Y., Hrazdil, K., & Li, X. (2017). The effect of industry classification on analyst following and the properties of their earnings forecasts. *Applied Economics Letters*, *24*(6), 417–421. https://doi.org/10.1080/13504851.2016.1197362
﻿

[41] Kakushadze, Z., & Yu, W. (2017). Open source fundamental industry classification. In *Data* (Vol. 2, Issue 2). https://doi.org/10.3390/data2020020
﻿

[42] Jackson, A. B., Plumlee, M. A., & Rountree, B. R. (2018). Decomposing the market, industry, and firm components of profitability: implications for forecasts of profitability. *Review of Accounting Studies*, *23*(3), 1071–1095. https://doi.org/10.1007/s11142-018-9446-2