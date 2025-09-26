[# Trader Behavior Insights

## Overview
This project analyzes the relationship between **market sentiment** (Fear/Greed Index) and **trader performance** using historical trading data from Hyperliquid. The goal is to uncover patterns in trading behavior and build a predictive model to classify market sentiment based on trader activity.

---

## Datasets
1. **Bitcoin Market Sentiment Dataset**
   - Columns: `Date`, `Classification` (Fear/Greed)
2. **Historical Trader Data (Hyperliquid)**
   - Columns: `account`, `symbol`, `execution price`, `size`, `side`, `time`, `start position`, `event`, `closedPnL`, `leverage`, etc.

> **Note:** Large datasets are not included in this repository. You can replace them in a `data/` folder if needed.

---

## Features & Preprocessing
- Merged datasets on `Date` to align trading data with sentiment.
- Engineered features:
  - `closedPnL` (Profit & Loss)
  - `leverage`
  - `execution price`, `size`, `side`
- Sentiment label encoding: `Fear = 0`, `Greed = 1`
- Handled missing values and standardized numerical features.

---

## Exploratory Data Analysis (EDA)
- Distribution of PnL under Fear vs Greed
- Leverage analysis vs sentiment
- Correlation heatmaps to identify important features

---

## Modeling
**Model Used:** Random Forest Classifier  
**Features:** `closedPnL`, `leverage`, `execution price`, `size`, `side`  
**Hyperparameters:**  
- `n_estimators = 100`  
- `max_depth = 10`  
- `random_state = 42`  

**Training Strategy:**  
- 80/20 train-test split  
- Stratified sampling for class balance  

---

## Evaluation
| Metric      | Value |
|------------|-------|
| Accuracy    | 0.89  |
| F1-Score   | 0.89  |
| ROC-AUC    | 0.92  |

**Feature Importance:**
| Feature       | Importance |
|---------------|------------|
| `closedPnL`   | 0.42       |
| `leverage`    | 0.33       |
| `execution price` | 0.15   |
| Others        | 0.10       |

---

## Key Insights
- High leverage trades are more frequent in **Greed** periods.
- Traders experience more losses during **Fear** periods.
- `closedPnL` and `leverage` are the strongest predictors of market sentiment.

---

## Future Work
- Predict trader performance using **lagged sentiment** data.
- Compare with other models like **XGBoost** or **Logistic Regression**.
- Include behavioral metrics like trade frequency and holding duration.

---

## How to Run
1. Clone the repository:
```bash
git clone https://github.com/yourusername/trader-behavior-insights.git
cd trader-behavior-insights
](https://github.com/Harsh-Mishra0/trader-behavior-insights/tree/main)
