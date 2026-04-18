# 🛍️ StyleCart AI Customer Support Agent

**AI-powered e-commerce support chatbot using RAG, LangGraph, and Gemini**

---

## 🚀 Overview

StyleCart is an end-to-end AI chatbot designed to automate customer support for e-commerce platforms. It handles queries related to returns, shipping, payments, and more using a **Retrieval-Augmented Generation (RAG)** pipeline.

Built with a modular agent architecture, the system ensures responses are **context-aware, accurate, and grounded in a knowledge base**, reducing hallucinations through evaluation.

---

## ✨ Key Features

- 🤖 AI-powered e-commerce FAQ assistant  
- 🔍 RAG-based query handling  
- 🧠 Multi-turn conversational memory  
- 🎯 Smart query routing (retrieval / tool / memory)  
- 📊 Answer faithfulness evaluation (RAGAS)  
- 📚 Semantic search with vector database  
- 🖥️ Interactive Streamlit UI  
- 🔎 Source attribution for transparency  

---

## 🏗️ Architecture

The system is built as a **LangGraph state machine**, where each query flows through structured nodes:
User Query
↓
Memory → Router → (Retrieve / Tool / Skip)
↓
Answer Generation → Evaluation → Save Response


### Node Responsibilities

- **Memory** → Maintains last 6 messages  
- **Router** → Classifies query type  
- **Retrieval** → Fetches relevant documents  
- **Tool** → Handles utility queries (e.g., date)  
- **Answer** → Generates response using LLM  
- **Eval** → Ensures answer faithfulness  
- **Save** → Stores conversation  

---

## 🧠 Tech Stack

- **LLM** → Google Gemini 2.5 Flash  
- **Framework** → LangGraph  
- **Embeddings** → all-MiniLM-L6-v2  
- **Vector DB** → ChromaDB  
- **Frontend** → Streamlit  
- **Evaluation** → RAGAS  
- **Language** → Python  

---

## 📚 Knowledge Base

Includes curated FAQ documents covering:

- Returns & Exchanges  
- Shipping & Delivery  
- Payments & Offers  
- Order Tracking  
- Size Guide  
- Loyalty Program  
- Customer Support  

---

## ⚙️ How It Works

1. User submits a query  
2. Router determines intent  
3. Relevant documents are retrieved  
4. LLM generates grounded response  
5. Response is evaluated for faithfulness  
6. Low-quality answers are regenerated  
7. Final answer is shown with sources  

---

## ⚡ Highlights

- ✅ Reduces hallucination using evaluation loop  
- 🧭 Efficient query routing improves performance  
- 🧠 Context-aware conversations  
- 🔍 Transparent answers with source tracking  
- 🔧 Modular & scalable architecture  

---

## 📦 Setup

```bash
git clone https://github.com/your-username/stylecart-ai-chatbot.git
cd stylecart-ai-chatbot
pip install -r requirements.txt


Create .env file:
GOOGLE_API_KEY=your_api_key


Run the app:
streamlit run app.py

⭐ Support
If you found this useful, consider giving it a ⭐
