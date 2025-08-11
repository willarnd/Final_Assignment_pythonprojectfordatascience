# Tesla & GameStop Stock and Revenue Analysis

This project is part of the IBM Data Analyst Professional Certificate (Final Assignment).  
It involves extracting stock price data and revenue data for **Tesla (TSLA)** and **GameStop (GME)**, then visualizing the data using Python.

## Project Steps

### Question 1: Extract Tesla Stock Data
- Used `yfinance` to create a Ticker object for Tesla (TSLA).
- Extracted historical stock data (`period="max"`).
- Reset the index and displayed the first five rows.

### Question 2: Extract Tesla Revenue Data
- Used `requests` to scrape the Tesla revenue page.
- Parsed HTML using `BeautifulSoup`.
- Extracted the Tesla Quarterly Revenue table into a DataFrame (`tesla_revenue`).
- Cleaned data by removing `$` and `,` and dropping null values.

### Question 3: Extract GameStop Stock Data
- Used `yfinance` to create a Ticker object for GameStop (GME).
- Extracted historical stock data (`period="max"`).
- Reset the index and displayed the first five rows.

### Question 4: Extract GameStop Revenue Data
- Used `requests` to scrape the GameStop revenue page.
- Parsed HTML using `BeautifulSoup`.
- Extracted the GameStop Quarterly Revenue table into a DataFrame (`gme_revenue`).
- Cleaned data by removing `$` and `,` and dropping null values.

### Question 5 & 6: Create Dashboards
Used the `make_graph` function to plot:

#### Tesla Stock Data and Revenue
![Tesla Stock Graph](Grafik%20tesla.png)

#### GameStop Stock Data and Revenue
![GameStop Stock Graph](Grafik%20Gamestop.png)

## Requirements
To run this project, install the following Python libraries:
```bash
pip install yfinance requests beautifulsoup4 html5lib pandas plotly
```

## How to Run
1. Open the Jupyter Notebook.
2. Run each cell in sequence from Question 1 to Question 7.
3. The graphs will be displayed inline in the notebook.
4. Final graphs are saved as `Grafik tesla.png` and `Grafik Gamestop.png`.

## Output Summary
- **Tesla**: Stock price shows rapid growth after 2019, while revenue also trends upward.
- **GameStop**: Stock price exhibits a spike in early 2021 (short squeeze), revenue relatively stable but fluctuating seasonally.

## 📂 Files in This Repository

- `Final Assignment-v2.ipynb` → Jupyter Notebook containing all code and explanations.
- `Grafik tesla.png` → Tesla stock and revenue visualization.
- `Grafik Gamestop.png` → GameStop stock and revenue visualization.
- `README.md` → Project documentation.

---
**Author:** IBM Data Analyst Capstone Project  
**Tools Used:** Python, Jupyter Notebook, yfinance, BeautifulSoup, pandas, plotly
