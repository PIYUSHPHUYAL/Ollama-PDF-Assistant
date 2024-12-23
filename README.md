# Ollama PDF Assistant

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

A Jupyter notebook for efficient PDF processing, analysis, and interaction using advanced programming techniques. Extract text, generate summaries, and gain insights from PDF documents with ease.

## 🚀 Features

- **PDF Text Extraction**: Extract both raw and structured text from PDF documents
- **Content Summarization**: Generate concise summaries of large text blocks using NLP
- **Interactive Analysis**: Dynamically query and explore PDF content
- **Customizable Functions**: Extend capabilities for specific use cases

## 📋 Prerequisites

- Python 3.8 or higher
- Jupyter Notebook/JupyterLab
- Required Python packages:
  ```
  pypdf2
  nltk
  ```

## 🛠️ Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/ollama-pdf-assistant.git
   cd ollama-pdf-assistant
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

## 📖 Usage

1. **Launch the Notebook**
   ```bash
   jupyter notebook Ollama_PDF_Assistant.ipynb
   ```

2. **Process Your PDF**
   ```python
   # Example code
   from pdf_processor import read_pdf
   
   # Load and process PDF
   pdf_content = read_pdf('your_document.pdf')
   ```

3. **Generate Summaries**
   ```python
   # Example summarization
   from text_processor import summarize_text
   
   summary = summarize_text(pdf_content, word_limit=200)
   ```

## 🏗️ Structure

### 1. Initialization
- Library imports (PyPDF2, NLTK)
- Environment setup
- Configuration initialization

### 2. PDF Processing
- File upload handling
- Text extraction
- Content parsing

### 3. Analysis Tools
- Text summarization
- Content querying
- Interactive analysis features

## 🔧 Customization

### Adding New Features
```python
# Example: Adding custom summarization
def custom_summarize(text, model="your-preferred-model"):
    # Your implementation here
    pass
```

### Modifying Existing Functions
- Adjust summarization parameters
- Customize text extraction
- Implement additional analysis methods

## ⚠️ Troubleshooting

### Common Issues

1. **Missing Dependencies**
   ```bash
   pip install missing_package_name
   ```

2. **PDF Processing Errors**
   - Ensure PDF is not password-protected
   - Verify file permissions
   - Check PDF format compatibility

### Debug Tips
- Enable debug logging
- Check console output
- Verify file paths

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch:
   ```bash
   git checkout -b feature/YourFeature
   ```
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📬 Contact

For support or queries, please open an issue in the GitHub repository.

---

**Note**: This notebook is in active development. Features and documentation may be updated frequently.