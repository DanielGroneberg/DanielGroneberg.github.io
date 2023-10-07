---
permalink: /
#excerpt: ""
author_profile: true
redirect_from: 
  - /#about/
  - /about.html
  - /about/
---
<div id="about"></div>
<!-- {#about} -->
&zwnj;
&zwnj;
My introduction to the data science process was as an undergraduate at Western Washington University where I modeled hillslope safety, precipitation estimates and river channel geometry using ArcGIS and Python. I also learned how to merge and modify dataframes and manage geodatabases. In a customer-facing role as a Geotechnical Field Technician with Earth Solutions, NW, I assisted construction site contractors in meeting targets by providing immediate feedback and recommendations based on data I collected onsite in order to achieve 95% soil compaction targets. In this role, I drafted daily technical reports summarizing my findings, mapping my data, and presenting it in spreadsheet format. This enabled me to serve as an intermediary between offsite technical experts and the client. I graduated from the General Assembly Data Science program, where I used Python for data analysis and modeling.
<div id="projects"></div>
<!-- {projects} -->
&nbsp;
### [Timeseries Forecast of Soil Moisture](https://github.com/DanielGroneberg/Climate_Group_Project) | Python: netCDF4, statsmodels, sktime, sklearn 
![SARIMA Model](/images/Sarima_overall.png)
*Underfit SARIMA model trained with incorrect stationarity assumption, later replaced with better-performing model.*

Used **Python** to forecast soil moisture in the United States. Extracted 64 years of .nc data with **netCDF4** and constructed a datetime index using encoded day count data. Applied Augmented Dickey–Fuller test to check for seasonality. Observed distinct shift from stationary soil moisture to decreasing moisture over time around year 2010. This shift took place close to original 80/20 train/test split resulting in an assessment of data as stationary overall which did not hold for test set and subsequent overestimation of soil moisture in the test set. SARIMA and Holt-Winters models both performed poorly with a best R2 score of .42. Applying Holt-Winters additive seasonality model did not see an improvement in performance. Forecasting using only section of data with downward trend (after 2010) resulted in much improved best R2 score of .76

### [Timeseries Forecast of Federal Reserve Interest Rates](https://github.com/DanielGroneberg/DSI-Project-5) | Python: BeautifulSoup, NLTK, statsmodels, sklearn
![Economic Metrics](/images/plots.png)
*Economic metrics used to develop vector autoregression including sentiment feature engineered from scraped Beige Book reports.*

Developed a timeseries forecast for key economic metrics including Federal Reserve interest rates using **Python**. Scraped 50 years of [Federal Reserve Beige Book transcripts](https://www.minneapolisfed.org/region-and-community/regional-economic-indicators/beige-book-archive) using **BeautifulSoup** and applied natural language processing to engineer sentiment feature from text data. Used a Vector Autoregression model to forecast interest rates.

### [Predicting Subreddit from Sample Post](https://github.com/DanielGroneberg/Predicting-Subreddit-from-Sample-Post) | Python: NLTK, spacy, sklearn
![Economic Metrics](/images/sentiment_distribution_by_sub.png)
*Distribution of sentiment across posts from the two subreddits examined: r/Jobs and r/AntiWork*

Developed a subreddit classification model using 7,155 posts scraped from r/Jobs and r/AntiWork. Examined how sentiment varied between the two subreddits when certain words like "manager" or "interview" were found in a post. Token vectorized the text data and experimented with logistic regression, kNN, random forest, and gradient-boosted models.

Best performing model was a stacking classifier model using logistic regressor and random forest classifier as the base estimators with a gradient-boosting classifier as the final estimator, which achieved a classification accuracy score of .85.
<div id="resume"></div>
<!-- {#resume} -->
&nbsp;
<object data="{{ site.url }}{{ site.baseurl }}/files/daniel_groneberg_dsi_resume_template.pdf" width="1000" height="1000" type="application/pdf"></object>
