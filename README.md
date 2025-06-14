# FinSynGen: Synthetic Financial Data Generator using LLMs

## 📌 Overview
FinSynGen is a robust framework for generating synthetic financial return data using Large Language Models (LLMs). It enables users to simulate realistic return sequences for stocks, ETFs, and indexes—useful for stress testing, Monte Carlo simulations, trading strategy backtesting, and AI model training.

This project leverages `yfinance` for real data collection and GPT-powered generation for synthetic data. A feedback loop ensures that outputs adhere to statistical realism such as volatility, skewness, and kurtosis.

## 🔁 Workflow

1. **Setup & Helper Functions**
2. **Load Real Financial Data (2019–2024)**  
   - Tickers: AAPL, MSFT, AMZN, NVDA, QQQ, SPY, ^GSPC, etc.
   - Daily OHLC, Log Returns, Moving Average, Volatility
3. **Extract Return Segments** (Windowed)
4. **Prompt Formatting for LLM**
5. **Generate Synthetic Log Returns**
6. **Score Outputs with Statistical Metrics**
7. **Reinforcement Prompting**  
   - Auto-corrects synthetic sequences based on KS-Test, Skew, Kurtosis
8. **Monte Carlo Simulation**  
   - GBM with 1,000 paths over 60 days
9. **Business Use Cases**  
   - Prompt-driven scenario modeling, stress testing, synthetic portfolios

## 📊 Statistical Metrics

- **Mean**  
- **Standard Deviation (Volatility)**  
- **Skewness**  
- **Kurtosis (Fat Tails)**  
- **Kolmogorov–Smirnov Test**  

## 🛠️ Technologies Used

- Python, Pandas, NumPy
- yFinance for real-time asset data
- OpenAI/GPT (or Gemini) for generation
- Matplotlib for diagnostics
- Scikit-learn, SciPy (for scoring and validation)

## 🧠 Prompt Example

```plaintext
Generate synthetic log returns for a high-risk crypto asset with extreme volatility and fat tails over a 60-day period.


## 📈 Use Cases

- **Stress Testing**: Evaluate new or illiquid portfolios under extreme market scenarios  
- **ML Model Training**: Bootstrap synthetic data for training machine learning models  
- **Strategic Scenario Planning**: Simulate user-defined asset behavior over time  
- **Compliance-Friendly Prototyping**: Generate financial data without exposing sensitive records  

---

## 🚧 Limitations

- ❗ LLMs may struggle with accurate **tail modeling**
- 🔗 Currently lacks **multivariate correlation** between assets
- ♻️ **Iterative prompting** needed to match statistical fidelity

---

## 🔮 Future Directions

- 🧪 **GUI-based synthetic data lab** for interactive generation and testing
- 🏦 **Fine-tuned financial LLMs** like `FinGPT` and `FinBERT` for improved contextual awareness
- 📉 **Multivariate return generation** to model portfolio-level interactions
- 🧵 **RAG pipelines** for prompt enrichment based on financial context

---

## 👥 Authors

- **Charan Kumar Pathakamuri**  
- **Darren Dcunha**

---

> 🚀 *Synthetic data complements real data—never replaces it. Use strategically to simulate risk and innovation in finance.*
