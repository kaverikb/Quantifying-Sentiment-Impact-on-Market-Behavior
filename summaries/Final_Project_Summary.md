Final Summary: Market Sentiment and Trading Behaviour

Phase 1: Data Preparation (Book1)
Two datasets were prepared for analysis: the Fear & Greed Index and historical trading data.
Both were inspected for structure, missing values, and time inconsistencies. All timestamps
were converted into a uniform UTC-based daily format to ensure proper alignment. Duplicate
and incomplete entries were removed. Each trade was linked to its corresponding sentiment
value through a unified date key. Three clean versions were created: one for sentiment, one
for trading, and one merged dataset for analysis. This step ensured accuracy and consistency
before beginning exploratory work.

Phase 2: Independent Exploration (Book2)
Both datasets were explored separately to understand their patterns and potential
relationships.
Sentiment data
• Showed long-term emotional cycles with stable fear or greed phases punctuated by short
volatile transitions.
• High autocorrelation confirmed that sentiment changes slowly, often persisting for weeks.
• These emotional regimes created the psychological context needed to study trading
decisions.
Trading data
• Exhibited strong skewness in profitability where most trades closed flat and a few large
trades dominated results.
• Trade size and volume distributions revealed both retail-scale and high-value positions.
• Daily activity spiked sharply in early 2025, hinting at volatility-driven participation.
Exploring both separately showed that sentiment represented the market’s emotional state,
while trading captured behavioral reactions. This naturally led to the idea of merging the two
to understand how one influences the other.

Phase 3: Integrated Behavioral Analysis (Book3)
The merged dataset enabled direct comparison of trading outcomes under different emotional
conditions.
1. Profitability vs Sentiment
• Average profit increased steadily from Neutral to Extreme Greed, but median profit
remained near zero.
• Win rate improved under Greed, yet PnL volatility was highest during both Fear and Greed.
• Profits were driven by a small group of extreme trades, creating a heavy-tailed distribution.
• Emotional extremes amplified both gains and losses, showing that sentiment affected the
magnitude of outcomes more than their direction.
2. Volume and Participation vs Sentiment
• Trading volume rose sharply in Fear and Extreme Fear phases, while activity declined
during calm or greedy markets.
• Volume often surged before sentiment transitions, suggesting that traders react early to
emotional shifts.
• Extreme volume spikes were concentrated in fear-driven markets, reflecting panic-based
decision-making.
3. Risk, Efficiency and Market Behavior
• PnL volatility was highest in Fear and Greed periods, pointing to higher risk-taking in
emotional markets.
• Extreme Greed brought more frequent but smaller trades, while Fear led to larger and more
concentrated positions.
• Risk-adjusted efficiency remained inconsistent across regimes, highlighting unstable control
over volatility.

Overall Insight:
The analysis shows that sentiment governs the intensity of trading rather than its direction.
Fear increases participation and volatility, while Greed improves success rate but not stability.
Neutral conditions are characterized by low activity and limited dispersion in outcomes.
These behavioral links suggest that traders can benefit by adapting risk exposure to prevailing
sentiment. Scaling back in fearful markets and controlling optimism during greedy phases.
This multi-stage approach, from data cleaning to integrated analysis, demonstrates how
market emotion shapes trader behavior and decision patterns in measurable ways.