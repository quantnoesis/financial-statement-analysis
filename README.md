# Financial Statement Analysis — Top 200 US Companies

A beginner data analysis project exploring financial ratios (ROE, current ratio, 
debt-to-equity) across 200 major US companies, built to combine a finance/accounting 
background with hands-on Python practice.

## What's in this project

- `financialdata.csv` — dataset used (source: Kaggle)
- `[your notebook filename].ipynb` — the full analysis notebook (Python, pandas, matplotlib)

## What I did

- Loaded and explored the dataset (structure, missing values, summary stats)
- Ranked companies by Return on Equity (ROE) and visualized the top 10
- Ranked companies by Current Ratio (liquidity) and visualized the top 10
- Plotted ROE against Debt-to-Equity across all 200 companies to check whether 
  high ROE tends to come with high leverage

## Key finding

McKesson Corporation had the highest ROE in the dataset — but a high ROE alone 
doesn't mean strong performance. It can be inflated by low or negative shareholder 
equity (for example, from heavy stock buybacks), so ROE should always be checked 
alongside debt levels rather than read on its own.

## Tools used

Python, pandas, matplotlib, Google Colab
