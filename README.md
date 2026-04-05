Simple Weather AI Agent

This project implements a lightweight AI agent capable of handling user queries by combining reasoning with tool usage. It is built using the Groq API and powered by the LLaMA 3.1 8B model.

Unlike traditional chatbots, this agent follows a structured decision-making loop to intelligently process queries and retrieve real-world data when required.

🧠 Agent Workflow

The system is based on a Plan → Action → Observe → Output paradigm:

Plan
The agent analyzes the user query and determines what needs to be done (e.g., whether external data is required).
Action
It decides which tool to use (such as a weather API) and executes the required function call.
Observe
The agent collects and interprets the response returned by the tool.
Output
Finally, it generates a natural language response combining reasoning + real-time data.
⚙️ Key Capabilities
Integrates LLM reasoning with external tools
Fetches real-time weather data via APIs
Handles flexible, natural language queries
Demonstrates agentic AI behavior (decision-making + execution)
Modular design for adding more tools (e.g., search, calculator, file system)
🛠️ Tech Stack
Language: Python
LLM API: Groq
Model: LLaMA 3.1 (8B)
Architecture: Tool-augmented AI agent (ReAct-style workflow)
