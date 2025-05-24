
# RAG-Based Personalized Financial Advisor Chatbot

This project implements a Retrieval-Augmented Generation (RAG)-based chatbot for providing **personalized financial investment advice**. The system uses a hybrid document retrieval strategy with a large language model to generate customized investment suggestions based on user-defined preferences.

---

## Features

- **Personalized Investment Advice** using user preferences (e.g., high ROI, low volatility).
- **Semantic Search with FAISS** for context-rich document retrieval.
- **Metadata Filtering with ChromaDB** for structured financial data.
- **Language Generation via Gemini API** for detailed, natural responses.
- **Real-Time Market Data** using `yfinance`.

---

## Architecture

```
User Input → ChromaDB Filter → FAISS Semantic Search → Gemini LLM → Final Response
                             ↘ yFinance API (for live stock info)
```

---

## Technologies Used

- Python, Jupyter Notebook
- FAISS (Facebook AI Similarity Search)
- ChromaDB (for structured metadata)
- Google Gemini API (for LLM-based text generation)
- yFinance (real-time stock data)
- SentenceTransformers (MiniLM for embeddings)
- LangChain (retriever management)

---

## Setup Instructions

1. Clone the repo or download this notebook.
2. Install dependencies:
   ```bash
   pip install faiss-cpu chromadb yfinance sentence-transformers google-generativeai
   ```
3. Add your Gemini API key in the appropriate cell.
4. Run the notebook in Google Colab (recommended for Drive integration).

---

## How It Works

1. User provides investment preferences.
2. System retrieves relevant stock descriptions from ChromaDB and FAISS.
3. Gemini API explains why each stock matches the preference.
4. Results are displayed in Markdown format with clear recommendations.

---

## Example Output

```
Top 5 Recommended Stocks:
- AAPL
- TSLA
- MSFT
...
Explanation:
Stock: AAPL
Reason: AAPL is a blue-chip technology stock with strong long-term growth potential...
```

---

## Team Members

This project was developed as part of the *Natural Language Processing* course.

- **M K Guruprasad** *(Myself)*  
- [**Manda Bala Sumanth**](https://github.com/Sumanth0019)  
- [**Mudrageda Bhargava Phani Sriram**](https://github.com/Sriram77805)

---

## Future Enhancements

- Web/mobile frontend for wider accessibility.
- Voice interaction capabilities.
- User profiles and history learning.
- Enhanced financial dataset (regulatory, tax, etc.).
