# 📚 Chat with PDF using Gemini AI

An advanced PDF chat application that allows users to upload PDF documents and ask questions about their content. Built
with Streamlit, LangChain, and Google's Gemini AI, this application provides intelligent responses based on the content
of uploaded PDFs.

## ✨ Features

- PDF document upload and processing (multiple files supported)
- Text extraction and chunking
- Vector embeddings using Google's Embedding Model
- Semantic search capabilities using FAISS
- Conversational AI powered by Gemini-1.5-flash
- Interactive chat interface
- Context-aware responses
- Local vector store persistence

## 🛠️ Technologies Used

- Python 3.x
- Streamlit
- LangChain
- Google Generative AI
- FAISS (Facebook AI Similarity Search)
- PyPDF2
- dotenv

## 📋 Prerequisites

Install the required packages:

```bash
pip install streamlit
pip install langchain
pip install langchain-google-genai
pip install google-generativeai
pip install faiss-cpu
pip install PyPDF2
pip install python-dotenv
```

## 🔑 API Key Setup

1. Obtain a Google Gemini AI API key from [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Create a `.env` file in the root directory
3. Add your API key:

```env
GOOGLE_API_KEY=your_api_key_here
```

## 🚀 Getting Started

1. Clone this repository:

```bash
git clone <repository-url>
cd pdf-chat-gemini
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the application:

```bash
streamlit run app.py
```

## 💻 How to Use

1. Open the application in your web browser
2. In the sidebar, upload one or more PDF files
3. Click "Submit & Process" to analyze the documents
4. Ask questions in the main chat interface
5. Receive AI-powered responses based on the PDF content

## 🔧 Core Components

### PDF Processing

```python
def get_pdf_text(pdf_docs)
```

- Extracts text from uploaded PDF files
- Combines content from multiple PDFs

### Text Chunking

```python
def get_text_chunks(text)
```

- Splits text into manageable chunks
- Uses recursive character text splitting
- Configurable chunk size and overlap

### Vector Store

```python
def get_vector_store(text_chunks)
```

- Creates embeddings using Google's model
- Builds and saves FAISS vector store
- Enables efficient similarity search

### Conversation Chain

```python
def get_conversational_chain()
```

- Sets up the QA chain with Gemini model
- Configures custom prompt template
- Manages context and question handling

## 📁 Project Structure

```
pdf-chat-gemini/
│
├── app.py                 # Main application file
├── .env                   # Environment variables
├── requirements.txt       # Project dependencies
├── faiss_index/          # Vector store directory
└── README.md             # Documentation
```

## ⚙️ Configuration Options

Key parameters that can be customized:

- Chunk size and overlap in text splitting
- Model temperature for response generation
- Embedding model selection
- Vector store configuration
- Prompt template customization

## 🔍 Features in Detail

1. **PDF Processing**
    - Multiple PDF upload support
    - Full text extraction
    - Content preservation

2. **Text Processing**
    - Intelligent text chunking
    - Context overlap maintenance
    - Efficient text handling

3. **Vector Search**
    - FAISS similarity search
    - Fast query processing
    - Persistent vector storage

4. **AI Integration**
    - Gemini AI integration
    - Context-aware responses
    - Temperature-controlled output

## 🛡️ Error Handling

The application includes error handling for:

- PDF processing errors
- API failures
- Invalid file formats
- Empty responses
- Vector store issues

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## ⚠️ Troubleshooting

Common issues and solutions:

1. **PDF Processing Issues**
    - Ensure PDFs are not password protected
    - Check PDF file permissions
    - Verify file format compatibility

2. **API Issues**
    - Verify API key configuration
    - Check API quota limits
    - Ensure internet connectivity

3. **Performance Issues**
    - Optimize chunk sizes for large documents
    - Monitor memory usage
    - Check vector store efficiency

## 📈 Future Enhancements

Potential improvements:

1. Support for more document formats
2. Enhanced error handling
3. User session management
4. Response caching
5. Advanced query optimization
6. Custom embedding models

## 💡 Best Practices

1. Use clear, specific questions
2. Upload high-quality PDF documents
3. Process documents in reasonable batches
4. Monitor vector store size
5. Regular maintenance of stored vectors

## 🙏 Acknowledgments

- Google Gemini AI team
- LangChain community
- Streamlit developers
- FAISS development team