# Python
Google Collab - AI

# 🤖 Gemini-Powered Data Analysis Agent (Python & LangChain)

## Overview
This project demonstrates the creation of a robust AI agent capable of performing complex data analysis on a local Pandas DataFrame (`sales_data.csv`) using natural language queries. The agent uses Google's **Gemini 2.5 Flash** model to generate and execute safe, accurate Python code, effectively turning the LLM into a powerful data analyst.

The project explores two key architectural approaches: a manual system built with the official Google GenAI SDK and an abstracted system using LangChain.

## ✨ Features

* **Natural Language Querying:** Ask complex data questions (e.g., "What is the total revenue for Electronics?") and receive direct answers.
* **Code Generation & Execution:** The Gemini model generates the necessary Pandas code (`df.groupby().sum()`), and the agent securely executes it locally.
* **Two Implementation Methods:**
    1.  **Official SDK/Manual Tooling:** Shows mastery of direct API function calling (`google-genai`).
    2.  **LangChain Integration:** Utilizes the `create_pandas_dataframe_agent` for rapid development and abstraction.
* **Interactive CLI:** Implemented a continuous chat loop using `input()` for multi-question analysis.

## ⚙️ Technologies Used

* **Model:** Google Gemini 2.5 Flash
* **Core Libraries:** Python, Pandas
* **Frameworks & SDKs:**
    * `google-genai` (Official Google SDK)
    * `langchain` / `langchain-google-genai`
    * `langchain-experimental` (for the DataFrame Agent)

## 🚀 Setup and Installation

### 1. Prerequisites

* Python 3.9+
* A **Gemini API Key** (Set as an environment variable or in Colab Secrets).
* Your data file (assumed to be `sales_data.csv`).

### 2. Install Dependencies

```bash
pip install -U google-genai pandas langchain langchain-google-genai langchain-experimental

✅ Agent ready. Type 'exit' or 'quit' to end the session.
------------------------------
❓ Your Data Question: List the total revenue broken down by category - Electronics.

> Entering new AgentExecutor chain...
Action: python_repl_ast
Action Input: print(df[df['category'] == 'Electronics']['total_price'].sum())
...
💡 Agent Answer: The total revenue for the 'Electronics' category is 1814.86.
------------------------------
❓ Your Data Question: 
