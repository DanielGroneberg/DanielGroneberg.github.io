---
permalink: /
title: "About me"
#excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
## Education

-Data Science Immersive | General Assembly (_September 2023_)**
-B.S., Geology	| Western Washington University (_December 2021_)**
--------
## Data Science Projects
### [Timeseries Forecast of Soil Moisture](https://github.com/DanielGroneberg/Climate_Group_Project) | Python: netCDF4, statsmodels, sktime, sklearn 
![SARIMA Model](/images/Sarima_overall.png)
*Underfit SARIMA model trained with incorrect stationarity assumption, later replaced with better-performing model.*

Used **Python** to forecast soil moisture in the United States using 64 years of climate data. Extracted 50 years of .nc data with ***netCDF4** and constructed a datetime index using encoded day count data. Applied Augmented Dickey–Fuller test to check for seasonality. Observed distinct shift from stationary soil moisture to decreasing moisture over time around year 2010. This shift took place close to original 80/20 train/test split resulting in an assesment of data as stationary overall which did not hold for test set and subsequent overestimation of soil moisture in the test set. SARIMA and Holt-Winters models both performed poorly with a best R2 score of .42. Applying Holt-Winters additive seasonality model did not see an improvment in performance. Forecasting using only section of data with downward trend (after 2010) resulted in much improved best R2 score of .76


### [Timeseries Forecast of Federal Reserve Interest Rates](https://github.com/DanielGroneberg/DSI-Project-5) | Python: BeautifulSoup, NLTK, statsmodels, sklearn
![Economic Metrics](/images/plots.png)
*Economic metrics used to develop vector autoregression including sentiment feature engineered from scaped Beige Book reports.*

Developed a timeseries forecast for key economic metrics including Federal Reserve interest rates using **Python**. Scraped 50 years of [Federal Reserve Beige Book transcripts](https://www.minneapolisfed.org/region-and-community/regional-economic-indicators/beige-book-archive) using **BeautifulSoup** and applied natural language processing to engineer sentiment feature from text data. Used a Vector Autoregression model to forecast interest rates.

### [Predicting Subreddit from Sample Post](https://github.com/DanielGroneberg/project-3) | Python: NLTK, spacy, sklearn
![Economic Metrics](/images/sentiment_distribution_by_sub.png)

-----------
## Work Experience
**Bike Delivery Driver at Jimmy Johns (_January 2023 - June 2023_)**
-	Assisted customers in understanding the menu, received orders over the phone and face-to-face.
-	Consistently exceeded 30-minute delivery time goals.
-	Developed and rode efficient delivery routes tailored for each batch of orders while under time pressure.
-	Updated routes in real time if new construction or traffic conditions encountered.
-	Communicated with coworkers to make routes as efficient as possible.

**Stagehand with IATSE Local 15 (_September 2022 - June 2023_)**
- Built video walls, installed lighting fixtures, and followed instructions from a variety of teams.
-	Worked efficiently in teams in order to meet road crew deadline requirements.

**Geotechnical Field Technician at Earth Solutions, NW (_July 2022 - September 2022_)**
- Oversaw trench backfill and provided immediate recommendations to meet 95% soil compaction targets.
-	Collected data and drafted daily technical reports outlining findings.
-	Communicated with technical and non-technical audiences including project geologist and site foreman.
