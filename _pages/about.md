---
permalink: /
title: "Portfolio"
#excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
## Education
#### General Assembly (_September 2023_)
Certificate of Completion, Data Science Immersive 

##### Western Washington University (_December 2021_)
B.S., Geology


## Data Science Projects
### [Timeseries Forecast of Soil Moisture](https://github.com/DanielGroneberg/Climate_Group_Project) | Python: netCDF4, statsmodels, sktime, sklearn 
![SARIMA Model](/images/Sarima_overall.png)
*Underfit SARIMA model trained with incorrect stationarity assumption, later replaced with better-performing model.*

Used **Python** to forecast soil moisture in the United States using 64 years of climate data. Extracted 50 years of .nc data with **netCDF4** and constructed a datetime index using encoded day count data. Applied Augmented Dickey–Fuller test to check for seasonality. Observed distinct shift from stationary soil moisture to decreasing moisture over time around year 2010. This shift took place close to original 80/20 train/test split resulting in an assessment of data as stationary overall which did not hold for test set and subsequent overestimation of soil moisture in the test set. SARIMA and Holt-Winters models both performed poorly with a best R2 score of .42. Applying Holt-Winters additive seasonality model did not see an improvment in performance. Forecasting using only section of data with downward trend (after 2010) resulted in much improved best R2 score of .76


### [Timeseries Forecast of Federal Reserve Interest Rates](https://github.com/DanielGroneberg/DSI-Project-5) | Python: BeautifulSoup, NLTK, statsmodels, sklearn
![Economic Metrics](/images/plots.png)
*Economic metrics used to develop vector autoregression including sentiment feature engineered from scaped Beige Book reports.*

Developed a timeseries forecast for key economic metrics including Federal Reserve interest rates using **Python**. Scraped 50 years of [Federal Reserve Beige Book transcripts](https://www.minneapolisfed.org/region-and-community/regional-economic-indicators/beige-book-archive) using **BeautifulSoup** and applied natural language processing to engineer sentiment feature from text data. Used a Vector Autoregression model to forecast interest rates.


### [Predicting Subreddit from Sample Post](https://github.com/DanielGroneberg/project-3) | Python: NLTK, spacy, sklearn
![Economic Metrics](/images/sentiment_distribution_by_sub.png)
*Distribution of sentiment across posts from the two subreddits examined: r/Jobs and r/AntiWork

Developed a subreddit classification model using 7,155 posts scraped from r/Jobs and r/AntiWork. Examined how sentiment varried between the two subreddits when certain words like "manager" or "interview" were found in a post. Token vectorized the text data and experimented with logistic regression, kNN, random forest and gradient boosted models.

Best performing model was a stacking classifier model using logistic regression and random forest classifier base estimators with a gradient boosting classifier as the final estimator, which achieved a classification accuracy score of .85.
