# 🤖 Smart Agent (Console Version)

This repository contains a terminal-based conversational agent designed to handle queries. The project demonstrates how to configure **OpenAI's official Agents SDK** to run on top of Google's **Gemini 2.0 Flash model** using OpenAI-compatible base URL routing. It also enforces custom behavioral guardrails for greetings and farewells.

---

## ⚙️ Project Architecture & Workflow

The script operates through four main steps behind the scenes:
1. **Environment Loading:** It safely retrieves the Gemini API key from a local `.env` file.
2. **Provider Bridging:** It initializes an asynchronous OpenAI client but routes its base URL directly to Google's generative language endpoint.
3. **Behavior Modeling:** It defines an explicit `Agent` instance containing structural rules that override standard model outputs for specific phrases.
4. **Synchronous Execution:** It captures local console inputs using a standard Python hook and pipes them through the SDK's execution runner.

---

## 📥 Local Setup & Installation

Follow these steps to configure the environment and test the agent locally on your machine:

### 1. Clone the repository and enter your project folder
git clone https://github.com/HibaDawood/SDK-Agent && cd https://github.com/HibaDawood/SDK-Agent

### 2. Install the required SDK dependencies
pip install openai-agents python-dotenv

### 3. Run the terminal application
python main.py
