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
## 📁 Files & Metadata
asset_metadata.csv – Asset sector, type, risk class

synthetic_data_responses.csv – Generated log returns

Presentation.pptx – Architecture, methodology, and visual diagnostics

## 📈 Use Cases
Stress testing of new asset portfolios

Bootstrapping data for ML models

Scenario analysis for strategic financial planning

Safe generation of data for compliance-sensitive environments

## 🚧 Limitations
LLMs may struggle with accurate tail modeling

No multivariate correlation across assets

Requires iterative prompting for high-fidelity results

## 🔮 Future Directions
GUI-based synthetic data lab

Fine-tuned financial LLMs (e.g., FinGPT, FinBERT)

Multivariate return generation

RAG for dynamic financial prompting

## 👥 Authors
Charan Kumar Pathakamuri

Darren Dcunha
