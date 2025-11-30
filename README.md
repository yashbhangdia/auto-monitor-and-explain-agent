# Auto-Monitor & Explain: AI Agent for Real-Time Market Intelligence

## 🚀 Overview

An AI-powered autonomous market monitoring agent built using **Google
Agent Development Kit (ADK)** and **Gemini** that continuously tracks
real-time stock prices, detects abnormal movements, and generates
human-readable explanations using live market data and news tools.

------------------------------------------------------------------------

## 🎯 Problem Statement

Manual tracking of live stock movements and identifying the reasons
behind sudden price changes is inefficient, time-consuming, and
error-prone for individual investors and analysts.

------------------------------------------------------------------------

## ✅ Solution

A real-time autonomous AI agent that: - Fetches live stock prices using
Alpha Vantage API - Detects abnormal price movements - Automatically
explains market movements using Gemini and live context - Operates
continuously using loop agents and async execution

------------------------------------------------------------------------

## 🧠 Key Features

-   Real-time price tracking
-   Threshold-based market movement detection
-   Automated AI-generated explanations
-   Tool-based reasoning (no hallucinations)
-   Multi-agent orchestration using Google ADK
-   Session & state management
-   Fully asynchronous execution

------------------------------------------------------------------------

## 🏗 Architecture

Watchlist → Loop Agent → Price Fetch Tool → Movement Detection → Gemini
LLM → Explanation Output

------------------------------------------------------------------------

## 🛠 Tech Stack

-   Python 3.11+
-   Google ADK
-   Gemini 2.x
-   Alpha Vantage API
-   AsyncIO

------------------------------------------------------------------------

## ⚙️ Setup Instructions

``` bash
git clone https://github.com/your-repo/market-agent.git
cd market-agent
pip install -r requirements.txt
export ALPHAVANTAGE_API_KEY="your_api_key"
python runner.py
```

------------------------------------------------------------------------

## 📊 Sample Output

    AAPL moved +1.82% in last 5 minutes.
    Reason: Increased buying activity driven by Nasdaq rally.
    Confidence: 0.87

------------------------------------------------------------------------

## 🔐 Security

-   No hardcoded API keys
-   All secrets loaded via environment variables

------------------------------------------------------------------------

## 🧾 Concepts Demonstrated

-   LLM-powered agents (Gemini)
-   Loop and Sequential Agents
-   Custom Tools
-   Long-running asynchronous agents
-   Session & Memory Management
-   Observability through logs

------------------------------------------------------------------------

## 🔮 Future Enhancements

-   Crypto & Forex monitoring
-   Alert notifications
-   Portfolio risk scoring
-   Deployment on cloud

------------------------------------------------------------------------

## 👨‍💻 Author

@yashbhangdia
