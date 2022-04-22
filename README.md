<p align="center">
  <img src="https://user-images.githubusercontent.com/65748007/164231809-0d7736b6-e71c-4d8f-9f19-6d4b61ca0821.png" alt="Project Cover"/>
</p>

#### 📌 Purpose
<p align="center">
  This project aims to effectively mitigate the violatility of cryptocurrency investment with machine learning models.
</p>

---

<br/>

#### 🧭 Table of Contents
1. [Data Curation & Preparation](./data/README.md)
2. [Evaluation of Model Performance](./metrics/README.md)
---

<br/>

#### 🛠️ Installation

- [pip](https://pip.pypa.io/en/stable/)

  ```
  $ pip install -r requirements.txt
  ```

---

<br/>

#### 📑 Data Sources
- Financial Data - <a href="https://sg.finance.yahoo.com/cryptocurrencies/" target="_blank">Yahoo Finance</a> / <a href="https://pypi.org/project/yfinance/" target="_blank">yfinance</a>
- Search Trends Data - <a href="https://trends.google.com/trends/?geo=SG" target="_blank">Google Trends</a> / <a href="https://pypi.org/project/pytrends/" target="_blank">pytrends</a>


---

<br/>

####  🔍 Algorithms & Machine Learning Models
- Rolling-Forecast ARIMA
- XGBRegressor
- LSTM


---

<br/>

####  🧰 Languages & Tools
- Languages <br/>
  <img alt="Python" src="https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue" height="25"/>


- Libraries, Packages <br/>
  <img alt="Numpy" src="https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white" height="25"/>
  <img alt="Pandas" src="https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white" height="25"/>
  <img alt="Scikit Learn" src="https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" height="25"/>
  <img alt="TensorFlow" src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=TensorFlow&logoColor=white" height="25"/>
  <img alt="Plotly" src="https://img.shields.io/badge/Plotly-239120?style=for-the-badge&logo=plotly&logoColor=white" height="25"/>

- Tools, IDE <br/>
  <img alt="Github" src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" height="25"/>
  <img alt="Jupyter" src="https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white" height="25"/>
  <img alt="Google Colab" src="https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252" height="25"/>

---

<br/>

####  📚 Notebooks Overview 

*Each notebook is prefixed with the chronological order of the analysis pipeline and can be executed as a standalone.*
<br/>

> [0_DataScraper.ipynb](./0_DataScraper.ipynb)

  - Retrieves stock information on <a href="https://sg.finance.yahoo.com/quote/BTC-USD/" target="_blank">Bitcoin (BTC-USD)</a> from <a href="https://sg.finance.yahoo.com/cryptocurrencies/" target="_blank">Yahoo Finance</a>

  - Annual archive of <a href="https://trends.google.com/trends/?geo=SG" target="_blank">Google Search Trends</a> using the <a href="https://pypi.org/project/pytrends/" target="_blank">pytrends</a> package 

  - Generate and export [BTC-SearchTrend.csv](./data/BTC-SearchTrend.csv) from the successful merger of above-mentioned datasets


> [1_DataAnalysis.ipynb](./1_DataAnalysis.ipynb)

  - Displays dataset overview and checks for any null values

  - Exploratory data analysis on the [BTC-SearchTrend.csv](./data/BTC-SearchTrend.csv) dataset


> [2_UnivariateForecast.ipynb](./2_UnivariateForecast.ipynb)

  - Utilises one stock ticker variable [(OPEN / CLOSE / HIGH / LOW)](./data/README.md) as the model data

  - Initialise, train and prediction <a href="https://sg.finance.yahoo.com/quote/BTC-USD/" target="_blank">Bitcoin (BTC-USD)</a> valuation with the following machine learning model(s):
    - Rolling-Forecast ARIMA
    - XGBRegressor
    - LSTM

  - Summarises and compares the performance of all previously ran models

> [3_MultivariateForecast.ipynb](./3_MultivariateForecast.ipynb)

  - Utilises entire [BTC-SearchTrend.csv](./data/BTC-SearchTrend.csv) dataset as the model data

  - Initialise, train and prediction <a href="https://sg.finance.yahoo.com/quote/BTC-USD/" target="_blank">Bitcoin (BTC-USD)</a> valuation with the following machine learning model(s):
    - LSTM

  - Summarises and compares the performance of all previously ran models

---

<br/>

####  👥 Contributors 

<a href="https://github.com/crystalcheong" target="_blank">Crystal Cheong</a><br/>

- Scraped data in [0_DataScraper.ipynb](./0_DataScraper.ipynb)
- Contributed to sections in [1_DataAnalysis.ipynb](./1_DataAnalysis.ipynb)
  - Daily Percentage Change
  - Scaled Time-Series Visualiation
  - Scaled Data Correlation
- Models in [2_UnivariateForecast.ipynb](./2_UnivariateForecast.ipynb), [3_MultivariateForecast.ipynb](./3_MultivariateForecast.ipynb)
  - Rolling-Forecast ARIMA
  - XGBRegressor
  - LSTM

<a href="https://github.com/AmosChong20" target="_blank">Yue Hong</a><br/>
- Contributed to Exploratory Data Analysis part (Visualisation)
- Presentation Slides

<a href="https://github.com/Jared7333" target="_blank">Jared Chan</a><br/>
- Script
