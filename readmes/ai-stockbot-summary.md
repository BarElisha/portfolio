
# AI StockBot - Portfolio Tracker

AI StockBot is a Python-based terminal tool designed to help private investors track their portfolio performance over time. It integrates monthly deposits, calculates returns, and pulls live financial data from stock APIs. The tool is optimized for users who want full control over investment analysis without relying on external platforms.

## 🧠 Features
- Tracks monthly investments (e.g. 1,400 ILS to IB, 600 ILS to TASE)
- Calculates total return, per-asset yield, and Sharpe ratio
- Fetches live quotes using Yahoo Finance or Alpha Vantage
- Displays individual asset performance in percentage and ILS
- Supports currency conversion and portfolio segmentation (e.g. crypto, stocks)
- Portfolio stored in local files, no cloud needed

## 📁 Project Structure
```
stockbot/
├── main.py
├── portfolio.json
├── settings.py
├── fetch_prices.py
└── calculate_metrics.py
```

## ⚙️ Setup

### Prerequisites
- Python 3.9+
- `yfinance`, `pandas`, `numpy`
- (Optional) Alpha Vantage API key

### Installation

```bash
pip install -r requirements.txt
python main.py
```

## 📈 Output
- Terminal summary (total investment, return %, absolute gains)
- Optional CSV export (planned)
- Strategy suggestions (future roadmap)

## 🧰 Authors
Built by Bar Elisha and enhanced with technical support from ChatGPT (OpenAI).
