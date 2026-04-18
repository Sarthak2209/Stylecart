🛍️ StyleCart AI Customer Support Agent

An end-to-end AI-powered customer support chatbot for e-commerce platforms, built using LangGraph, Gemini (Google Generative AI), ChromaDB, and Streamlit.

The system simulates a real-world fashion e-commerce assistant capable of handling queries related to returns, shipping, payments, and more using a Retrieval-Augmented Generation (RAG) pipeline with built-in evaluation for answer faithfulness.

🚀 Features
🤖 AI-powered FAQ chatbot for e-commerce
🔍 Retrieval-Augmented Generation (RAG) pipeline
🧠 Context-aware multi-turn conversations
🎯 Intelligent query routing (retrieval / tool / memory)
📊 Faithfulness evaluation using RAGAS
📚 Semantic search with vector database
🖥️ Interactive Streamlit chat interface
🔎 Source attribution for transparency
🏗️ System Architecture

The chatbot is built using a LangGraph state machine, where each user query flows through multiple processing nodes:

Memory Node → Maintains conversation history (last 6 turns)
Router Node → Classifies query type
Retrieval Node → Fetches relevant documents from vector DB
Tool Node → Handles utility queries (e.g., date)
Answer Node → Generates response using LLM
Eval Node → Validates answer faithfulness
Save Node → Stores response in memory
🧠 Tech Stack
Component	Technology
LLM	Google Gemini 2.5 Flash
Agent Framework	LangGraph
Embeddings	all-MiniLM-L6-v2
Vector Database	ChromaDB
Frontend	Streamlit
Evaluation	RAGAS
Language	Python
📚 Knowledge Base

The chatbot uses curated FAQ documents covering:

Return Policy
Shipping & Delivery
Payment Methods
Order Tracking
Exchange Process
Cancellation Policy
Size Guide
Loyalty Program (StyleCoins)
COD & Offers
Customer Support
💻 How It Works
User enters a query
System classifies intent
Relevant documents are retrieved
LLM generates a grounded answer
Answer is evaluated for faithfulness
If score < 0.7 → response is regenerated
Final answer is displayed with sources
🖼️ Demo
📌 Return Policy Query
Bot retrieves correct policy and answers accurately
No hallucination beyond knowledge base
📌 Multi-turn Conversation
Handles follow-up queries
Maintains conversational context
Displays sources used
⚡ Unique Highlights
✅ RAG + Faithfulness Evaluation (reduces hallucination)
🧭 Smart query routing system
🧠 Sliding window conversational memory
👤 Customer name extraction for personalization
🔍 Source transparency in UI
🔧 Modular and scalable architecture
🔮 Future Improvements
Persistent vector database (Pinecone / Weaviate)
Live knowledge base updates (admin panel)
Multilingual support (Hindi + regional languages)
Order-level personalization via APIs
Voice interface (speech-to-text)
Analytics dashboard
Human agent escalation system
📦 Installation & Setup
# Clone the repo
git clone https://github.com/your-username/stylecart-ai-chatbot.git

# Go to project folder
cd stylecart-ai-chatbot

# Install dependencies
pip install -r requirements.txt

# Add your API key in .env file
GOOGLE_API_KEY=your_api_key_here

# Run the app
streamlit run app.py
📌 Usage
Open the Streamlit app in browser
Ask queries like:
"What is your return policy?"
"Do you offer COD?"
"How long does delivery take?"
🎯 Conclusion

StyleCart demonstrates the power of Agentic AI + RAG systems in automating customer support.
By combining semantic search, LLMs, and evaluation frameworks, the chatbot delivers accurate, reliable, and scalable support solutions for real-world e-commerce platforms.


⭐ If you like this project

Give it a ⭐ on GitHub!
