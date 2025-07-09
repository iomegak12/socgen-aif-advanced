# Azure AI Foundry - Advanced Document Intelligence

This repository contains advanced examples and implementations for Azure AI Document Intelligence services, demonstrating various approaches to document analysis, custom model creation, and intelligent content extraction.

## 📋 Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Modules](#modules)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

## 🔍 Overview

This project showcases advanced techniques for working with Azure AI Document Intelligence, including:

- **Document Intelligence APIs**: Direct API integration for document analysis
- **REST API Management**: Creating and managing custom analyzers
- **Prebuilt Models**: Leveraging Azure's prebuilt document models
- **Custom Models**: Training and deploying custom document intelligence models
- **Multi-format Support**: Processing various document formats (PDF, images, audio, video)

## 📁 Project Structure

```
aif-advanced/
├── 1-doc-intelligence/          # Core document intelligence examples
│   ├── conference-video-analyzer.py    # Video content analysis
│   ├── invoice-analyzer.py             # Invoice processing
│   ├── slide-analyzer.py               # Presentation slide analysis
│   ├── voicemail-analyzer.py           # Audio transcription and analysis
│   └── sample files (PDF, MP3, MP4, JPG)
├── 2-rest-api/                  # REST API integration examples
│   ├── create-analyzer.py              # Custom analyzer creation
│   ├── read-card.py                    # Business card reader
│   ├── biz-card.json                   # Business card schema
│   └── sample business card images
├── 3-prebuilt-doc-intelligence/ # Prebuilt model examples
│   ├── document-analysis.py            # Document analysis with prebuilt models
│   └── sample-invoice.pdf
├── 4-custom-doc-intelligence/   # Custom model training and testing
│   ├── test-model.py                   # Custom model testing
│   ├── setup scripts (CMD/Shell)
│   └── sample-forms/                   # Training data with labels
└── requirements.txt             # Python dependencies
```

## 🛠 Prerequisites

- **Python 3.8+**
- **Azure Subscription** with AI Services enabled
- **Azure AI Document Intelligence** resource
- **Visual Studio Code** (recommended)

### Required Azure Services

1. **Azure AI Document Intelligence** - For document analysis and custom models
2. **Azure AI Foundry** - For advanced AI capabilities
3. **Storage Account** (optional) - For storing training data

## ⚙️ Setup

### 1. Clone the Repository

```bash
git clone <repository-url>
cd aif-advanced
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Environment Configuration

Create a `.env` file in the root directory with your Azure credentials:

```env
# Azure AI Document Intelligence
ENDPOINT=https://your-resource.cognitiveservices.azure.com/
KEY=your-api-key
DOC_INTELLIGENCE_ENDPOINT=https://your-doc-intelligence.cognitiveservices.azure.com/
DOC_INTELLIGENCE_KEY=your-doc-intelligence-key

# Custom Models
MODEL_ID=your-custom-model-id
ANALYZER_NAME=your-analyzer-name

# Azure AI Foundry (if applicable)
AZURE_CONTENT_UNDERSTANDING_AAD_TOKEN=your-aad-token
```

### 4. Additional Setup for Custom Models

For the custom document intelligence module:

**Windows:**
```cmd
cd 4-custom-doc-intelligence
setup.cmd
```

**Linux/macOS:**
```bash
cd 4-custom-doc-intelligence
chmod +x setup.sh
./setup.sh
```

## 📚 Modules

### 1. Document Intelligence Core (`1-doc-intelligence/`)

Advanced document processing capabilities:

- **Invoice Analyzer**: Extract structured data from invoices
- **Conference Video Analyzer**: Process meeting recordings for insights
- **Slide Analyzer**: Extract content from presentation slides
- **Voicemail Analyzer**: Transcribe and analyze voice messages

**Example Usage:**
```bash
cd 1-doc-intelligence
python invoice-analyzer.py
```

### 2. REST API Integration (`2-rest-api/`)

Direct API management and custom analyzer creation:

- **Create Analyzer**: Build custom document analyzers
- **Business Card Reader**: Extract contact information from business cards

**Example Usage:**
```bash
cd 2-rest-api
python create-analyzer.py
python read-card.py
```

### 3. Prebuilt Models (`3-prebuilt-doc-intelligence/`)

Leverage Azure's prebuilt document models:

- Invoice processing
- Receipt analysis
- ID document extraction
- General document analysis

**Example Usage:**
```bash
cd 3-prebuilt-doc-intelligence
python document-analysis.py
```

### 4. Custom Model Training (`4-custom-doc-intelligence/`)

Train and deploy custom document intelligence models:

- Model training with labeled data
- Custom field extraction
- Model testing and validation

**Example Usage:**
```bash
cd 4-custom-doc-intelligence
python test-model.py
```

## 🚀 Usage

### Quick Start

1. **Configure your environment** with Azure credentials
2. **Choose a module** based on your use case
3. **Run the example scripts** to see the functionality
4. **Modify the code** to fit your specific requirements

### Working with Different Document Types

- **PDFs**: Use the invoice analyzer or prebuilt models
- **Images**: Business card reader or slide analyzer
- **Audio**: Voicemail analyzer for transcription
- **Video**: Conference video analyzer for meeting insights

### Custom Model Development

1. Prepare your training data in the `sample-forms/` directory
2. Use the provided label files as templates
3. Run the setup scripts to configure your environment
4. Train your model using Azure AI Document Intelligence Studio
5. Test your model with `test-model.py`

## 🔧 Configuration

### API Endpoints

The project supports multiple Azure AI services:

- **Document Intelligence**: Standard document analysis
- **AI Foundry**: Advanced content understanding
- **Custom Models**: Your trained models

### File Formats Supported

- **Documents**: PDF, DOC, DOCX
- **Images**: JPG, PNG, BMP, TIFF
- **Audio**: MP3, WAV
- **Video**: MP4, AVI

### Performance Optimization

- Use appropriate file sizes (recommended: <20MB)
- Implement retry logic for API calls
- Consider batch processing for multiple documents
- Cache results when appropriate

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines

- Follow PEP 8 for Python code style
- Add docstrings to functions and classes
- Include error handling in your implementations
- Test with sample data before submitting

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For issues and questions:

1. Check the [Azure AI Document Intelligence documentation](https://docs.microsoft.com/azure/applied-ai-services/form-recognizer/)
2. Review the [Azure AI Foundry documentation](https://docs.microsoft.com/azure/ai-foundry/)
3. Open an issue in this repository
4. Contact the Azure support team for service-related issues

## 🔗 Useful Links

- [Azure AI Document Intelligence](https://azure.microsoft.com/services/form-recognizer/)
- [Azure AI Foundry](https://azure.microsoft.com/products/ai-foundry/)
- [Document Intelligence Studio](https://formrecognizer.appliedai.azure.com/)
- [Python SDK Documentation](https://docs.microsoft.com/python/api/azure-ai-formrecognizer/)

---

**Note**: This project requires valid Azure subscriptions and API keys. Ensure you have the necessary permissions and quotas before running the examples.
