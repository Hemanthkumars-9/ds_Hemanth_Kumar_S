# Trader Behavior vs Market Sentiment (Fear vs Greed)

This project analyzes how trading behavior (PnL, win rate, volume) changes across different market sentiment regimes using Hyperliquid historical trade data and the Bitcoin Fear \& Greed Index.

The goal is to identify patterns that can help improve trading decisions and risk management.

----

## 📌 Project Structure

ds\_<your\_name>/
├── notebook\_1.ipynb
├── csv\_files/
│ ├── historical\_trades.csv
│ ├── fear\_greed.csv
│ ├── merged\_trades\_with\_sentiment.csv
│ ├── account\_daily\_metrics.csv
│ └── kpi\_by\_sentiment.json
├── outputs/
│ ├── daily\_pnl\_by\_sentiment.png
│ ├── volume\_usd\_by\_sentiment.png
│ ├── winrate\_by\_sentiment.png
│ └── logreg\_metrics.txt
├── ds\_report.pdf
└── README.md

----

## 🚀 How to Run the Notebook

1. Open `notebook\_1.ipynb` in **Google Colab**.
2. Run all cells from top to bottom.
3. The notebook will:
  - Load and clean the raw data  

  - Fix timestamps (IST → UTC)

  - Merge sentiment with trade data

  - Compute profitability, win rate, and volume metrics

  - Generate charts and KPIs

  - Save outputs into `/csv\_files` and `/outputs`


## 📊 Key Steps Performed


- Cleaned and standardized timestamps  

- Merged sentiment and trade data by UTC date  

- Aggregated daily metrics (PnL, winrate, volume) per account  

- Compared Greed days vs. Fear days  

- Visualized differences using bar charts  

- Exported insights + metrics into CSV/JSON files  

- Produced a final summary report (`ds\_report.pdf`)


## ✅ Insights Summary


- **Profitability:** Mean PnL doesn't change significantly across Fear/Greed, but median PnL is higher on Greed days.

- **Winrate:** Very similar across both sentiments (~36–37%).

- **Volume:** Traders commit **significantly more capital on Fear days**, indicating higher risk exposure.

- **Takeaway:** Market sentiment affects **risk behavior**, not prediction accuracy.



## 📁 Outputs

All generated files (charts + metrics) are available in:

- `/csv\_files/` (processed datasets)

- `/outputs/` (plots and model results)


## 📝 Notes

- This analysis uses daily sentiment data. Intraday sentiment not included.

- Unknown sentiment days come from missing rows in the Fear/Greed dataset.

- Data does not include leverage fields, so risk behavior is measured through volume.


If you have any trouble running the notebook or need help understanding specific sections, feel free to reach out!



