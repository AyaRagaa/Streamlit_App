# 🤖 LangGraph Agent with Streamlit (Groq)

This project is a conversational **LangGraph-powered agent** with a **Streamlit** interface.  
It integrates **Groq LLMs**, **RAG (Retrieval-Augmented Generation)**, and **tool-augmented reasoning**, allowing the agent to answer user queries using:

- 🔢 Built-in math tools (add, subtract, multiply, divide)
- 🌍 Web search (DuckDuckGo)
- 📚 Retrieval from a local knowledge base (`knowledge.txt`)

The frontend is built with **Streamlit** for an interactive chat UI.

---

## 🚀 Features
- **LangGraph-based Agent**: Graph-driven reasoning with state management.
- **Retrieval-Augmented Generation (RAG)**: Uses FAISS + HuggingFace embeddings (`all-MiniLM-L6-v2`) to fetch knowledge from `knowledge.txt`.
- **Tool Support**:
  - Arithmetic operations (add, subtract, multiply, divide)
  - Web search using DuckDuckGo
  - Local knowledge search
- **Groq-Powered LLM**: Uses `ChatGroq` with model `openai/gpt-oss-120b`.
- **Streamlit UI**: Clean chat-like interface for user interaction.

---

## 📂 Project Structure
- agent.py # Core LangGraph agent logic (tools, RAG, Groq integration)
- app.py # Streamlit UI for chatting with the agent
- knowledge.txt # Local knowledge base (optional)
- system_prompt.txt # Custom system prompt for guiding the agent
- requirements.txt # Python dependencies
- README.md # Project documentation


---

## ⚙️ Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/AyaRagaa/Streamlit_App.git
   cd Streamlit_App
   ```


2. **Create a Virtual Environment (recommended)**
  ```bash
  python -m venv venv
  source venv/bin/activate   # Mac/Linux
  venv\Scripts\activate      # Windows
  ```

3. **Install Dependencies**
  ```bash
  pip install -r requirements.txt
  ```

---

## 🏃 Usage

- Make sure you have a Groq API key in your .env file:

  ```bash
  GROQ_API_KEY=your_api_key_here
  ```


- Add any knowledge to knowledge.txt (optional).

- Run the Streamlit app:

  ```bash
  streamlit run app.py
  ```


---

## ✨ Example Tools

### Math Tool

  ```bash
  User: add 10 and 5  
  Agent: 15
  ```


### Web Search

  ```bash
  User: latest AI news  
  Agent: [retrieves top results from DuckDuckGo]
  ```


### RAG Search

  ```bash
  User: How old is Aya?  
  Agent: [retrieved answer from knowledge.txt]
  ```

---

## 📜 Requirements

The main dependencies are:

- streamlit
- langgraph
- langchain
- langchain_groq
- langchain_community
- duckduckgo-search
- faiss-cpu
- sentence-transformers
- python-dotenv





