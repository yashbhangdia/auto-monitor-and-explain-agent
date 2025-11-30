# **Auto-Monitor & Explain: AI Agent for Real-Time Market Intelligence**


### Problem Statement

Monitoring financial markets in real-time is an essential task for traders, analysts, and students of finance. However, tracking multiple stock tickers and understanding the reasons behind sudden price movements is a time-consuming, error-prone, and cognitively intensive process. Existing solutions either provide raw numerical data without context or delayed insights, which limits the ability of users to make timely, informed decisions. This gap creates a clear need for a system that can autonomously monitor market movements and provide **actionable, data-driven explanations** in real-time.

Our project addresses this problem by leveraging **multi-agent AI systems** powered by the **Google Agent Development Kit (ADK)** and **Gemini 2.x**. The system continuously monitors stock prices, detects significant movements, and explains the observed changes by analyzing contextual information from external tools, including news and search APIs. The result is a fully autonomous, **loop-driven agent** that functions as a personal financial analyst capable of delivering timely, human-readable insights.

---

### Why agents?

Agents are particularly suitable for this problem because they are capable of **autonomous decision-making, asynchronous operation, and continuous monitoring**. Instead of relying on a static script that fetches data once or requires human supervision, agents can operate in loops, maintain state, and invoke reasoning workflows based on conditions, such as a sudden price change. Specifically:

* **Loop Agents:** Continuously poll multiple tickers for price changes without human intervention.
* **Sequential Agents:** Orchestrate the workflow from price fetching → movement detection → explanation generation.
* **Tool-Powered Agents:** Ground their reasoning in structured data, preventing hallucinations and ensuring reliability.
* **Session & Memory:** Maintain context across time, remembering prior checks and previous outputs to avoid redundant processing.

This agent-driven architecture ensures that the system is **scalable, real-time, and reliable**, making it suitable for monitoring multiple stocks simultaneously and providing actionable insights in near real-time.

---

### What I've created 

The project is a **multi-agent system** integrating live price fetching, threshold-based movement detection, and reasoning with the Gemini LLM. The high-level workflow is as follows:

1. **Watchlist Input:** Users define stock tickers they want to monitor.
2. **Loop Agent (ADK):** Runs continuously, polling the watchlist at a set interval (e.g., every minute).
3. **Price Fetch Tool:** Retrieves intraday stock prices from Alpha Vantage. The tool ensures the agent always works with fresh, reliable data.
4. **Movement Detection Logic:** Compares current price with recent historical data. When price movement exceeds a threshold, the system triggers reasoning.
5. **Gemini LLM Agent:** Generates concise, data-backed explanations using external context from Google Search or News tools.
6. **Output Logging & Session Management:** Stores results, maintains continuity, and logs insights with timestamps and confidence scores.

**Architecture Diagram:**

```
Watchlist → Loop Agent → Price Fetch Tool → Movement Detection → Gemini LLM → Explanation Output
```

This modular design makes the system extensible, allowing additional tools, markets, or technical indicators to be integrated seamlessly in the future.

---

### Technical Implementation

**Languages & Frameworks:**

* Python 3.11+
* Google ADK for agent orchestration
* Gemini 2.x LLM for reasoning

**APIs & Tools:**

* Alpha Vantage for real-time intraday prices
* Google Search and News tools for contextual explanations
* AsyncIO for non-blocking, continuous execution

**Key Implementation Highlights:**

* **Loop & Sequential Agents:** Continuously monitor stocks and trigger reasoning workflows based on price changes.
* **Custom Tools:** Alpha Vantage price fetcher and movement detection logic to provide structured input to Gemini.
* **Session & State Management:** Using ADK’s InMemorySessionService, the agent keeps track of previously observed prices and avoids redundant calculations.
* **Observability:** Structured logging captures key events, results, and confidence levels for easy debugging and analysis.
* **Error Handling & Rate Limit Management:** The agent gracefully handles API errors, missing data, and adheres to Alpha Vantage’s free-tier rate limits (5 requests per minute).

**Execution Flow:**

1. Fetch latest price for each ticker.
2. Compute percentage change over a configurable window (e.g., last 5 minutes).
3. If threshold exceeded, trigger Gemini agent to generate explanation.
4. Combine external context from news and search tools.
5. Log the explanation and confidence score.

The system is fully **asynchronous**, allowing multiple tickers to be monitored simultaneously without blocking execution.

---

### Demo

The agent produces actionable outputs such as:

```
AAPL moved +1.82% in the last 5 minutes.
Reason: Increased buying activity driven by Nasdaq rally and positive earnings sentiment.
Confidence: 0.87
```

Users receive real-time explanations grounded in market data and news, enabling them to make informed decisions quickly. This demonstrates the practical utility of multi-agent systems in **real-time data monitoring and contextual reasoning**.

---

### Innovation & Impact

The project demonstrates **innovative use of AI agents** in finance:

* **Autonomous monitoring** reduces manual labor and error.
* **Tool-grounded reasoning** ensures accurate, reliable explanations.
* **Loop & sequential agent orchestration** simulates a human analyst in continuous operation.
* **Session management** ensures the agent is aware of prior state, improving reliability and context understanding.

This combination of real-time monitoring, reasoning, and tool integration highlights the **value of agent-based automation** for financial analysis, making this approach highly relevant for students, retail investors, and analysts.

---

### Future Enhancements

With additional time or resources, the system could be expanded to:

* Monitor **crypto, forex, and commodities** alongside stocks.
* Provide **portfolio-level risk analysis** and aggregated market insights.
* Send **alerts via email, SMS, or messaging apps** when significant movements occur.
* Incorporate **technical indicators and sentiment scoring** for richer analysis.
* Deploy on the **cloud for continuous, 24/7 operation**.

These enhancements would make the system even more valuable, turning it into a fully-fledged autonomous market intelligence platform.

---

### Conclusion

The Auto-Monitor & Explain Agent is a **practical demonstration of how AI agents can automate complex, repetitive tasks** while providing meaningful, human-readable insights. By integrating **real-time price fetching, threshold detection, tool-based reasoning, and LLM explanations**, this project bridges the gap between **raw financial data and actionable intelligence**.

It showcases **innovation, practical utility, and extensibility**, demonstrating how multi-agent systems can solve real-world problems that are traditionally labor-intensive and cognitively demanding.


------------------------------------------------------------------------

## ⚙️ Setup Instructions

1. Clone the repository.
2. Get the ipynb notebook file and upload to kaggle notebooks.
3. Add two secrets under "Add-ons" tab. [GOOGLE_API_KEY, AV_API_KEY]
4. Run the cells of the notebook.

------------------------------------------------------------------------

