# 🚀 LangGraph Multi-Utility AI Chatbot (RAG + Tools)

An advanced AI chatbot built using **LangGraph**, **Gemini**, and **Retrieval-Augmented Generation (RAG)** that can:

✅ Answer questions from uploaded PDFs  
✅ Use real-time web search  
✅ Fetch live stock prices  
✅ Perform calculations  
✅ Maintain conversation memory per thread  
✅ Stream responses in real-time  

This project demonstrates production-style AI system design with tool orchestration, vector search, and persistent chat state.

---

## 🔥 Features

### 📄 PDF Intelligence (RAG)
- Upload a PDF and instantly chat with it.
- Documents are chunked and embedded using **Gemini embeddings**.
- Stored in a **FAISS vector database** for fast retrieval.

### 🧠 LangGraph Agent Architecture
- Graph-based execution instead of linear chains.
- Tool routing handled automatically by the LLM.
- Persistent conversation state using SQLite checkpointing.

### 🛠️ Tool Calling
The assistant can dynamically decide when to use tools:

- 🌐 DuckDuckGo web search  
- 📈 Live stock price API  
- ➗ Calculator  
- 📚 PDF retrieval tool  

### 💬 Multi-Thread Conversations
Each chat session has:

- Independent memory  
- Separate vector store  
- Isolated document context  

### ⚡ Streaming Responses
Real-time token streaming for a smoother chat experience.

---

## 🧱 Tech Stack

- **LLM:** Google Gemini (Flash)
- **Embeddings:** `gemini-embedding-001`
- **Agent Framework:** LangGraph
- **Vector DB:** FAISS
- **Frontend:** Streamlit
- **State Persistence:** SQLite
- **Tools:** LangChain Community Tools

---

## 🏗️ Architecture Overview

```
User → Streamlit UI  
      ↓  
LangGraph Agent  
      ↓  
Decision Layer → (LLM decides)  
      ├── Web Search  
      ├── Calculator  
      ├── Stock API  
      └── PDF Retriever (FAISS)  
```

---

## ⚙️ Installation

### 1️⃣ Clone the repo

```bash
git clone https://github.com/your_username/langgraph_chatbot.git
cd langgraph_chatbot
```

---

### 2️⃣ Create virtual environment

```bash
python -m venv venv
source venv/bin/activate
```

---

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Add Environment Variables

Create a `.env` file:

```
GOOGLE_API_KEY=your_google_api_key
LANGCHAIN_API_KEY=your_langsmith_key   # optional (for tracing)
```

---

## ▶️ Run the App

```bash
streamlit run app.py
```

Upload a PDF and start chatting 🚀

---

## 📊 Why This Project Matters

This is NOT a basic chatbot.

It demonstrates real-world AI engineering patterns:

✅ Retrieval-Augmented Generation  
✅ Tool orchestration  
✅ Agent-based architecture  
✅ Persistent memory  
✅ Streaming UX  
✅ Thread isolation  

These are the same concepts used in production AI systems.

---

## 🔮 Future Improvements

- Persistent vector storage (instead of in-memory)
- Authentication & multi-user support
- Docker deployment
- Async tool execution
- Hybrid search (keyword + vector)
- Observability with LangSmith

---

## 👨‍💻 Author

**Praveen K**

If you found this useful, consider starring ⭐ the repo!

---

## ⭐ Pro Tip for Recruiters

This project focuses on **system design for AI applications**, not just model usage — highlighting skills relevant to modern AI engineering roles.