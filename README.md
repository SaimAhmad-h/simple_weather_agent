## 📓 View Full Notebook
👉 [Click here to view the complete notebook](https://colab.research.google.com/drive/1WNW1PveTpn0XrW_pZgaixDHMwKvzaYma?usp=sharing)


# 🌦️ Simple Weather AI Agent

## 🚀 Overview

Simple Weather AI Agent is a Python-based AI application that combines a Large Language Model (LLM) with a weather API to answer weather-related questions in natural language.

The project uses the Groq API and the LLaMA 3.1 (8B Instant) model to understand user queries, determine when weather information is required, call an external weather tool, and generate a final response based on real-time weather data.

This project demonstrates the fundamentals of AI agents, tool calling, and LLM integration with external APIs.

---

## ✨ Features

* 🌦️ Real-time weather information retrieval
* 🤖 LLM-powered query understanding
* 🛠️ Tool-calling architecture
* 📍 Location-based weather lookup
* ⚡ Groq-powered inference using LLaMA 3.1 (8B)
* 🔄 Plan → Action → Observe → Output workflow
* 🛡️ Robust API error handling
* 🐍 Beginner-friendly Python implementation

---

## 🛠️ Technologies Used

* Python
* Groq API
* LLaMA 3.1 8B Instant
* WeatherAPI
* Requests
* JSON

---

## 🧠 Agent Workflow

The agent follows a structured reasoning process:

User Query
↓
Plan
↓
Action (Tool Call)
↓
Observe
↓
Final Output

### Step 1: User Query

The user asks a weather-related question.

Example:

What is the weather in Lahore today?

### Step 2: Planning

The LLM analyzes the request and determines the required action.

Example:

{
"step": "plan",
"content": "The user is interested in weather information for Lahore."
}

### Step 3: Action

The LLM selects the appropriate tool and executes it.

Example:

{
"step": "action",
"function": "get_weather",
"input": "Lahore"
}

### Step 4: Observation

The weather tool returns the result.

Example:

{
"step": "observe",
"output": "34°C, Partly Cloudy"
}

### Step 5: Final Response

The LLM generates a natural language answer.

Example:

The current weather in Lahore is 34°C with partly cloudy conditions.

---



#### 1. LLM Module

Responsible for:

* Understanding user requests
* Generating plans
* Selecting tools
* Producing final responses

#### 2. Weather Tool

Responsible for:

* Calling WeatherAPI
* Fetching current weather data
* Returning structured weather information

#### 3. Agent Loop

Responsible for:

* Processing planning steps
* Executing actions
* Handling observations
* Producing final output

---

## 💬 Example Queries

* What is the weather in Lahore?
* Tell me the weather in Islamabad.
* Is it raining in Karachi?
* How hot is Faisalabad today?
* What is the current weather in New York?

---

## 🛡️ Error Handling

The weather tool includes robust exception handling for:

* Request timeouts
* Connection failures
* HTTP errors
* Invalid API responses
* Unexpected runtime errors

Example responses:

* Weather data unavailable (timeout error)
* Weather data unavailable (connection error)
* Weather data unavailable (HTTP error)

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone <repository-url>
cd weather-agent
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure API Keys

Add your API keys inside the code:

```python
client = Groq(
    api_key="YOUR_GROQ_API_KEY"
)
```

```python
api_key = "YOUR_WEATHERAPI_KEY"
```

### 4. Run the Project

```bash
python main.py
```

---

## 📌 Current Scope

Currently supported:

* Current weather lookup
* City-based weather retrieval
* Natural language weather queries
* Single-tool AI agent workflow

---

## ⚠️ Limitations

* Requires internet connectivity
* Depends on external APIs
* Supports weather functionality only
* Accuracy depends on API availability and data quality

---

## 🔮 Future Improvements

Potential enhancements include:

* Weather forecast support
* Search tool integration
* Calculator tool integration
* Multi-tool agents
* Conversation memory
* Voice interaction
* Web interface
* Streamlit dashboard
* Multi-city comparisons

---

## 🎯 Learning Objectives

This project helps beginners understand:

* LLM API integration
* Tool calling concepts
* AI agent fundamentals
* Weather API usage
* Prompt engineering
* Structured JSON outputs
* External API integration
* Agent execution loops

---

## 📜 License

This project is intended for educational and learning purposes.

---

## ⭐ Conclusion

Simple Weather AI Agent demonstrates how a Large Language Model can interact with external tools to access real-time information. The project provides a beginner-friendly introduction to AI agents, tool calling, and API-integrated LLM applications using Python, Groq, and WeatherAPI.

## 📓 Notebook

View the project notebook:

https://colab.research.google.com/drive/1WNW1PveTpn0XrW_pZgaixDHMwKvzaYma?usp=sharing

---

## 📜 License

This project is intended for educational and learning purposes.

---

## ⭐ Conclusion

Simple Weather AI Agent demonstrates how a Large Language Model can work together with an external API to provide real-time information through natural language interactions. It serves as a beginner-friendly introduction to tool-augmented AI applications and AI agent fundamentals.

