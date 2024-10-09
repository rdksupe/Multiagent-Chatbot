# Multiagent Chatbot with Tool-Using Capabilities

## Overview

This repository contains a multiagent chatbot system built with LangGraph and LangChain. The system uses various language models to create an agent that can use tools to perform web searches, scrape websites, interact with LinkedIn profiles, and more.

## Features

- **Tool-equipped AI agents**: The chatbot can use various tools to enhance its capabilities:
  - Web search (via Google Search API)
  - Web scraping
  - LinkedIn profile fetching
  - LinkedIn posting
  - Human interaction

- **Multiple LLM Support**: The system is designed to work with multiple language models:
  - Ollama (local models like Hermes)
  - Anthropic Claude
  - Google Gemini
  - Mistral AI
  - Groq
  - Fireworks AI
  - Cohere

- **Memory Integration**: Includes infrastructure for memory (currently commented out) using Mem0 for persistent chat history.

## How It Works

The system uses LangGraph to create a workflow where:

1. User queries are processed by the language model
2. The model can decide to use tools when needed
3. Tool results are fed back to the model for final responses
4. The entire conversation flow is managed via a state graph

## Getting Started

### Prerequisites

- Python 3.10+
- API keys for various services (placed in a `.env` file):
  - Google Search API
  - Mem0
  - LangChain
  - Various LLM providers

### Installation

1. Clone this repository
```bash
git clone https://github.com/yourusername/Multiagent-Chatbot.git
cd Multiagent-Chatbot
```

2. Install dependencies
```bash
pip install langchain langgraph langchain-anthropic langchain-cohere langchain-google-community langchain-together langchain-groq langchain-mistralai langchain-fireworks langchain-google-genai langchain-ollama mem0 linkedin-api
```

3. Create `.env` file with your API keys

### Usage

Open the `pipe.ipynb` notebook in Jupyter or your preferred notebook environment:

```bash
jupyter notebook pipe.ipynb
```

The notebook contains cells that:
1. Import necessary libraries and set up credentials
2. Define tool functions
3. Configure language models
4. Set up the agent workflow
5. Provide an interface for chatting with the agent

## Example Usage

The notebook includes an example where the agent searches for current news. You can modify the input in the streaming cell to ask different questions.

## Customizing the Agent

You can customize the agent by:
- Changing the language model (uncomment different model initialization)
- Adding new tools (create new functions with the `@tool` decorator)
- Modifying the system prompts
- Adjusting the workflow graph

## License

This project is meant for educational and research purposes.

## Acknowledgements

- LangChain and LangGraph teams
- The open-source LLM community