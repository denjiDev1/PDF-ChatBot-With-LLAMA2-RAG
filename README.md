# PDF Reader Web App with LLaMA 2 7B and RAG

## Overview
This project delivers a **web-based PDF Reader** powered by **LLaMA 2 7B** and **Retrieval-Augmented Generation (RAG)**. Users can upload PDF files, ask questions via a web UI, and receive accurate answers based on the document content. The system stores PDFs in **MongoDB**, embeds their content into a vector database, and queries them in real time using **LLaMA 2 7B**.

## Features
- **Web Interface**: Upload PDFs and ask questions via a browser.
- **PDF Storage**: Saves PDF files in MongoDB.
- **Text Extraction**: Extracts and processes text using PyMuPDF.
- **Embeddings & Indexing**: Generates vector embeddings using ChromaDB.
- **Query Answering**: Uses RAG with LLaMA 2 7B for context-aware answers.
- **Testing Framework**: Evaluates model performance with Pytest.

## Technologies Used
- **LLaMA 2 7B** (via Hugging Face Transformers)
- **LangChain** for orchestrating RAG
- **MongoDB** for PDF storage
- **ChromaDB** for vector search
- **PyMuPDF** for text extraction
- **FastAPI / Streamlit / Flask** (choose one) for web UI
- **Pytest** for testing and evaluation

## Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/pdf-reader-llama-web.git
   cd pdf-reader-llama-web
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure Environment**
   - Edit `config.py` or `.env` file with your MongoDB credentials:
     ```python
     MONGO_URI = "your_mongo_connection_string"
     MONGO_DB = "your_database_name"
     ```

4. **Start the Web App**
   ```bash
   # If using FastAPI
   uvicorn app.main:app --reload

   # If using Streamlit
   streamlit run app.py

   # If using Flask
   python app.py
   ```

## Usage

1. **Upload PDFs via the Web App**
   - Navigate to the web UI
   - Upload your PDF files through the upload form

2. **Ask Questions**
   - Enter natural language queries about your uploaded PDFs
   - Get real-time answers based on document content

3. **Testing the Model**
   - Evaluate accuracy using `pytest`:
     ```bash
     pytest test.py
     ```


```

## Future Enhancements
- Add **user authentication**
- Support for **multi-document querying**
- Enable **domain-specific fine-tuning**
- Improve **embedding efficiency** and indexing speed
- Deploy with **Docker** and **Kubernetes**

## License
MIT License
