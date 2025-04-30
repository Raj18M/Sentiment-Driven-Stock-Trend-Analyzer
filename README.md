# Sentiment-Driven Stock Trend Analyzer

This project provides a generalized Python-based pipeline for conducting sentiment analysis on any stock using its related news headlines and historical stock prices. The goal is to extract insights about price movements by combining fundamental sentiment signals with technical indicators and anomaly detection.

---

## 🔍 What This Project Does

- Retrieves **100 recent news headlines** for a given stock ticker from Google's RSS feed.
- Applies **VADER sentiment analysis** to the headlines.
- Fetches **closing stock prices** from Yahoo Finance and maps them to news sentiment based on the article's publish date.
- Calculates **technical indicators**:
  - SMA (10-day)
  - LMA (50-day)
  - Labels the trend as Bullish / Bearish / Neutral
- Applies **Isolation Forest** to detect anomalies in the stock price.
- Maps anomalies to relevant news headlines for deeper context.
- Extracts key named entities (like people, locations, policies) from headlines using **spaCy**.

---

## 🧰 Tech Stack

- Python
- Google Colab
- Pandas, NumPy
- VADER Sentiment Analyzer (`nltk.sentiment.vader`)
- Yahoo Finance (`yfinance`)
- Isolation Forest (`sklearn.ensemble`)
- SpaCy (Named Entity Recognition)
- Matplotlib / Seaborn for visualizations

---

## 🚀 How to Use

1. Clone this repository or open the `.ipynb`.
2. Replace the default stock ticker (e.g., `'RELIANCE.NS'`) with your desired stock's ticker First chunk of code where you define replace [reliance] then change the ticker symbol before executing yfinance library.
4. Run all cells from top to bottom.
5. Output files will be saved to your Google Drive (Excel format) with:
   - News + sentiment data
   - Mapped stock prices and trends
   - Anomaly-marked datasets

---

## 📦 Output

- `news_data.xlsx` – headlines and URLs  
- `sentiment_scores.xlsx` – VADER scores  
- `price_sentiment_trend.xlsx` – price + SMA/LMA + trend  
- `anomaly_mapped_articles.xlsx` – anomalies linked with headlines

---

## ✅ Why Use This?

This project provides a modular, reusable framework for integrating:
- **Fundamental signals** (from news headlines),
- **Technical trend indicators**, and
- **ML-based anomaly detection**.

It’s ideal for finance students, ML enthusiasts, or anyone interested in understanding market movements through a hybrid lens.

---

## 📌 Example Use Case

Track how public sentiment around a company influences its stock trend, detect unexpected price jumps, and link them to key news events — all without needing full article access.
As an added bonus same analysis was conducted by just replacing the said adjustments (mentioning the stock/commodity name and it's respective ticker symbol). The analysis is on
Natural Gas, showing the range of applicability of this methodology to even commodities market.

---

## 📄 License

This project is licensed under the MIT License.

---

## 🤝 Contributions

Pull requests are welcome. For major changes, please open an issue first to discuss what you’d like to change.

---

## 🧠 Author

Developed by Raj Srivastava.

