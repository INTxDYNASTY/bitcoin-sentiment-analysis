# Bitcoin Market Sentiment vs Trader Performance Analysis

## Project Overview

This project analyzes the relationship between Bitcoin market sentiment and trader performance using historical trading data from Hyperliquid and the Bitcoin Fear & Greed Index.

The objective is to determine how different market sentiment conditions (Fear, Greed, Extreme Fear, Extreme Greed, and Neutral) influence trading behavior and profitability. The analysis provides insights that can help traders make more informed trading decisions.

---

## Dataset Description

### 1. Bitcoin Market Sentiment Dataset
Contains daily market sentiment information.

**Columns**
- Timestamp
- Date
- Value (Fear & Greed Index)
- Classification
  - Extreme Fear
  - Fear
  - Neutral
  - Greed
  - Extreme Greed

### 2. Historical Trader Data (Hyperliquid)

Contains historical trading activity.

**Important Columns**
- Account
- Coin
- Execution Price
- Size Tokens
- Size USD
- Side (Buy/Sell)
- Timestamp
- Start Position
- Direction
- Closed PnL
- Fee
- Transaction Hash

---

## Project Workflow

### Step 1
Loaded both datasets into Pandas DataFrames.

### Step 2
Performed data cleaning:
- Checked missing values
- Removed duplicate records
- Converted UNIX timestamps into readable dates

### Step 3
Merged both datasets using the common **Date** column so that every trade was associated with the corresponding market sentiment.

### Step 4
Performed Exploratory Data Analysis (EDA) to study the relationship between market sentiment and trading performance.

---

## Analysis Performed

The following analyses were conducted:

- Number of trades under each market sentiment
- Average Closed PnL by sentiment
- Total profit by sentiment
- Average trade size by sentiment
- Buy vs Sell distribution
- Trading fee analysis
- Profit distribution using boxplots and histograms
- Top performing traders
- Most profitable coins
- Correlation analysis using a heatmap
- Highest profit and highest loss trades

---

## Key Insights

- Trading activity varies across different market sentiment conditions.
- Trader profitability changes depending on market sentiment.
- Buy and Sell behavior differs between Fear and Greed periods.
- Trade sizes are not uniform across sentiment categories.
- A small number of trades contribute significantly to overall profit and loss.
- Certain coins consistently generate higher profits than others.

---

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

## Repository Structure

```
├── analysis.ipynb
├── README.md
├── fear_greed_index.csv
├── historical_data.csv
└── output graphs
```

---

## Conclusion

This analysis demonstrates that market sentiment has a measurable influence on trader behavior and trading performance. By combining trader history with the Bitcoin Fear & Greed Index, it is possible to identify patterns in profitability, trading activity, and risk-taking behavior.

Such insights can support the development of data-driven trading strategies and improve decision-making under different market conditions.
