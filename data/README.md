<h3 align="center">
  Data Curation & Preparation
</h3>

---

#### 📌 Requirements
- [x] Availability of historical & latest data
- [x] From credible and reliable source
- [x] Contains relevant variables for manipulation

---
<p align="center">
  <img src="https://user-images.githubusercontent.com/65748007/164248322-c5ee7471-9536-4f83-916a-4534df42df1d.png" alt="Data Curation and Preparation"/>
</p>

#### 📑 More About Data Sources
- Financial Data - <a href="https://sg.finance.yahoo.com/cryptocurrencies/" target="_blank">Yahoo Finance</a> / <a href="https://pypi.org/project/yfinance/" target="_blank">yfinance</a>

   *Scraped from **yfinance** - a Python library that fetches current and historical stock market price data from Yahoo Finance, and so much more.*

    > [BTC-SearchTrend.csv](./BTC-SearchTrend.csv)

    COLUMN | DESCRIPTION | TYPE
    :------------ | :-------------| :-------------| 
    DATE| shown in YYYY-MM-DD format | DatetimeIndex
    OPEN | the price at the market start | float64
    CLOSE | the last price of the day | float64
    HIGH| the highest price on that day | float64
    LOW | the lowest price on that day | float64
    VOLUME | the number of shares traded | int64
    BITCOIN | daily mean search percentile index for term 'bitcoin' | int64
    CRYPTOCURRENCY | daily mean search percentile index for term 'cryptocurrency' | int64

<br/>

- Search Trends Data - <a href="https://trends.google.com/trends/?geo=SG" target="_blank">Google Trends</a> / <a href="https://pypi.org/project/pytrends/" target="_blank">pytrends</a>

    ***Pytrends** is an unofficial Google Trends API that provides different methods to download reports of trending results from google trends.*

    > [trend-2017_2021.csv](./searchTrends/trend-2017_2021.csv)

    COLUMN | DESCRIPTION | TYPE
    :------------ | :-------------| :-------------| 
    dtime | shown in YYYY-MM-DD HH:MM:SS format | datetime64[ns]
    bitcoin | search percentile index for term 'bitcoin' | int64
    cryptocurrency | search percentile index for term 'cryptocurrency' | int64
    isPartial | true if the data point is complete for that particular date | int64

---

<br/>

#### 🔬 Data Preparation

> [trend-2017_2021.csv](./searchTrends/trend-2017_2021.csv)

- To conform to time-series data formats, we pivoted the data to split the `dtime` into separate columns of `date` and `time`

- Generated **daily average search percentile** from the mean of grouped hourly entries by `date`
    - .groupby(['Date']) = perform the equivalent of SQL’s GROUP BY operation
    - .mean() = aggregate function to find the average

<br/>

> [BTC-SearchTrend.csv](./BTC-SearchTrend.csv)

- By-product of the *inner join* merger with [trend-2017_2021.csv](./searchTrends/trend-2017_2021.csv) using the `DATE` value
    - .merge() = merge/join datasets

<br/>

<p align="center">
  <img src="https://user-images.githubusercontent.com/65748007/164257496-417e6cf7-cea2-4f4b-b8ae-2e7f53a7e998.png" alt="BTC-SearchTrend dataset preview"/>
</p>

<p align="center">
    Dataframe preview of <a href="./BTC-SearchTrend.csv" target="_blank">BTC-SearchTrend.csv</a>
</p>

---
