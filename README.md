📊 Real-Time Sentiment-Integrated LSTM Framework for Adaptive Trading Signal Generation

This repository contains my research work on building a real-time, sentiment-aware algorithmic trading framework that integrates multi-source news sentiment analysis, technical indicators, and LSTM-based volatility forecasting to generate context-aware trading signals.

The objective of this research is to bridge the gap between isolated sentiment analysis and actionable trading strategy generation by designing an end-to-end, production-oriented system capable of operating reliably under real-world data constraints.

📄 Research Overview

Title: Real-Time Sentiment-Integrated LSTM Framework for Adaptive Trading Signal Generation
Author: Abhijith E
Affiliation: Department of Computer Science, CHRIST (Deemed to be University), Bengaluru, India

In this research, I propose a unified framework that combines alternative data (news sentiment) with deep learning models and technical indicators to identify market regimes and recommend appropriate trading strategies ranging from aggressive volatility plays to conservative income-based approaches.

🎯 Key Objectives

Integrate real-time news sentiment into quantitative trading models

Predict future market volatility using LSTM neural networks

Generate adaptive trading strategies based on market regime identification

Ensure robustness and resilience through API fallback mechanisms

Design a system suitable for real-time market monitoring

🚀 Key Contributions

Multi-Source Sentiment Aggregation

Real-time news ingestion from Alpha Vantage, Financial Modeling Prep, and NewsAPI

RSS feed and synthetic headline fallback mechanisms for uninterrupted operation

Sentiment Analysis Pipeline

VADER-based sentiment scoring optimized for short-form financial news

Daily sentiment aggregation aligned with market data

LSTM-Based Volatility Forecasting

Two-layer LSTM architecture using a 20-day rolling window

Predicts one-step-ahead market volatility using combined technical and sentiment features

Multi-Factor Trading Strategy Engine

Combines volatility regime, RSI momentum, and sentiment signals

Generates differentiated trading strategies (directional, volatility, income-based)

Production-Oriented System Design

Graceful degradation across multiple data tiers

Robust error handling and real-time processing considerations

🧠 System Architecture Overview
1️⃣ Data Acquisition Layer

Historical price data from yFinance

News sentiment from:

Alpha Vantage (primary)

Financial Modeling Prep

NewsAPI

RSS feeds (Reuters, CNN Money)

Synthetic fallback headlines (for resilience)

2️⃣ Sentiment Analysis Pipeline

Headline extraction and timestamp normalization

Sentiment scoring using VADER

Daily aggregation to reduce intraday noise

3️⃣ Technical Indicator Computation

Log returns

Annualized volatility

Relative Strength Index (RSI)

20-day and 50-day Simple Moving Averages (SMA)

4️⃣ LSTM-Based Prediction Model

Input features:

Log returns

Current volatility

Sentiment score

SMA (20, 50)

RSI

Two stacked LSTM layers with dropout regularization

Mean Squared Error loss optimized using Adam

5️⃣ Trading Strategy Decision Engine

Identifies:

Volatility regimes

Momentum regimes

Sentiment regimes

Maps regime combinations to nine trading strategies, including:

Strong Buy/Sell

Volatility straddles

Covered calls

Credit spreads

Wait signals

📊 Experimental Evaluation
🔬 Evaluation Setup

Stocks Analyzed: 10 major US equities (AAPL, MSFT, GOOGL, AMZN, TSLA, META, NVDA, JPM, JNJ, XOM)

News Volume: 20–70 articles per stock

Prediction Target: One-step-ahead volatility

📈 Key Results

Volatility prediction MAE ranged from 0.0233 to 0.0722

Successfully identified market regimes across multiple stocks

Strategy distribution favored:

Income strategies

Volatility plays

Conservative wait signals during uncertainty

🧠 Observations

Positive sentiment aligned strongly with bullish income strategies

High volatility regimes triggered straddle and hedging strategies

Neutral sentiment favored income-based options strategies

🛠️ Technologies Used

Python

TensorFlow / Keras

NumPy

Pandas

Scikit-learn

yFinance

VADER Sentiment Analyzer

Matplotlib / Seaborn

⚠️ Limitations

Backtesting does not include transaction costs or slippage

LSTM trained on limited historical sequences

VADER sentiment may miss context-specific financial language

No explicit portfolio-level risk management implemented

🔮 Future Work

In future extensions of this research, I plan to:

Integrate transformer-based sentiment models (BERT, FinBERT)

Add portfolio-level optimization and position sizing

Include social media and earnings call sentiment

Perform long-horizon backtesting with realistic execution costs

Extend the system to multi-asset portfolio decision-making

📌 Citation

If you use or build upon this work, please cite:

Abhijith E,
"Real-Time Sentiment-Integrated LSTM Framework for Adaptive Trading Signal Generation",
Department of Computer Science, CHRIST (Deemed to be University), Bengaluru.

👤 Author

Abhijith E
M.Sc. Artificial Intelligence and Machine Learning
CHRIST (Deemed to be University), Bengaluru
📧 abhijith.e@msam.christuniversity.in
