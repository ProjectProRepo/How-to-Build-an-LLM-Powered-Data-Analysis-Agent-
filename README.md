# LLM-Powered Data Analysis Agent

This repository showcases the creation of an LLM-Powered Data Analysis Agent, leveraging powerful tools such as LangChain, Groq, Llama 3, and Exa for efficient data handling and analysis. It provides a framework for analyzing cryptocurrencies. A user can ask for a cryptocurrency report, which triggers an agent to gather relevant news, another agent to analyze prices, and then a final report summarizing the market and making predictions.

## Key Features

- **LangChain Integration** for managing LLM-powered workflows.
- **Custom cryptocurrency price tool** to fetch historical prices.
- **News tool** to get real-time cryptocurrency news.
- **LLM-powered Agents** for tasks like price analysis, news analysis, and report writing.
- **Use of Groq** for optimized inference with Llama 3 models.
- **Agent-based architecture** enabling task delegation and collaboration.
- **Customer Communicator Agent** for interactive cryptocurrency inquiries.
- **News Analyst Agent** for market trend analysis based on news.
- **Price Analyst Agent** for market analysis based on historical prices.
- **Report Writer Agent** that synthesizes analyses into a final report.

## Overview

This repository contains an LLM-powered data analysis agent designed to handle cryptocurrency analysis using multiple tools and agents. The system is built around various components that work together to gather, analyze, and report on cryptocurrency news and price trends. Below is an overview of the key elements that drive the data analysis pipeline.

## Tools

### Search Tool (Exa API)
- **Purpose:** Used to search for and summarize the latest cryptocurrency news.
- **Usage:** The tool fetches relevant news based on a given query, processes the results, and returns a summary with relevant details.
- **API:** [Exa API Key](https://dashboard.exa.ai/api-keys)


### Cryptocurrency Price Tool
- **Purpose:** Retrieves the daily closing prices for a given cryptocurrency symbol for the last 60 days.
- **Usage:** This tool is critical for gathering historical price data to analyze trends and market predictions.

### Search Tool (Cryptocurrency News)
- **Purpose:** A variant of the search tool that specifically looks for cryptocurrency-related news.
- **Usage:** This tool integrates with the Exa tool to search for cryptocurrency news articles and prepare summaries for analysis.

### Groq for Inference
- **Purpose:** Uses the Llama 3 model in combination with Groq for enhanced inference and processing.
- **Usage:** Efficient model inference is achieved using Groq to process and analyze queries related to cryptocurrency trends.

## Agents

### Customer Communicator
- **Role:** Senior cryptocurrency customer communicator.
- **Goal:** Identify which cryptocurrency the customer is interested in for further research and analysis.
- **Tools:** Uses the search tool to gather data from various sources.

### Cryptocurrency News Analyst
- **Role:** Analyze the latest news related to cryptocurrency trends.
- **Goal:** Write a short analysis based on recent news and make a prediction about market trends (up, down, or neutral).
- **Tools:** Uses the cryptocurrency news tool to fetch articles and summarize them.

### Cryptocurrency Price Analyst
- **Role:** Analyze historical price trends of cryptocurrency.
- **Goal:** Produce a report with predictions based on price history, focusing on technical analysis.
- **Tools:** Uses the cryptocurrency price tool to gather historical data and analyze trends.

### Cryptocurrency Report Writer
- **Role:** Compile analysis from the news and price analysts into a final report.
- **Goal:** Write a comprehensive report summarizing the market trends and predictions.
- **Tools:** Uses the outputs from the news and price analysis agents to compose the final report.

## Tasks

### Get Cryptocurrency Interest:
- **Description:** The customer communicator agent asks the user which cryptocurrency they are interested in researching.
- **Expected Output:** The cryptocurrency symbol (e.g., BTC).

### Get News Analysis:
- **Description:** The news analyst uses the search tool to gather news for the selected cryptocurrency and creates a summary along with a market prediction.
- **Expected Output:** A one-paragraph report predicting market trends based on news.

### Get Price Analysis:
- **Description:** The price analyst uses the price tool to retrieve historical data for the selected cryptocurrency and provides an analysis along with a market prediction.
- **Expected Output:** A one-paragraph report predicting future trends based on price data.

### Write Final Report:
- **Description:** Combines the outputs from both the news and price analysts to create a final report summarizing market trends and predictions.
- **Expected Output:** A comprehensive one-paragraph report summarizing the market and making a prediction about the cryptocurrency's future.

## Example Workflow

1. **Get Cryptocurrency Interest:** The customer specifies which cryptocurrency they want to explore (e.g., BTC).
2. **Get News Analysis:** The news analyst searches for and analyzes the latest news related to the chosen cryptocurrency.
3. **Get Price Analysis:** The price analyst retrieves and analyzes historical data for the cryptocurrency.
4. **Write Final Report:** The report writer combines the findings from the news and price analysis into a final report.

## Getting Started

To get started with the LLM-Powered Data Analysis Agent, you'll need to sign up for and obtain the following API keys, which are essential for the tools and agents involved:

1. **GROQ API Key**  
   Sign up at [GROQ Console](https://console.groq.com/keys) to get your API key.  
   This key is required to interact with the Groq API, used for managing and processing data in the analysis pipeline.

2. **Exa API Key**  
   Sign up at [Exa Dashboard](https://dashboard.exa.ai/api-keys) to obtain your API key.  
   This key allows integration with the Exa Search and Content Extraction Tool, which aids in gathering relevant data and news articles based on specific queries.

3. **Alpha Advantage API Key**  
   Sign up at [Alpha Advantage](https://www.alphavantage.co/support/#api-key) to acquire your API key.  
   This key is needed for financial data analysis and integration with the Alpha Advantage API, offering real-time stock market data, technical indicators, and more.

Once you have the three API keys, you can add them to the IPython notebook of this repository and start running the code in a Google Colab notebook. Happy Coding! :)

## Resources

For a detailed description of this code, check out ProjectPro’s blog: [LLM Data Analysis Agent](https://www.projectpro.io/article/llm-data-analysis-agent/1093)

## Special Thanks

We would like to extend our heartfelt thanks to the following organizations for their invaluable contributions:

- **[Alpha Vantage](https://www.alphavantage.co/)** for providing high-quality financial data and APIs, which power the cryptocurrency analysis in this project.  
- **[Groq](https://console.groq.com/)** for enabling high-performance AI model inference with their advanced hardware and API capabilities.  
- **[crewAI-tools](https://github.com/crewAIInc/crewAI-tools/tree/main/crewai_tools/tools/exa_tools)** for the Exa Tools integration, which powers real-time search and content analysis in our solution.  


Thank you for your contribution to the AI community!
