# Market-Sentiment-Trade-Performance-Dashboard
🧠 Overview

This project is a Power BI dashboard that analyzes trading performance using market data. It focuses on understanding profitability, risk, and market behavior using key metrics like Win Rate, Closed PnL, and Classification (sentiment).

The dashboard helps visualize how different trading factors such as coin type, execution price, risk group, and classification impact overall performance.

🎯 Objectives
Analyze overall trading performance using Win Rate and PnL
Identify profitable coins and trading patterns
Study impact of market classification (sentiment)
Evaluate risk levels and their effect on returns
Build an interactive dashboard for decision-making

📂 Dataset Description

The dataset contains trade-level information including:

Coin – Asset traded (e.g., BTC, ETH)
Execution Price – Entry price of trade
Size (USD / Tokens) – Trade volume
Side – Buy or Sell
Closed PnL – Profit or loss from trade
win – TRUE/FALSE outcome
Classification – Market sentiment / trade category
risk_group – Risk level of trade
Timestamp / Date – Trade time
Trade ID / Order ID – Unique identifiers

🧹 Data Processing
Converted Boolean win (TRUE/FALSE) into numeric Win Flag (1/0)
Created calculated measures using DAX
Cleaned and structured dataset in Power BI
Ensured correct formatting for KPIs and visuals

📐 Key Measures (DAX)
Win Flag = IF('merged'[win] = TRUE(), 1, 0)

Win Rate = DIVIDE(SUM('merged'[Win Flag]), COUNTROWS('merged'))

Total Trades = COUNTROWS('merged')

Total Wins = SUM('merged'[Win Flag])

Total Losses = COUNTROWS('merged') - SUM('merged'[Win Flag])

📊 Dashboard Visuals

The Power BI dashboard includes:

📊 KPI Cards (Win Rate, Trades, Wins, Losses)
🍩 Donut Chart (Win vs Loss Distribution)
🍩 Pie Chart (Classification Breakdown)
📊 Column Charts (Coin vs Performance)
📈 Line Chart (Trend Analysis over time)
📊 Bar Chart (Risk Group Analysis)

🔍 Key Insights
Win Rate helps evaluate trading efficiency
Certain coins show higher profitability than others
Classification impacts trading success significantly
Risk groups influence volatility and returns
Scatter plot reveals trade efficiency patterns across price levels

📌 Tools Used
Power BI
DAX (Data Analysis Expressions)
Excel / CSV Dataset

🚀 Conclusion

This project demonstrates how data visualization can be used to analyze trading performance and market behavior. It provides actionable insights for improving trading strategies and understanding risk vs reward patterns.
