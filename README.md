# 📊 Trader Performance vs Market Sentiment Analysis

## 🔹 Objective

The goal of this project is to analyze how market sentiment (Fear vs Greed) influences trader behavior and performance on Hyperliquid, and to derive actionable trading insights.

---

## 🔹 Datasets Used

1. **Bitcoin Market Sentiment Dataset**

   * Columns: Date, Classification (Fear / Greed)

2. **Historical Trader Data (Hyperliquid)**

   * Includes: account, symbol, execution price, size, side, time, closedPnL, leverage, etc.

---
## 🔹 Data

Due to file size limitations, datasets are not included in this repository.

They can be downloaded from:
https://drive.google.com/drive/folders/1kY4dNxs6VUkm8htK0JYFmVoaGagkDJa7?usp=sharing

---

## 🔹 Methodology

### 1. Data Preparation

* Converted timestamps to datetime format
* Aligned both datasets on daily level
* Merged sentiment data with trading data
* Handled missing values and inconsistent column formats

### 2. Feature Engineering

Created key metrics:

* Daily PnL per trader
* Win rate (profitability)
* Trade frequency
* Average trade size
* Long/short ratio
* Leverage usage

### 3. Behavioral Analysis

Compared trader behavior across:

* Fear vs Greed sentiment
* Trade frequency
* Position bias (long vs short)
* Trade size and leverage

### 4. Trader Segmentation

Traders were segmented into:

* Frequent vs Infrequent traders
* Winners vs Losers

Performance and behavior were compared across these groups.

---

## 🔹 Key Insights

1. **Higher Volatility During Greed**

   * Greed periods show wider PnL distribution, indicating higher risk and reward.

2. **Cautious Behavior During Fear**

   * Trade frequency decreases, suggesting selective trading.

3. **Behavior Changes with Sentiment**

   * Traders adjust position sizes and trade direction depending on market sentiment.

4. **Segmentation Insight**

   * Frequent traders and high-activity accounts exhibit different risk-return profiles compared to infrequent traders.

---

## 🔹 Strategy Recommendations

### ✅ Strategy 1: Risk Reduction in Fear Markets

* Reduce leverage exposure
* Focus on fewer, high-confidence trades
* Avoid overtrading

### ✅ Strategy 2: Controlled Aggression in Greed Markets

* Increase participation moderately
* Cap leverage to manage downside risk
* Apply strict risk management (stop-loss, position sizing)

---

## 🔹 Bonus: Predictive Modeling

A Logistic Regression model was built to predict trade profitability using:

* Market sentiment
* Trade direction
* Trade size (log-transformed)

### Improvements:

* Handled class imbalance using `class_weight='balanced'`
* Added behavioral feature (trade direction)
* Applied log transformation to stabilize variance

### Findings:

* Sentiment and trade behavior influence profitability
* Model performance is moderate, indicating that profitability is inherently noisy and difficult to predict with limited features

---

## 🔹 How to Run

1. Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

2. Run the notebook:

```bash
jupyter notebook notebook.ipynb
```

---

## 🔹 Conclusion

Market sentiment plays a significant role in shaping trader behavior and performance. While sentiment alone cannot fully predict profitability, combining it with behavioral signals can improve decision-making and risk management.

---


