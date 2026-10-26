# NIFTY 50: A 10-Year Analysis of Returns, Risk & Market Behaviour

## Project Overview
A Python-based analysis of historical NIFTY 50 index data sourced from NSE India, covering 1 April 2016 to 30 March 2026.

The project explores long-term performance, daily and annual returns, volatility, drawdowns and hypothetical investment outcomes.

## Questions Explored
- How did the NIFTY 50 index level change over the observed period?
- Which complete calendar years were strongest and weakest?
- What were the best and worst trading days?
- When was market volatility highest?
- What was the maximum drawdown?
- How long did the largest drawdown take to recover?
- What would a hypothetical ₹1 lakh tracking the index-level movement become?
- What happens to the hypothetical ending value if the strongest trading days are missed?

## Data Source
Historical NIFTY 50 index data downloaded from NSE India.

**Period:** 1 April 2016 – 30 March 2026

**Variables:**
- Date
- Open
- High
- Low
- Close
- Shares Traded
- Turnover (₹ Cr)

The original yearly files are preserved in `data/raw/`, while the combined cleaned dataset is stored in `data/processed/`.

## Tools Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- VS Code

## Project Workflow
1. Download historical NIFTY 50 data from NSE India
2. Inspect individual yearly CSV files
3. Validate consistency across files
4. Combine yearly datasets
5. Clean column names and convert dates
6. Validate missing values, duplicates and OHLC consistency
7. Calculate daily returns
8. Analyse annual returns
9. Calculate rolling volatility
10. Analyse drawdowns and recovery
11. Simulate hypothetical ₹1 lakh index-level growth
12. Run a missed-strongest-days counterfactual experiment
13. Summarise findings and create visualisations

## Key Findings
- NIFTY 50 index level moved from **7,713 to 22,331**
- Overall index-level change: **+189.53%**
- Equivalent CAGR: **11.22%**
- Hypothetical ₹1 lakh: **₹2,89,527**
- Best daily return: **+8.76% on 7 April 2020**
- Worst daily return: **-12.98% on 23 March 2020**
- Peak 21-day annualised volatility: **87.89% on 9 April 2020**
- Maximum drawdown: **-38.44%**
- Peak-to-full-recovery period: **300 calendar days**
- Strongest complete calendar year: **2017 (+28.65%)**
- Weakest complete calendar year: **2018 (+3.15%)**

## Visuals

### NIFTY 50 Journey

visuals/
  nifty50_10_year_journey.png

### Annual Returns

visuals/
  nifty50_annual_returns.png

### Best vs Worst Trading Day

visuals/
  nifty50_best_vs_worst_day.png

### Rolling Volatility

visuals/
  nifty50_rolling_volatility.png

### Maximum Drawdown

visuals/
  nifty50_drawdowns.png

### Missing the Strongest Days

visuals/
  nifty50_missing_strongest_days.png

- Stayed invested: **₹2,89,527**
- Missed strongest 5 days: **₹2,13,845**
- Missed strongest 10 days: **₹1,76,631**
- Missed strongest 20 days: **₹1,29,953**

This is a hindsight-based counterfactual experiment rather than an investment strategy.

## Project Structure
`nifty50-analysis/`
- `data/`
  - `raw/`
  - `processed/`
- `notebooks/`
  - `nifty50_analysis.ipynb`
- `visuals/`
- `src/`
- `README.md`
- `requirements.txt`

## Limitations
- NIFTY 50 itself is an index and cannot be invested in directly.
- The ₹1 lakh analysis tracks index-level movement rather than the realised return of an actual index fund or ETF.
- Taxes, transaction costs, fund expenses and tracking error are not included.
- The missing-strongest-days analysis uses hindsight and should not be interpreted as a trading strategy.
- 2026 is only partially represented through 30 March 2026 and is therefore not treated as a complete calendar year.

## Conclusion
Across the observed period, the NIFTY 50 showed substantial long-term growth, but that growth included periods of significant volatility and drawdown.

The analysis also illustrates why evaluating market performance requires more than looking at start and end values alone. Daily returns, volatility, drawdowns and recovery periods provide important context about the path taken between those points.