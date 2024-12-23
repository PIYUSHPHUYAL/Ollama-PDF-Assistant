# PDF Chat Assistant

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Langchain](https://img.shields.io/badge/Langchain-Enabled-green.svg)](https://python.langchain.com/docs/get_started/introduction)
[![Ollama](https://img.shields.io/badge/Ollama-Powered-blue.svg)](https://ollama.ai/)

An intelligent PDF chat system that allows users to have natural conversations about the content of their PDF documents. Built using Langchain for document processing, Ollama for model management, and Mistral as the underlying language model, with RAG (Retrieval Augmented Generation) for accurate and contextual responses.

## 🌟 Features

- **Interactive PDF Chat**: Ask questions about your PDF documents in natural language
- **RAG Implementation**: Get accurate, context-aware responses using retrieval-augmented generation
- **Mistral Integration**: Powered by the powerful Mistral language model through Ollama
- **Document Processing**: Efficient PDF parsing and text extraction using Langchain
- **Vector Storage**: Optimized document embeddings for quick retrieval
- **Context Awareness**: Maintains conversation context for follow-up questions

## 🛠️ Technology Stack

- **Langchain**: For document processing and RAG implementation
- **Ollama**: Local model management and inference
- **Mistral**: Large Language Model
- **RAG**: For enhanced response accuracy
- **Vector Database**: For efficient document embeddings storage
- **Python**: Core programming language

## 📋 Prerequisites

- Python 3.8 or higher
- Ollama installed and running locally
- Sufficient storage for model weights and vector embeddings
- Required Python packages:
  ```
  langchain
  pypdf
  chromadb
  sentence-transformers
  ```

## 🚀 Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/pdf-chat-assistant.git
   cd pdf-chat-assistant
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Install Ollama and download Mistral model:
   ```bash
   # Install Ollama (instructions vary by OS)
   curl https://ollama.ai/install.sh | sh
   
   # Pull Mistral model
   ollama pull mistral
   ```

## 💻 Usage

1. **Start the Application**
   ```bash
   python main.py
   ```

2. **Upload PDF**
   ```python
   from pdf_processor import process_pdf
   
   # Load and process PDF
   document = process_pdf('your_document.pdf')
   ```

3. **Start Chatting**
   ```python
   from chat_engine import ChatEngine
   
   # Initialize chat engine
   chat = ChatEngine(document)
   
   # Ask questions
   response = chat.ask("What is the main topic of this document?")
   ```

## 🔍 How It Works

1. **Document Processing**
   - PDF is uploaded and processed using Langchain
   - Text is split into chunks and embedded
   - Embeddings are stored in vector database

2. **RAG Implementation**
   - User query is processed and embedded
   - Relevant document chunks are retrieved
   - Context is provided to Mistral model

3. **Response Generation**
   - Mistral model generates response using retrieved context
   - Response is formatted and returned to user

## ⚙️ Configuration

```python
# config.py example
CONFIG = {
    "chunk_size": 1000,
    "chunk_overlap": 200,
    "model_name": "mistral",
    "temperature": 0.7,
    "max_tokens": 500
}
```

## 🔧 Customization

### Model Selection
```python
# Use different Ollama models
SUPPORTED_MODELS = [
    "mistral",
    "llama2",
    "codellama"
]
```

### RAG Parameters
```python
# Adjust retrieval settings
RAG_CONFIG = {
    "k_retrieval": 4,
    "similarity_threshold": 0.7
}
```

## ⚠️ Troubleshooting

### Common Issues

1. **Ollama Connection**
   ```bash
   # Check if Ollama is running
   curl http://localhost:11434/api/version
   ```

2. **Memory Issues**
   - Adjust chunk size
   - Optimize vector storage
   - Monitor RAM usage

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch
3. Implement your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Langchain for the amazing document processing tools
- Ollama team for local model deployment
- Mistral AI for the language model
- Open-source community for various tools and libraries

## 📬 Contact

For questions and support:
- Open an issue in the GitHub repository
- [Your Contact Information]

---

**Note**: This is an active project. Expect regular updates and improvements.