# PrimeTrade Data Science Assessment

# 📊 Trader Behavior & Sentiment Analysis

## 🧠 Objective
Analyze how trader performance and behavior change under different market sentiment regimes (Fear vs Greed), and build predictive + clustering models.

---

## 📁 Dataset
- Trade-level data (PnL, size, direction, account, etc.)
- Sentiment data (Fear & Greed Index)

---

## ⚙️ Data Preparation
- Converted timestamps (ms → datetime, UTC → IST)
- Aligned datasets at **date level**
- Handled missing values using **forward fill**
- Created key features:
  - `win` (PnL > 0)
  - `position_type` (Long / Short)
  - `leverage_proxy`

---

## 📊 Key Metrics
- Daily PnL
- Win rate
- Trade frequency
- Average trade size
- Long/Short ratio

---

## 📈 Key Insights

- **Fear / Extreme Fear:**
  - Higher trade frequency
  - Larger trade sizes
  - Indicates reactive / aggressive behavior

- **Greed / Extreme Greed:**
  - Lower trade frequency
  - Smaller trade sizes
  - More stable and controlled trading

- **PnL Behavior:**
  - Higher volatility during Greed
  - More stable during Fear

- **Win Rate:**
  - Highest during Extreme Greed

---

## 🤖 Modeling

### 🔹 Predictive Model
- Model: XGBoost Classifier
- Target: Next-day profitability bucket
- Features:
  - Trade size
  - Leverage proxy
  - Sentiment index
  - Win indicator

---

### 🔹 Clustering
- Algorithm: KMeans
- Segments identified:
  - Conservative traders
  - Aggressive traders
  - Consistent traders

---

## 🚀 Strategies

### 1. Fear Strategy (Risk Control)
- Reduce leverage
- Avoid overtrading
- Focus on high-confidence trades

### 2. Greed Strategy (Efficiency)
- Follow trend
- Maintain controlled risk
- Avoid unnecessary trades

---

## 🎯 Conclusion
Trader behavior is strongly influenced by sentiment:
- Fear → high activity + high risk
- Greed → controlled and stable trading

---

## 🛠 Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost


## The project can be executed via Jupyter Notebook after installing dependencies using requirements.txt
