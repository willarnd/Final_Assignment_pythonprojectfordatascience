# Tesla & GameStop Stock and Revenue Analysis

This project is part of the IBM Data Analyst Professional Certificate (Final Assignment).  
It involves extracting stock price data and revenue data for **Tesla (TSLA)** and **GameStop (GME)**, then visualizing the data using Python.

## Project Steps

### Question 1: Extract Tesla Stock Data
- Used `yfinance` to create a Ticker object for Tesla (TSLA).
- Extracted historical stock data (`period="max"`).
- Reset the index and displayed the first five rows.
  ### Q1 — Tesla Stock Data (First 5 Rows)

| Date                       | Open     | High     | Low      | Close    | Volume     | Dividends | Stock Splits |
|----------------------------|----------|----------|----------|----------|------------|-----------|--------------|
| 2010-06-29 00:00:00-04:00  | 1.266667 | 1.666667 | 1.169333 | 1.592667 | 281494500  | 0.0       | 0.0          |
| 2010-06-30 00:00:00-04:00  | 1.719333 | 2.028000 | 1.553333 | 1.588667 | 257806500  | 0.0       | 0.0          |
| 2010-07-01 00:00:00-04:00  | 1.666667 | 1.728000 | 1.351333 | 1.464000 | 123282000  | 0.0       | 0.0          |
| 2010-07-02 00:00:00-04:00  | 1.533333 | 1.540000 | 1.247333 | 1.280000 | 77097000   | 0.0       | 0.0          |
| 2010-07-06 00:00:00-04:00  | 1.333333 | 1.333333 | 1.055333 | 1.074000 | 103003500  | 0.0       | 0.0          |


### Question 2: Extract Tesla Revenue Data
- Used `requests` to scrape the Tesla revenue page.
- Parsed HTML using `BeautifulSoup`.
- Extracted the Tesla Quarterly Revenue table into a DataFrame (`tesla_revenue`).
- Cleaned data by removing `$` and `,` and dropping null values.
  ### Q2 — Tesla Revenue Data (Last 5 Rows)

| Date                          | Revenue |
|-------------------------------|---------|
| 1970-01-01 00:00:00.000002017 | 11759   |
| 1970-01-01 00:00:00.000002018 | 21461   |
| 1970-01-01 00:00:00.000002019 | 24578   |
| 1970-01-01 00:00:00.000002020 | 31536   |
| 1970-01-01 00:00:00.000002021 | 53823   |


### Question 3: Extract GameStop Stock Data
- Used `yfinance` to create a Ticker object for GameStop (GME).
- Extracted historical stock data (`period="max"`).
- Reset the index and displayed the first five rows.
### Q3 — GameStop Stock Data (First 5 Rows)

| Date                       | Open     | High     | Low      | Close    | Volume    | Dividends | Stock Splits |
|----------------------------|----------|----------|----------|----------|-----------|-----------|--------------|
| 2002-02-13 00:00:00-05:00  | 1.620128 | 1.693350 | 1.603296 | 1.691667 | 76216000  | 0.0       | 0.0          |
| 2002-02-14 00:00:00-05:00  | 1.712707 | 1.716074 | 1.670626 | 1.683250 | 11021600  | 0.0       | 0.0          |
| 2002-02-15 00:00:00-05:00  | 1.683250 | 1.687458 | 1.658002 | 1.674834 | 8389600   | 0.0       | 0.0          |
| 2002-02-19 00:00:00-05:00  | 1.666418 | 1.666418 | 1.578047 | 1.607504 | 7410400   | 0.0       | 0.0          |
| 2002-02-20 00:00:00-05:00  | 1.615920 | 1.662209 | 1.603295 | 1.662209 | 6892800   | 0.0       | 0.0          |


### Question 4: Extract GameStop Revenue Data
- Used `requests` to scrape the GameStop revenue page.
- Parsed HTML using `BeautifulSoup`.
- Extracted the GameStop Quarterly Revenue table into a DataFrame (`gme_revenue`).
- Cleaned data by removing `$` and `,` and dropping null values.
### Q4 — GameStop Revenue Data (Last 5 Rows)

| Date       | Revenue |
|------------|---------|
| 2006-01-31 | 1667    |
| 2005-10-31 | 534     |
| 2005-07-31 | 416     |
| 2005-04-30 | 475     |
| 2005-01-31 | 709     |


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
