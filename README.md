# Junior Data Scientist – Trader Behavior Insights

## Overview
This project analyzes the relationship between **trader performance** and **Bitcoin market sentiment** using historical trader data from Hyperliquid and the Bitcoin Fear & Greed Index. The goal is to uncover hidden patterns, behavioral insights, and actionable trading strategies.  

---

## Dataset
1. **Historical Trader Data** (`trader_data_hyperliquid.csv`)  
   - Columns include: `account`, `symbol`, `execution price`, `size`, `side`, `time`, `start position`, `event`, `closedPnL`, `leverage`, etc.  
   - Captures individual trader activity, trades executed, and profit/loss.  

2. **Bitcoin Market Sentiment Data** (`fear_greed_index.csv`)  
   - Columns: `Date`, `Classification` (e.g., Fear, Greed)  
   - Represents daily market sentiment using the Fear & Greed Index.  

> **Note:** Ensure both CSV files are in the same directory as the notebook before running the analysis.  

---

## Environment
- Python 3.12  
- Libraries used:  
  - `pandas` (data manipulation)  
  - `numpy` (numerical operations)  
  - `matplotlib` & `seaborn` (visualizations)  

---

## Project Workflow
1. **Data Loading**  
   - Load the trader data and sentiment data CSV files.  
   - Inspect columns and data types.  

2. **Data Cleaning & Preprocessing**  
   - Convert timestamps to `datetime` objects.  
   - Ensure numeric columns (`closedPnL`, `size`) are clean.  
   - Handle missing values.  

3. **Feature Engineering**  
   - Aggregate trader data to calculate **daily PnL**, total volume, and number of trades per trader.  
   - Extract daily sentiment labels.  

4. **Exploratory Data Analysis (EDA)**  
   - Analyze overall trader performance against market sentiment.  
   - Compare average PnL across Fear and Greed days.  

5. **Trader Segmentation & Deep Dive**  
   - Segment traders into **Top 25% (Successful)**, **Bottom 25% (Unsuccessful)**, and **Mid-Tier** based on total PnL.  
   - Evaluate segment performance under different market sentiments.  

6. **Trading Activity Analysis**  
   - Calculate total buy/sell volume by sentiment.  
   - Analyze net flow and buy/sell imbalances.  

7. **Insights & Strategy Recommendation**  
   - Summarize key findings from data analysis.  
   - Propose a simple sentiment-driven trading strategy based on successful trader behavior.  

8. **Optional Enhancements**  
   - Export merged datasets for further use.  
   - Enhanced visualizations: heatmaps, pie charts, line charts.  

---

## Key Insights
- Traders perform differently under Fear and Greed conditions.  
- Successful traders often profit more during certain sentiment periods (e.g., Fear).  
- Buy/Sell imbalances provide opportunities for contrarian strategies.  
- Net flow analysis highlights market participation patterns under different sentiment levels.  

---

## How to Run
1. Place the CSV files in the same directory as the notebook.  
2. Open the Jupyter Notebook (`Trader_Behavior_Insights.ipynb`).  
3. Run the cells sequentially from 1 to 10.  
4. Optional: Export the results using the provided cells.  

---

## Files Included
- `Trader_Behavior_Insights.ipynb` – Main notebook with all analysis  
- `trader_data_hyperliquid.csv` – Historical trader data  
- `fear_greed_index.csv` – Bitcoin market sentiment data  
- `trader_sentiment_analysis.csv` – Exported merged dataset (optional)  
- `segment_pnl_summary.csv` – Exported segment-level summary (optional)  

---

## Future Enhancements
- Include **time-lagged sentiment effects** on PnL.  
- Explore **leverage impact** on trader performance.  
- Develop **interactive dashboards** for real-time insights.  
