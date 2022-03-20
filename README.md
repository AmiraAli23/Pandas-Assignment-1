# A Whale Off the Port(folio)

## Introduction

This assignment required an analysis of several portfolios ; Soros Fund Management, Paulson & Co, Tiger Global Management, Berkshire Hathaway Inc, Algo 1, Algo, 2 and the S&PTSX 60. 

## Process

After importing the csv files and dropping the nulls, I removed  the commas and "$" in the S&P data frame in order to make the data comparable and useable. I also converted the "Close" price column to float otherwise the percentage change function would not have run.

<img width="508" alt="Screen Shot 2022-03-19 at 10 46 32 PM" src="https://user-images.githubusercontent.com/99091066/159145843-3ebd25af-9a09-4db6-bc3b-b51e887604b2.png">

<img width="535" alt="Screen Shot 2022-03-19 at 10 47 59 PM" src="https://user-images.githubusercontent.com/99091066/159145864-13847a8b-3f87-4cae-9b83-580068482610.png">

Afer calculating the daily returns and merging the data frames, I plot the "all data" DF to visualize how each portfolio performed. 

<img width="580" alt="Screen Shot 2022-03-19 at 10 50 14 PM" src="https://user-images.githubusercontent.com/99091066/159145930-30736afc-d12a-4e26-8e16-556bd4077a3a.png">

As seen in the figure above, each portfolio performed relatively similar. Tiger global management had a few extreme points, once in 2017 when they outperformed the portfolios, and once in 2019 when they significantly underperformed compared to their counterparties. 

I calculated the cumulative returns of all portfolios and plot the figure below. Each portfolio seems to move similary with the others. For example each portfolio experienced a rise in 2019-01, after the dramatic dip at the end of 2019. This drop could be attributed to the January affect, that normally isn't as dramatic as it was in 2019 [Source](https://www.cnbc.com/2019/03/26/the-2019-stock-market-comeback-resembles-a-january-effect-on-steroids.html). The January effect is a phenomenon in which stock prices incerease each January because investors are selling their top preformning stocks at the end of the year to realize a capital gain. 
Through this chart, it is evident that Algo 1 outperformed the other portfolios, while Paulson & Co Inc underperformed.

<img width="578" alt="Screen Shot 2022-03-19 at 10 52 55 PM" src="https://user-images.githubusercontent.com/99091066/159145981-c33c1a5d-9ddd-4b51-a6bf-89a24d6b2e93.png">

The box plot below, shows the returns for each portfolio. Assesing it visually, it is clear that Berkshire has the biggest spread, or deviations or returns, compared to S&P TSX or Paulson & Co. This is also confirmed when assesing the standard deviations for each portfolio, Berkshire has the highest deviation at 0.128, while the S&P has 0.0070 and Paulson is 0.0069.

<img width="547" alt="Screen Shot 2022-03-19 at 11 07 59 PM" src="https://user-images.githubusercontent.com/99091066/159146339-7d2e6a8e-bb0e-4f4a-9c7f-bad412c00ca2.png">

<img width="514" alt="Screen Shot 2022-03-19 at 11 16 34 PM" src="https://user-images.githubusercontent.com/99091066/159146527-13c20588-56c6-4a40-a0eb-3404f339d884.png">
<img width="345" alt="Screen Shot 2022-03-19 at 11 17 44 PM" src="https://user-images.githubusercontent.com/99091066/159146543-1d834fd5-17ab-4cd9-9186-32abd4211d97.png">

Through the box plot, standard deviation, and annualized standard deviation calculations it is evident that Berkshire is the riskiest portfolio, and significantly more risky than the S&P. 

Below is the correlation matrix for all of the portfolios compared to the S&P. The portfolio most correlated with the S&P is Algo 2, their standard deviations are similar as well. The portfolio that is least correlated with is Algo 1. Berkshire falls somewhere in between. To mitigate risk, it is important to select stocks that have a lower correlation with each other in order to diversify the portfolio. 

<img width="513" alt="Screen Shot 2022-03-19 at 11 26 07 PM" src="https://user-images.githubusercontent.com/99091066/159146725-9770f242-b5d7-484d-b7b1-3b6c7f31bb4b.png">

The Beta of the sample and is around 0.75. This was calculated by taking the covariance of Soros Fund Management and the S&P, divided by the variance of the S&P. The higher the beta, the more riskier the portoflio is. Generally, a beta more than 1 is considered risky. 
<img width="236" alt="Screen Shot 2022-03-19 at 11 53 59 PM" src="https://user-images.githubusercontent.com/99091066/159147391-d3b07155-10ed-496b-b94c-ea0046e41d0b.png">

Overtime, the Beta or risk has fluctuated. The two were riskiest in 2018-07, in around 2019-03. 

<img width="643" alt="Screen Shot 2022-03-19 at 11 59 52 PM" src="https://user-images.githubusercontent.com/99091066/159147511-48cd24fb-fb66-4e6a-b0a0-f91a77452004.png">

Sharpe Ratios measures performance that is adjusted by risk. The higher the sharpe ratio, the better. Through calculating the ratios, it is clear that Algo 1 has the highest value while Paulson has the lowest. Most portfolios are outperforming the S&P. Based on the graph, Paulson is expected to have negative returns. Algorithmic strategies outperformed all Whale portfolios, as well as the S&P.

<img width="443" alt="Screen Shot 2022-03-20 at 12 48 21 AM" src="https://user-images.githubusercontent.com/99091066/159148670-6ad0e781-dc33-4278-a6a7-21ec42778b1b.png">


## Creating Custom Portolio

