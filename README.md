# 📈 Data-Driven Investment Intelligence Using NIFTY-50


An AI-powered investment intelligence platform built on 21 years of NIFTY-50 historical data. The system combines machine learning, portfolio optimization, and risk analytics to support data-driven investment decisions for three investor profiles: Conservative, Balanced, and Aggressive.

---

## 🔍 Project Modules

| Module | Description |
|---|---|
| EDA | Return distribution, sector analysis, volatility, correlation heatmap |
| Feature Engineering | 15 technical indicators per stock (MA, EMA, MACD, RSI, Bollinger Bands, ATR, OBV) |
| Stock Predictor Engine | XGBoost regression (return magnitude) + classification (price direction) |
| Portfolio Construction | Mean-Variance Optimization for 3 investor profiles |
| Risk Assessment | Sharpe Ratio, Sortino Ratio, Max Drawdown, VaR (95%) |
| Explainability | XGBoost feature importance analysis |

---

## 📊 Key Results

### Stock Prediction
| Metric | Value |
|---|---|
| Mean RMSE (49 stocks) | 0.02696 |
| Mean MAE (49 stocks) | 0.01841 |
| Best Stock (HDFCBANK RMSE) | 0.01682 |
| Mean Directional Accuracy | 50.00% |

### Portfolio Performance
| Portfolio | Return | Volatility | Sharpe Ratio |
|---|---|---|---|
| Conservative | 13.27% | 15.84% | 0.459 |
| Balanced | 12.57% | 18.96% | 0.346 |
| Aggressive | 23.90% | 21.37% | 0.838 |

### Top Stocks by Sharpe Ratio
| Stock | Sharpe | Max Drawdown |
|---|---|---|
| SHREECEM | 0.827 | -79.97% |
| BAJFINANCE | 0.678 | -93.28% |
| BAJAJFINSV | 0.656 | -86.79% |
| NESTLEIND | 0.569 | -32.40% |

---

## ⚙️ Setup & Run

### 1. Clone the repo
```bash
git clone https://github.com/radhika-wq/NIFTY50-Investment-Intelligence.git
cd NIFTY50-Investment-Intelligence
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Download the dataset
Download from Kaggle:
👉 https://www.kaggle.com/datasets/rohanrao/nifty50-stock-market-data/data

Create a `data/` folder in the project root and place all CSV files inside it.

### 4. Run the notebook
```bash
jupyter notebook final.ipynb
```
Run all cells from top to bottom.

---

## 📦 Dataset

| Parameter | Value |
|---|---|
| Source | Kaggle — rohanrao/nifty50-stock-market-data |
| Stocks | 49 NIFTY-50 companies |
| Date Range | January 2000 – April 2021 |
| Total Records | 235,192 (after cleaning) |
| Features Engineered | 15 technical indicators per stock |

> ⚠️ Dataset not included in this repo due to Kaggle licensing. Download separately using the link above.

---

## 🛠️ Tech Stack

- **Python 3.x**
- pandas, numpy — data processing
- matplotlib, seaborn — visualisation
- scikit-learn — model evaluation, cross-validation
- xgboost — prediction models
- ta — technical indicators
- scipy — portfolio optimisation

---

## 📓 Notebook Structure
The entire project is in one notebook `final.ipynb`:
1. Data Loading & Cleaning
2. Exploratory Data Analysis
3. Feature Engineering (15 technical indicators)
4. Stock Predictor Engine (XGBoost)
5. Portfolio Construction (Mean-Variance Optimization)
6. Risk Assessment (Sharpe, Sortino, Max Drawdown, VaR)
7. Feature Importance & Explainability
8. Project Summary Dashboard

## 💡 Key Insights
- NESTLEIND is the safest stock — lowest volatility (24.23%) and smallest drawdown (-32.40%)
- SHREECEM has the best Sharpe Ratio (0.827) among all 49 stocks
- Aggressive portfolio achieves 23.90% return vs 13.27% conservative — nearly double
- BB_Low (Bollinger Band) is the most predictive feature at 62% importance
- COALINDIA and WIPRO have negative Sharpe ratios — destroyed wealth on risk-adjusted basis
- Mean directional accuracy of 50% is honest and expected — markets are near-random
---

## 🗂️ Repository Structure
