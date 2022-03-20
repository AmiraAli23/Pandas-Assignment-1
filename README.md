# A Whale Off the Port(folio)

## Introduction

The following is a risk/performance analysis of the below portfolios: 

* Soros Fund Management
* Paulson & Co
* Tiger Global Management
* Berkshire Hathaway Inc
* Algo 1
* Algo 2 
* S&PTSX 60

A custom portfolio was also created, and its risk/performance was evaluated against to the others.

### Data Processing

The raw data was sourced from various means, including Google Finance, and can be found [here](https://github.com/AmiraAli23/Pandas-Assignment-1/tree/main/Resources).

The raw data was cleaned to remove commas and dollar signs, ("$"). The "Close" price column was converted to float to allow for mathematical operations, and null values were removed.

<img width="508" alt="Screen Shot 2022-03-19 at 10 46 32 PM" src="https://user-images.githubusercontent.com/99091066/159145843-3ebd25af-9a09-4db6-bc3b-b51e887604b2.png">

<img width="535" alt="Screen Shot 2022-03-19 at 10 47 59 PM" src="https://user-images.githubusercontent.com/99091066/159145864-13847a8b-3f87-4cae-9b83-580068482610.png">


## Evaluation

Afer calculating the daily returns and merging the data frames, the "all data" DF was plotted to visualize the performance of each portfolio:

<img width="580" alt="Screen Shot 2022-03-19 at 10 50 14 PM" src="https://user-images.githubusercontent.com/99091066/159145930-30736afc-d12a-4e26-8e16-556bd4077a3a.png">

As seen in the figure above, each had a fairly similar performance. The data for Tiger Global Management had a few extreme points: once in 2017, when they outperformed the portfolios, and once in 2019 when they significantly underperformed compared to their counterparties. 

The cumulative returns of all portfolios were calculated and plotted in the figure below. Each portfolio seems to move similary as the others. Notably, each portfolio experienced a rise in 2019-01, after the dramatic dip at the end of 2019. This drop could be attributed to the [January effect](https://www.cnbc.com/2019/03/26/the-2019-stock-market-comeback-resembles-a-january-effect-on-steroids.html), which normally isn't as dramatic as it was in 2019. The January effect is a phenomenon that sees a stock prices increase each January due to investors selling their top performing stocks at the end of the year. This is generally done to realize a capital gain. 

Through this chart, it is evident that Algo 1 outperformed the other portfolios, whereas Paulson & Co Inc generally underperformed.

<img width="578" alt="Screen Shot 2022-03-19 at 10 52 55 PM" src="https://user-images.githubusercontent.com/99091066/159145981-c33c1a5d-9ddd-4b51-a6bf-89a24d6b2e93.png">

The box plot below displays the returns for each portfolio. Visually, it is clear that Berkshire has the biggest spread, or deviations of returns, compared to the S&P TSX or Paulson & Co. This is also confirmed when assessing the standard deviations for each portfolio, as Berkshire has the highest deviation at 0.128, while the S&P has 0.0070 and Paulson is 0.0069.

<img width="547" alt="Screen Shot 2022-03-19 at 11 07 59 PM" src="https://user-images.githubusercontent.com/99091066/159146339-7d2e6a8e-bb0e-4f4a-9c7f-bad412c00ca2.png">


<img width="514" alt="Screen Shot 2022-03-19 at 11 16 34 PM" src="https://user-images.githubusercontent.com/99091066/159146527-13c20588-56c6-4a40-a0eb-3404f339d884.png">


<img width="345" alt="Screen Shot 2022-03-19 at 11 17 44 PM" src="https://user-images.githubusercontent.com/99091066/159146543-1d834fd5-17ab-4cd9-9186-32abd4211d97.png">

Through the box plot, standard deviation, and annualized standard deviation calculations, it is evident that Berkshire is the riskiest portfolio, and significantly more risky than the S&P. 

Below is the correlation matrix for all of the portfolios compared to the S&P. The portfolio most correlated with the S&P is Algo 2, and their standard deviations are similar as well. The portfolio that is least correlated with S&P is Algo 1, and Berkshire falls somewhere in between. To mitigate risk, it is important to select stocks that have a lower correlation with each other in order to diversify the portfolio. Therefore, the stocks in Algo would be better paired with the S&P.


<img width="513" alt="Screen Shot 2022-03-19 at 11 26 07 PM" src="https://user-images.githubusercontent.com/99091066/159146725-9770f242-b5d7-484d-b7b1-3b6c7f31bb4b.png">


### Beta

The Beta of the sample and is around 0.75. This was calculated by taking the covariance of Soros Fund Management and the S&P, divided by the variance of the S&P. The higher the beta, the more riskier the portoflio is. Generally, a beta more than 1 is considered risky.

<img width="236" alt="Screen Shot 2022-03-19 at 11 53 59 PM" src="https://user-images.githubusercontent.com/99091066/159147391-d3b07155-10ed-496b-b94c-ea0046e41d0b.png">

Over time, the Beta or risk has fluctuated. The two were riskiest in 2018-07, and around 2019-03. 

<img width="643" alt="Screen Shot 2022-03-19 at 11 59 52 PM" src="https://user-images.githubusercontent.com/99091066/159147511-48cd24fb-fb66-4e6a-b0a0-f91a77452004.png">


### Sharpe Ratios

Sharpe Ratios measure performance that is adjusted by risk, and a higher value indicates a higher return. Upon review, it is clear that Algo 1 has the highest value, while Paulson has the lowest, and most portfolios are outperforming the S&P. Based on the graph below, Paulson is expected to have negative returns. Algorithmic strategies outperformed all Whale portfolios, as well as the S&P.


<img width="443" alt="Screen Shot 2022-03-20 at 12 48 21 AM" src="https://user-images.githubusercontent.com/99091066/159148670-6ad0e781-dc33-4278-a6a7-21ec42778b1b.png">


## Custom Portolio

Before selecting stocks to create a custom portfolio, the first logical step was to calculate the date range in the alldata data frame. This was done by finding the maximum and minimum dates, and its purpose is to ensure that only stocks with data available during the specified time period are considered.

The stocks chosen for the custom portofolio are as follows:

* Ebay
* Amazon
* Nvidia

These stocks are well-established, and contain a wealth of data.

After calculating the weighted returns, this data was merged with the the alldata dataframe to create the completeport (complete portfolio) dataframe, which was used for subsequent analyses.

The standard deviation of the weighted returns fluctuated quite a bit, peaking in January of each year. 

<img width="527" alt="Screen Shot 2022-03-20 at 4 00 15 PM" src="https://user-images.githubusercontent.com/99091066/159183722-1dd6ee08-3060-4122-a2a9-bce4414a97f8.png">

The correlation of all portfolios was calculated, and visualized this using a heatmap. 

The custom portfolio was least correlated with Algo 1, and most correlated with Soros Fund Management. Compared to the S&P, the custom portfolio has a correlation of 0.45. 


<img width="516" alt="Screen Shot 2022-03-20 at 4 07 53 PM" src="https://user-images.githubusercontent.com/99091066/159183963-8d70af7d-2df2-4f25-bfb0-728dac651890.png">

The Beta of the new portfolio is a lot higher than the previous portfolio (0.74994 compared to the new beta of 1.0316). It is clear that adding the custom portfolio generally made the combined portfolio a lot riskier. 


<img width="294" alt="Screen Shot 2022-03-20 at 4 09 59 PM" src="https://user-images.githubusercontent.com/99091066/159184024-48291b62-6abd-4235-b32d-6ad4629b41c5.png">


Comparing the S&P with the custom portfolio, the Beta values seem to be a higher than before. It appears to be generally consistent, with very high peaks in 2018-05.

<img width="533" alt="Screen Shot 2022-03-20 at 4 13 57 PM" src="https://user-images.githubusercontent.com/99091066/159184166-f2852c37-1b52-40da-b698-6a20a2bed48b.png">


Below are the sharpe ratios for all portfolios

<img width="316" alt="Screen Shot 2022-03-20 at 4 14 53 PM" src="https://user-images.githubusercontent.com/99091066/159184200-135de143-ed26-4444-8a07-056837fe5f04.png">

The custom portfolio has a high sharpe ratio, second to Algo 1. Paulson & CO and Tiger Global management both had negative values. Compared to the S&P, all portfolios except the negatives, outperformed.




