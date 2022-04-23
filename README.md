### SC1015 Data Science Project — *Crypto-Genie*

> This project aims to effectively mitigate the violatility of cryptocurrency investment by evaluating the media hype from <a href="https://trends.google.com/trends/?geo=SG" target="_blank">Google Trends</a> in our prediction models.

<br/>

<p align="center">
  <img src="https://user-images.githubusercontent.com/65748007/164874137-06790bfc-6efe-4bd2-82df-29632665f7a3.png" alt="Project Cover"/>
</p>

---

#### 🛠️ Installation and Set Up

  - Clone repository
    ```
    git clone https://github.com/crystalcheong/crypto-genie.git
    ```

  - Install dependencies with [pip](https://pip.pypa.io/en/stable/)
    ```
    $ pip install -r requirements.txt
    ```

---

<details>
<summary>📂 Project Structure</summary>
<br/>
  
```
📦crypto-genie
 ┣ 📂data
 ┃ ┣ 📂searchTrends
 ┃ ┣ 📜BTC-SearchTrend.csv
 ┃ ┗ 📜README.md
 ┣ 📂metrics
 ┃ ┣ 📜README.md
 ┣ 📂models
 ┣ 📜0_DataScraper.ipynb
 ┣ 📜1_DataAnalysis.ipynb
 ┣ 📜2_UnivariateForecast.ipynb
 ┣ 📜3_MultivariateForecast.ipynb
 ┣ 📜README.md
 ┗ 📜requirements.txt
 ```


 [`/data`](./data) - stores all the collected data to be utilized <br/>
 [`/metrics`](./metrics) - contains the exported measurement of accuracy & efficacy<br/> 
 [`/models`](./models) - contains the exported pre-trained models<br/>

 </details>

---

#### 📑 Data Sources
- Financial Data - <a href="https://sg.finance.yahoo.com/cryptocurrencies/" target="_blank">Yahoo Finance</a> / <a href="https://pypi.org/project/yfinance/" target="_blank">yfinance</a>
- Search Trends Data - <a href="https://trends.google.com/trends/?geo=SG" target="_blank">Google Trends</a> / <a href="https://pypi.org/project/pytrends/" target="_blank">pytrends</a>


---

#### 🧭 In-depth Documentation
- [Data Curation & Preparation](./data/README.md)
- [Evaluation of Model Performance](./metrics/README.md)

---

<details>
<summary>📚 Notebooks Overview</summary>
<br/>
  
*Each notebook is prefixed with the chronological order of the analysis pipeline and can be executed as a standalone.*
<br/>

- [Data Scraper](./0_DataScraper.ipynb)

  > - Retrieves stock information on <a href="https://sg.finance.yahoo.com/quote/BTC-USD/" target="_blank">Bitcoin (BTC-USD)</a> from <a href="https://sg.finance.yahoo.com/cryptocurrencies/" target="_blank">Yahoo Finance</a>
  > - Annual archive of <a href="https://trends.google.com/trends/?geo=SG" target="_blank">Google Search Trends</a> using the <a href="https://pypi.org/project/pytrends/" target="_blank">pytrends</a> package 
  > - Generate and export [BTC-SearchTrend.csv](./data/BTC-SearchTrend.csv) from the successful merger of above-mentioned datasets

- [Data Analysis](./1_DataAnalysis.ipynb)

  > - Displays dataset overview and checks for any null values
  > - Exploratory data analysis on the [BTC-SearchTrend.csv](./data/BTC-SearchTrend.csv) dataset

- [Univariate Forecast](./2_UnivariateForecast.ipynb)

  > - Utilises **one** stock ticker variable [(OPEN / CLOSE / HIGH / LOW)](./data/README.md) as the model data
  > - Initialise, train and predict <a href="https://sg.finance.yahoo.com/quote/BTC-USD/" target="_blank">Bitcoin (BTC-USD)</a> valuation with the following machine learning model(s):
  >   - Rolling-Forecast ARIMA
  >   - XGBRegressor
  >   - LSTM
  > - Summarises and compares the performance of all previously ran models

- [Multivariate Forecast](./3_MultivariateForecast.ipynb)

  > - Utilises **all** stock ticker and search trend variables as the model data
  > - Initialise, train and predict <a href="https://sg.finance.yahoo.com/quote/BTC-USD/" target="_blank">Bitcoin (BTC-USD)</a> valuation with the following machine learning model(s):
  >   - LSTM
  > - Summarises and compares the performance of all previously ran models

</details>

---
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

#### Contributors ✨

<table>
  <tr>
    <td align="center"><a href="https://github.com/crystalcheong"  target="_blank"><img src="https://avatars.githubusercontent.com/u/65748007?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Crystal Cheong</b></sub></a><br /></td>
    <td align="center"><a href="https://github.com/AmosChong20" target="_blank"><img src="https://avatars.githubusercontent.com/u/95435362?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Yue Chong</b></sub></a><br /></td>
    <td align="center"><a href="https://github.com/Jared7333" target="_blank"><img src="https://avatars.githubusercontent.com/u/104131548?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Jared Chan</b></sub></a><br /></td>
  </tr>
  <tr>
    <td>
      <li>Data Collection & Preparation</li>
      <li>Data Analysis</li>
      <li>Machine Learning</li>
      <li>Repository Documentation</li>
      <li>Presentation Slides & Script</li>
    </td>
    <td>
      <li>Data Analysis</li>
      <li>Data Visualisations</li>
      <li>Presentation Slides & Script</li>
      <li>Video Presenter</li>
    </td>
      <td>
      <li>Machine Learning</li>
      <li>Presentation Slides & Script</li>
      <li>Video Presenter</li>
    </td>
  </tr>
</table>

---

*This repository is submitted as a project work for Nanyang Technological University's [SC1015- Data Science and Aritificial Intelligence course](https://www.ntu.edu.sg/docs/librariesprovider124/economics-and-data-science/sc1015-introduction-to-data-science-ai.pdf?Status=Master&sfvrsn=b6e8f226_4).*

