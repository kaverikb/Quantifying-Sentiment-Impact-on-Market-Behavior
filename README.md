**Analyzing how trading behavior (profitability, risk, volume, and leverage) aligns with market sentiment (Fear vs. Greed)**

---

### Overview

This project explores the relationship between **market sentiment** and **trading behavior**, using the **Fear & Greed Index** alongside historical trade data.
The goal was to identify whether emotional market conditions such as *Fear* and *Greed* influence how traders perform — in terms of **profitability, participation, and risk-taking behavior**.

The workflow follows a structured, multi-stage process:

1. **Data cleaning and preparation**
2. **Independent exploration of sentiment and trading data**
3. **Integrated analysis of trading behavior under different emotional regimes**

---

### Folder Structure

```
DS_Kaveri_Biswas/
│
├── notebooks/
│   ├── Book1_Data_Preparation.ipynb
│   ├── Book2_Independent_EDA.ipynb
│   └── Book3_Merged_Analysis.ipynb
│
├── data/
│   ├── sentiment_cleaned.csv
│   ├── data_cleaned.csv
│   └── merged_dataset.csv
│
├── summaries/
│   ├── Summary_Book1_Data_Preparation.md
│   ├── Summary_Book2_EDA.md
│   ├── Summary_Book3_Merged_Analysis.md
│   └── Final_Project_Summary.md
│
├── outputs/
│   ├── sentiment_trend.png
│   ├── pnl_distribution.png
│   ├── volume_vs_sentiment.png
│   └── risk_efficiency_chart.png
│
├── report/
│   └── ds_report.pdf
│
└── README.md
```

---

### Phase 1: Data Preparation (Book1)

**Goal:** Prepare both datasets for analysis.

* Standardized all timestamps (UTC alignment).
* Removed duplicates, invalid rows, and missing timestamps.
* Aggregated to daily granularity to merge market sentiment and trading data.
* Created `date_key` for consistent merge logic.
* Exported cleaned datasets:

  * `sentiment_cleaned.csv`
  * `data_cleaned.csv`
  * `merged_dataset.csv`

**Outcome:**
Three high-quality datasets, each consistent and merge-ready for behavioral analysis.

---

### Phase 2: Independent Exploration (Book2)

#### Sentiment Data

* Covered 2018–2025, showing recurring emotional cycles of Fear and Greed.
* High autocorrelation (~0.95) indicating persistence in sentiment.
* Emotional extremes align with major volatility events, confirming sentiment’s predictive potential.

#### Trading Data

* Spanned Sep 2024–Apr 2025 with 7,000+ trades.
* Most trades near breakeven; few large wins/losses dominated results.
* Daily activity spiked in early 2025 — suggesting high market volatility.

**Outcome:**
Understanding both emotional context (sentiment) and behavioral response (trading) separately helped define merging logic and hypothesis for integrated analysis.

---

### Phase 3: Integrated Analysis (Book3)

#### 1. Profitability vs Sentiment

* Mean profit rises with optimism (Neutral → Fear → Greed → Extreme Greed).
* Median profit ~0 across all phases, showing heavy-tailed outcomes.
* Win rate peaks in Extreme Greed (≈47%) and drops in Neutral (~35%).
* Risk also rises sharply, showing overconfidence bias during Greed.

#### 2. Volume & Participation vs Market Sentiment

* Trading volume highest during Fear and Extreme Fear.
* Fear-driven spikes often precede sentiment changes, indicating panic-based reaction.
* Greed periods show fewer but more confident trades.

#### 3. Risk & Efficiency

* PnL volatility and risk-taking behavior surge in emotional markets.
* Traders behave defensively under Fear (larger, concentrated bets).
* Greed produces frequent, smaller, confidence-driven trades.

**Outcome:**
Emotions don’t dictate trade direction but intensity.
Fear inflates participation and volatility; Greed improves success rate but not consistency.
Sentiment-driven awareness can guide smarter position sizing and leverage management.

---

### Key Visual Outputs

Saved in `/outputs/`:

* **sentiment_trend.png:** Evolution of Fear–Greed sentiment over time
* **pnl_distribution.png:** Distribution of profitability across sentiment regimes
* **volume_vs_sentiment.png:** Trading volume behavior under Fear vs. Greed
* **risk_efficiency_chart.png:** Risk–return efficiency comparisons across emotional states

---

### Report and Summaries

All supporting explanations are documented in the `/summaries/` folder.
The complete compiled report (`ds_report.pdf`) is included in `/report/`.

---

### Final Insight

Market emotion governs **intensity, not direction**.
Fear triggers overreaction and volume surges; Greed fuels confidence and profit variance.
Neutral sentiment brings calm and balanced performance.
Combining emotional indicators with behavioral metrics can significantly improve trading strategy design.

