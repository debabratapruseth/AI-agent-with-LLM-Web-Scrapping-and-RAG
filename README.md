# 🌐 Web Insights Agent using OpenAI, Web Scraping and RAG 

The project demonstrates how to build a scalable and efficient Web Insights Agent using RAG (Retrieval-Augmented Generation). The agent scrapes a web page and its internal links, stores their content in a FAISS vector store, and uses GPT-4 to answer user questions based on relevant retrieved chunks.

## 🧑‍🏫 What You’ll Learn
This project is ideal for beginner to intermediate Python/AI learners and covers:

Advanced web scraping and internal link handling

Semantic chunking and embedding with OpenAI

Vector similarity search using FAISS

RetrievalQA pipeline with GPT-4 for contextual question answering

Core RAG concepts in practice

## 🛠️ Technologies Used
This solution integrates the following tools:

requests + BeautifulSoup: Scrape HTML content and recursively visit child/internal links.

RecursiveCharacterTextSplitter (LangChain): Chunk large documents into LLM-friendly segments.

OpenAI’s text-embedding-ada-002: Create embeddings for each text chunk.

FAISS (Facebook AI Similarity Search): Vector database to store and retrieve embeddings efficiently.

LangChain’s RetrievalQA Chain: Combines a retriever (FAISS) with GPT-4 to generate accurate answers.

GPT-4 / GPT-3.5: LLM engine for answering questions using retrieved web knowledge.

Google Colab: Notebook-based interface for easy execution and experimentation.

## 🧠 How It Works
Input: User provides a question and a target URL.

Scraping: The code scrapes content from the main URL and child pages (limited to 5–10 by default).

Chunking & Embedding:

  Content is split into manageable chunks.

  Embeddings are created and stored in FAISS.

Retrieval + LLM:

  User’s question is converted into an embedding.

  FAISS returns top-k similar chunks.

GPT-4 is called with those chunks and the user’s question.

Response: The agent returns a concise, contextually correct answer.


## 🚀 Getting Started
Clone the repository or open the notebook in Google Colab.

Set your OpenAI API key (OPENAI_API_KEY).

Run all cells and try your own questions on any website!



## 🔮 Future Enhancements
Add persistent FAISS index saving/loading

Integrate ChromaDB or Pinecone for cloud-scale use

Build a Streamlit UI for non-technical users

Add summarization for longer child pages before embedding
