# Market Risk During Financial Stress

**A comparison of volatility, drawdowns, recovery and market sensitivity**

- **Project type:** Independent finance project
- **Data period:** January 2020 to December 2021
- **Tools used:** Python, Pandas, NumPy, Matplotlib and Google Colab

## About the Project

In this project, I looked at how the stock market behaved during the COVID-19 market crash in February and March 2020. I compared four Indian companies with the NIFTY 50 index.

I wanted to see how much their prices moved, how far they fell during the crash, how long they took to recover, and how their daily returns were related to the market.

## Companies and Index

- Reliance Industries (RELIANCE)
- HDFC Bank (HDFCBANK)
- Infosys (INFY)
- Tata Motors (TMPV)
- NIFTY 50 (market benchmark)

The company data came from NSE historical equity data files. I kept the EQ series used in the analysis. The Tata Motors data is the NSE series downloaded under the symbol TMPV and covers the company as it traded in 2020–2021, before the 2025 demerger. It should not be treated as data for only today's commercial vehicles business.

I used historical NIFTY 50 data from the official NIFTY Indices website as the market benchmark.

## Time Periods

| Period | Dates |
|---|---|
| Before the stress period | 1 January – 19 February 2020 |
| Stress period | 20 February – 23 March 2020 |
| Recovery period | 24 March 2020 – 31 December 2021 |

The stress period covers the acute COVID-19 market sell-off. The dates were chosen retrospectively, so this should be kept in mind when interpreting the results.

## What I Did

I cleaned the data, arranged it by date, and calculated daily returns. Then I compared the results across the three periods.

The project includes:

- **Daily returns:** The percentage change between one closing price and the previous closing price.
- **Annualized volatility:** A measure of how much daily returns varied, scaled to a year using 252 trading days.
- **Maximum drawdown:** The largest fall from an earlier closing-price peak to a later low.
- **Recovery time:** Calendar days from the maximum-drawdown trough until the closing price first returned to or exceeded its earlier peak.
- **Correlation:** A measure of how closely two sets of daily returns moved together.
- **Beta:** A measure of how a stock's returns moved in relation to NIFTY 50 returns.
- **Trading volume:** A comparison of average daily trading volume before and during the stress period.
- **Normalized price chart:** A chart that starts each price series at 100 so their movements are easier to compare.

## Main Findings

- Volatility increased during the stress period for all five series.
- Tata Motors had the largest maximum drawdown, at about **67.4%**.
- Infosys had the smallest maximum drawdown among the four stocks, at about **34.2%**.
- Reliance took about **74 calendar days** to recover to its earlier peak.
- Tata Motors took about **283 calendar days** to recover to its earlier peak.
- Average daily trading volume was higher during the stress period for all four stocks.
- Full-period beta was **1.096** for Reliance, **1.094** for HDFC Bank, **0.835** for Infosys and **1.386** for Tata Motors.
- Correlations with the NIFTY 50 ranged from **0.612 to 0.805** over the full period and from **0.827 to 0.903** during the stress period.

The full-period figures include the stress days, so the comparison with stress-period correlations is indicative only. The stress window has just 21 trading days, so these results should be interpreted carefully.

The results showed me that volatility is not the only way to compare risk. The size of a fall, recovery time and relationship with the wider market also matter.

## How to Run the Notebook

1. Open the `.ipynb` notebook in Google Colab.
2. If the original data files are not included in the repository, download the company data from the NSE India website and the NIFTY 50 data from the official NIFTY Indices website.
3. For each company, use the relevant historical equity data and retain the EQ series used in this project. Download NIFTY 50 data for the same date range.
4. Upload the required files to Colab when prompted by the notebook.
5. Run the cells from top to bottom and review the tables and charts.

Download options may change, so check that the downloaded symbols, dates and columns match the data expected by the notebook.

## Files in This Repository

The repository should contain these files; adjust the names below to match the files you upload:

- `Market_Risk_During_Financial_Stress_Project.pdf` — the report.
- `Market_Risk_During_Financial_Stress_Project_code.ipynb` — the Python notebook containing the analysis.
- `Market_Risk_DFS_Excel.xlsx` — cleaned data and results exported from the notebook (values, not formulas).
- `Market_Risk_During_Financial_Stress_Project_Readme.md` — this README.

## Limitations

- The project covers 2020–2021, four companies and one major stress event, so it does not represent the entire Indian stock market.
- The analysis uses end-of-day raw closing prices. Intraday movements are not captured, and corporate actions such as splits, bonuses or demergers can affect price comparisons.
- The pre-stress period contains 36 trading days and the stress period contains 21 trading days. Estimates from these short windows can be sensitive to individual daily returns.
- The stress period was chosen retrospectively with knowledge of the crash dates.
- Beta depends on the selected sample period and benchmark.
- Recovery is measured using closing prices returning to an earlier peak; dividends are not included.
- The Tata Motors series is pre-demerger and includes Jaguar Land Rover, so it should not be treated as a representation of only today's commercial vehicles business.
- Past results do not guarantee future performance.

## Data Sources

**Company data:** Historical daily equity data for Reliance Industries (RELIANCE), HDFC Bank (HDFCBANK), Infosys (INFY) and Tata Motors (TMPV) was obtained from the National Stock Exchange of India (NSE).

NSE historical equity reports:  
https://www.nseindia.com/all-reports#cr_equity

**Market benchmark:** Historical NIFTY 50 index data was obtained from the official NIFTY Indices website.

NIFTY Indices historical data:  
https://www.niftyindices.com/reports/historical-data

The study covers 1 January 2020 to 31 December 2021. Check the original sources for current download options and terms of use.

## Author

**Janhavi Malik**

This project was made for learning and academic portfolio purposes. It is not investment advice.
