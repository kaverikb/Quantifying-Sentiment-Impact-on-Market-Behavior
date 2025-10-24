Data Cleaning and Preparation

Objective
To inspect, clean, and align two independent datasets : the Fear & Greed Index (sentiment)
and trading history. Ensuring both are consistent, reliable, and ready for merged analysis.
Key Cleaning Steps

1. Structure and Format Validation
• Verified shapes, column names, and data types for both files to understand their structure.
• Identified inconsistencies in timestamp formats such as mixed epoch and IST time zones in
the trading data.
• Standardized all datetime columns to a common UTC-based date for reliable merging later.
2. Handling Missing and Invalid Entries
• Checked for null or malformed timestamp values using .isna() and filled or dropped them
where necessary.
• Removed duplicate trades and overlapping entries within the same time window to avoid
inflated volume counts.
• Filtered out incomplete rows and lines with structural errors that could disrupt analysis.
3. Temporal Alignment
• Rounded timestamps in both datasets to daily granularity, ensuring one sentiment record
matched a set of trades for that day.
• Confirmed consistent date ranges; sentiment covering 2018–2025 and trading covering
2024–2025, leaving an overlapping window for joint study.
4. Aggregation and Key Generation
• Created a unified date_key column as the central merge point between the two datasets.
• Tested both inner and left merge options to retain all trades while assigning each to its
corresponding sentiment day.
• Validated merge accuracy by manually checking a few random samples.
5. Output and Reusability
• Saved three clean files:
• sentiment_cleaned.csv — normalized Fear & Greed Index
• data_cleaned.csv — cleaned trade-level dataset
• merged.csv — integrated version for later analysis
• Ensured each file is lightweight, reproducible, and free from conversion issues.

Insights from Cleaning
• Cleaning revealed the temporal complexity of the trading data and the slow-moving nature
of sentiment data.
• It became clear that merging should occur at a daily level to balance granularity and
interpretability.
• This stage set the foundation for meaningful EDA in the next notebooks : Book2 for
independent exploration and Book3 for integrated behavioral analysis.