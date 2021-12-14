---
title: Can Macroeconomic Variables Predict the Stock Market?
subtitle: An empirical evidence from Chinese Stock Market and Machine Learning Methods
date: 2021-07-08T11:20:34.033Z
draft: false
featured: true
authors:
  - admin
  - Min Peng
  - Yanzhao Lai
tags:
  - Computational Finance
categories: []
projects:
  - the-prediction-and-explanation-of-asset-prices
image:
  filename: ""
  focal_point: Smart
  preview_only: false
  alt_text: ""
---
## Introduction
Compared with individual stocks, indices of the stock market generally are less volatile and considered as the representative of the stock market, since they are the aggregation of multiple stocks from different sectors. Thus stock market indices can reveal the overall movement of the stock market and also the current state of the economy.

Therefore, instead of predicting the price of the stock, there are researches focusing on forecasting the stock market index. Although there were different methods applied in this area to predict the movement of the index, the major difference between these methods is the feature set as the input of these methods. Generally, they can be divided into two groups: Firstly, there were researches that considered only the original time series data of the index, and secondly, efforts that incorporated various other data, such as technical factors, social media feeds, news, and especially macroeconomic variables.

So why do Micro Economic Variables matter? From the first effort of Fama, there were a large number of studies have found that the stock return is autocorrelated. Yet the time-varying risk premia are not sufficiently large to explain it unless we take the business cycle into consideration. Thus there were also studies contributing to evaluating the links between macroeconomic variables and the stock market returns. Their work shows a strong correlation between stock market returns and macroeconomic variables in in-sample data. However, an investor cannot make investment decisions with unseen data. Hereby the predictive power of macroeconomic variables is more essential and applicable.

In this post, we investigate the predictive power via an out-of-sample approach, and our work can be distinguished by two contributions in out-of-sample stock market price prediction: 1) We adopt 44 macroeconomic variables whose correlations with stock market price are already evaluated in economic approaches, which can extend the research of macroeconomic variables in prediction, and 2) we perform out-of-sample recursive prediction in Chinese stock market based on three indices: SSE Composite Index, CSI 300 Index, and CSI 500 Index. For the prediction target, we compare the performance in the monthly log return of the index, along with the monthly price trend. We adopt out-of-sample R-square to test the predictive power on monthly log return, and weighted F1 score on the monthly price trend. We also compared a series of ML methods for regression and classification.
The empirical evidence from out-of-sample forecasting regressions is not encouraging for a 'kitchen sink' method which includes all macroeconomic variables, neither nor any 'single factor' methods. However, when forecasting the monthly trend of indices, the method with macroeconomic variables presents an expressive result in the F1 score. It clearly shows that macroeconomic variables embed fundamental information of the circle of the stock market.

##  Related Work
The forecasting of the stock market has attracted more and more attention these years. The first effort dates back to 1965 when Fama et al. [1] gives a fundamental hypothesis called Efficient Market Hypothesis (EMH), which assumes that the financial market is efficient. Although the hypothesis itself implies that there is no consistent excess return for technical analysis or fundamental analysis, recent studies [2-3] provided evidence contrary to the EMH. Therefore, researchers first introduced linear methods into this area, such as autoregressive integrated moving average (ARIMA) [4] and generalized autoregressive conditional heteroskedasticity (GARCH) [5]. Afterward, machine learning methods such as Logistic regression and support vector machines were also incorporated to solve the predicting problems [6]. Recently, with the development of deep learning methods, it was not only the academic but also asset management companies and investment banks that applied deep learning methods to increase the predictive power in the stock market[7-10].
However, previous work generally considered market data such as previous price or volume. Since most of the macroeconomic variables are published monthly or quarterly, previous studies focusing on daily or intraday prediction cannot utilize the information embedded. Yet the correlation between macroeconomic variables and the stock market has been supported by a series of research efforts. Ahmed et al. revealed the causal connections between stock prices and macroeconomic variables in India [11]. Asgharian et al. showed that the dependencies of long-run stock and bond volatility along with stock-bond correlation on macroeconomic uncertainty [12].  Barakat et al. utilized data from Tunisia and Egypt to examine the relationship between the stock market and macroeconomic factors [13]. They found that CPI, exchange rate, money supply, and interest rate were co-integrated with the stock market.  Massacci et al. quantified the links between firms' tail risk and economic environment [14]. Giri et al. examined the long-run and short-run relationship between stock price and macroeconomic variables in India [15]. Megaravalli et al. further extended the research to India, China, and Japanese stock markets [16]. Liu et al. showed that the growth of industries and M2 can significantly influent the stock return in the Chinese stock market [17]. Wen et al. studied the correlations between macroeconomic variables and industry profits [18]. Mao et al. found that there is a direct influence of macroeconomic shocks on the stock market [19]. Guan et al. suggested a consistent long-run positive correlation between nominal GDP and the index [20]. Maio et al. showed that economic activity plays an important role in explaining momentum-based anomalies [21]. González, et al. analyzed the determinants of macroeconomic variables on the stock market betas [22]. Si, et al. proposed that in recession periods business cycle tends to lead the stock market [23].

There were also several studies that utilized the macroeconomic variables. Welch, et al. reported that macroeconomic variables are only predicted well in an in-sample regression [24]. Yet, Weng et al. reported a contrary result that the macroeconomic indicators alone can predict the monthly closing price of U.S. indices [25]. Jiang et al. proposed a stacking method with an ensemble model and deep learning methods, based on historical prices and macroeconomic variables [26]. Hoseinzade et al. proposed CNNpred which incorporates historical prices, technical indicators, and macroeconomic variables to predict U.S index trends [27]. However, existing methods generally predict daily index returns or trends with the fixed horizon, which means their methods will predict the return or trend of the index between day t and day t+h at day t. There were no efforts to examine the predictive power of macroeconomic variables on monthly returns or trends of the stock market. Moreover, researches in the Chinese stock market integrated both historical prices and macroeconomic variables. There was no evidence for the fundamental question in predicting the Chinese stock market via macroeconomic variables: Can Macroeconomic Variables Predict the Stock Market?

## Data
In this section, we describe our data which consists of two major parts: the predicted objective and the features.

First, for the predicted objective, the monthly log return:

LNR = log(P_{t+1}) - log(P_{t})LNR=log(P t+1)−log(P t)

Prices: The index monthly prices from 2007-01-01 to 2020-12-31 are from CSMAR database. These are the last close price for the month.

For the monthly price trend:

TR = \frac{sign(LNR) + 1}{2}TR= 2 sign(LNR)+1
​
 
the trend of the index will be 1 if the log return is greater than 0, otherwise 0.
As for the features, we adopt 44 macroeconomic variables which can be grouped into several categories:

- Economic growth: the retail sales of national social consumer goods, the export and import, fixed assets investment(Manufactory, Real estate, and Infrastructure), growth of industries, M1 and M2, and credit.
- Inflation: CPI, PPI, the exchange rate, and commodities(Oil)
- Liquidity: SHIBOR, DR001, DR007, and the currency supply

Data is all collected from the Tonghuashun financial database. In each prediction subperiod, we normalize the features.

Finally, we compare the following ML methods:

- OLS
- ElasticNet
- RandomForest
- LightGBM
- xgboost
- ANN

For each method, we adopt time-series cross-validation first to tune the method in the training period and apply the tuned method to predict the next month's objective. We set the first 72 months as a training period, and recursively rolling the other months for prediction. After we finished the prediction in the month, we immediately append the month data to the training period for next month's prediction. Thus the length of the training period in the first prediction month is 72 and the last month is 82.

**We will report our result in the published version**
