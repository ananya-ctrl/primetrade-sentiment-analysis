# Project Summary

## Objective
This project analyzes how Bitcoin market sentiment relates to trader behavior and performance on Hyperliquid.

## Methodology
- Loaded and inspected both datasets
- Checked shapes, missing values, and duplicates
- Converted timestamps into proper datetime format
- Aligned both datasets at the daily level using overlapping dates
- Created daily performance and behavior metrics
- Compared performance across Fear, Greed, and Neutral sentiment conditions
- Segmented traders into:
  - Frequent vs Infrequent
  - Consistent Winners vs Inconsistent
  - High Size vs Low Size

## Main Findings
- Fear days produced the strongest average performance in the aligned sample.
- Fear days also showed the highest trading activity and largest average trade size.
- Greed days were relatively more sell-heavy.
- Frequent traders outperformed infrequent traders.
- High Size traders had slightly better average daily PnL, but lower win rate than Low Size traders.

## Strategy Recommendations
1. Allow stronger participation on Fear days, but with controlled risk.
2. Be more selective on Greed days and avoid blindly increasing exposure.
3. Increase activity mainly for trader profiles that already show stable execution quality.

## Limitation
The overlap between the sentiment dataset and trader dataset is limited, so the results should be interpreted as directional insights rather than universal rules.