# Trader Performance vs Market Sentiment

This project analyzes how Bitcoin market sentiment (Fear/Greed) relates to trader behavior and performance on Hyperliquid.

The goal is to identify whether trader profitability, activity, and trading behavior change across different market sentiment conditions, and to extract actionable trading insights from the patterns observed.

## Project Objective

The analysis focuses on:

- cleaning and inspecting both datasets
- converting timestamps and aligning data at the daily level
- creating daily trading metrics such as:
  - total daily PnL
  - average PnL per trade
  - win rate
  - average trade size
  - average fee
  - number of trades per day
  - buy/sell ratio
- comparing performance across Fear, Greed, and Neutral sentiment conditions
- segmenting traders into behavioral groups
- proposing actionable strategy recommendations

## Datasets Used

1. **Bitcoin Market Sentiment (Fear/Greed)**  
   Columns used: `timestamp`, `classification`, `date`

2. **Historical Trader Data (Hyperliquid)**  
   Columns used: `Account`, `Execution Price`, `Size USD`, `Direction`, `Closed PnL`, `Fee`, `Timestamp`

## Project Structure

```text
primetrade-sentiment-analysis/
│
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   └── analysis.ipynb
├── outputs/
│   ├── charts/
│   ├── tables/
│   └── summary/
├── src/
├── README.md
├── requirements.txt
└── .gitignore
```

## Methodology
1. Data preparation
Loaded both datasets
Checked shapes, columns, missing values, and duplicates
Converted timestamps to proper datetime format
Created daily date keys
Aligned both datasets using overlapping dates only
2. Feature engineering

### Created day-level trading features including:

total daily pnl
average pnl per trade
win rate
average trade size in USD
average execution price
average fee
trades per day
buy trades
sell trades
buy/sell ratio
3. Analysis

### Compared trader performance and behavior across sentiment groups:

Fear
Greed
Neutral

### Also created 3 trader segments:

Frequent vs Infrequent traders
Consistent Winners vs Inconsistent traders
High Size vs Low Size traders
4. Strategy recommendations

Based on the findings, proposed practical rules of thumb for trading behavior under different sentiment conditions.

## Key Findings
Fear days showed the strongest performance in the aligned sample, with the highest average total daily PnL, average PnL per trade, and win rate.
Fear days also showed the highest average trade size and the highest activity level.
Greed days appeared relatively more sell-heavy, with a buy/sell ratio below 1.
Frequent traders outperformed infrequent traders on both average daily PnL and win rate.
High Size traders had slightly higher average daily PnL than Low Size traders, but their average win rate was lower.
Strategy Recommendations
Allow stronger participation on Fear days, but with controlled risk.
Be more selective on Greed days and avoid blindly increasing exposure.
Increase activity primarily for trader profiles that already show stable performance.
Important Note

The overlap between the sentiment dataset and historical trader dataset is limited.
Because of that, the results should be treated as directional insights based on the aligned sample, not as universal market rules.

## How to Run

### 1. Clone the repository

git clone <your-repo-link>
cd primetrade-sentiment-analysis

### 2. Create and activate a virtual environment
python -m venv .venv
.venv\Scripts\activate

### 3. Install dependencies
pip install -r requirements.txt


### 4. Open the notebook
Open notebooks/analysis.ipynb in VS Code or Jupyter and run all cells in order.

