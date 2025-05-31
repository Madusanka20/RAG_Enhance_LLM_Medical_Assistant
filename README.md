# 🩺 RAG-Enhanced LLM Medical Assistant

Welcome to the **RAG-Enhanced LLM Medical Assistant** — a smart, multilingual chatbot designed to support patients and hospital staff by providing **friendly, informative responses** about **Holter monitors**. This assistant runs inside a mobile hospital app, powered by advanced **Retrieval-Augmented Generation (RAG)** methods and **Large Language Models (LLMs)**.

It understands **English**, **Sinhala**, and **Tamil**, making it highly accessible in multilingual regions.

---

## ✨ Features

- **🌐 Multilingual Support**  
  Understands and responds to queries in **English, Sinhala, and Tamil** using **Azure’s Translation API**, ensuring smooth communication across language barriers.

- **🔍 Retrieval-Augmented Generation (RAG)**  
  Uses a **FAISS** vector database with **HuggingFace SentenceTransformer embeddings** to retrieve context-relevant content about Holter monitors from curated markdown files.

- **🧠 Conversational Memory**  
  Powered by **LangChain’s ConversationBufferMemory**, the assistant maintains contextual coherence throughout the conversation.

- **🤖 Friendly and Reassuring Tone**  
  Delivers information in a supportive, casual tone—perfect for reducing anxiety and promoting trust. It offers guidance, but always reminds users to consult a medical professional when appropriate.

- **⚡ FastAPI Backend**  
  A modern, fast backend using **FastAPI**, with **CORS support** for integration with mobile and web platforms.

---

## 🗂 Project Structure

📁 RAG-Enhanced-LLM-Medical-Assistant/
├── chat.py # Main chatbot logic: memory, context, and response generation
├── Creating_Vector_DBs.py # Builds the FAISS vector database from markdown data
├── retrieve_context.py # Retrieves relevant markdown content using similarity search
├── palmyra.py # Integration with Palmyra-Med-70B for medical response generation
├── gemini.py # Configures Gemini-1.5-Flash for summarizing conversations
├── summarize.py # Summarizes chat exchanges for long-term memory
├── translator.py # Azure translation logic for multilingual input/output
├── chatbot_endpoint.py # FastAPI app exposing the chatbot interface
├── test.py # Command-line client for testing the API
├── requirements.txt # Required Python dependencies
└── README.md # Project documentation
---
## 🔐 Set Required Environment Variables
Set these environment variables securely, e.g., in a .env file or system environment:

PALMYRA_API_KEY – Your Palmyra-Med-70B model API key

GEMINI_API_KEY – Your Gemini model API key

AZURE_TRANSLATE_KEY – Azure Translator API subscription key

AZURE_TRANSLATE_ENDPOINT – Azure endpoint for translation API
---
## 💬 Usage
Type your query in English, Sinhala, or Tamil.

The assistant will respond in your preferred language.

You can ask questions about Holter monitors (e.g., “How do I wear a Holter monitor?”).

Type quit at any time to exit the session.

⚠️ Disclaimer: This chatbot is designed to provide helpful information, not medical advice. Always consult a licensed healthcare professional for medical concerns.
