# Chat with Multiple Pdf App

The Chat with Multiple Pdf App is a Python application that allows you to chat with multiple PDF documents. You can ask questions about the PDFs using natural language, and the application will provide relevant responses based on the content of the documents. This app utilizes a language model to generate accurate answers to your queries. Please note that the app will only respond to questions related to the loaded PDFs.

## How It Works
The application employs a standard **Retrieval-Augmented Generation (RAG)** pipeline to fetch and synthesize answers

![](screenshot.png)

The application follows these steps to provide responses to your questions:

1. **PDF Loading:** The app reads multiple PDF documents and extracts their text content.
2. **Text Chunking:** The extracted text is divided into smaller chunks that can be processed effectively.
3. **Language Model:** The application utilizes a language model to generate vector representations (embeddings) of the text chunks.
4. **Similarity Matching:** When you ask a question, the app compares it with the text chunks and identifies the most semantically similar ones.
5. **Response Generation:** The selected chunks are passed to the language model, which generates a response based on the relevant content of the PDFs.

---

## 🛠️ Tech Stack

* **Frontend:** [Streamlit](https://streamlit.io/) (for building the interactive web UI)
* **LLM & Embeddings:** [OpenAI API](https://openai.com/) (or LangChain-supported open-source alternatives)
* **Framework:** [LangChain](https://python.langchain.com/) (for managing the RAG pipeline and memory)
* **PDF Processing:** PyPDF2 / PyMuPDF
* **Vector Store:** FAISS (or Pinecone/Chroma depending on configuration)

---
