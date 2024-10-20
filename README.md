# HealthWhiz - Medical Chatbot with Llama 2

HealthWhiz is an intelligent medical chatbot powered by a quantized Llama 2 model, integrated with LangChain and Chainlit. The system provides efficient and responsive healthcare consultations by leveraging advanced natural language processing techniques.

## 🌟 Features

- **AI-Powered Medical Consultations**: Utilizes the Llama 2 7B Chat model for intelligent medical query responses
- **PDF Knowledge Base**: Processes and learns from medical documents to provide accurate information
- **Interactive Chat Interface**: Built with Chainlit for a smooth user experience
- **Vector Database**: Uses FAISS for efficient similarity search and information retrieval
- **Local Deployment**: Runs completely locally, ensuring data privacy and security

## 🔧 Technical Architecture

- **Language Model**: TheBloke/Llama-2-7B-Chat-GGML (Quantized)
- **Framework**: LangChain for orchestration
- **Embeddings**: HuggingFace sentence-transformers/all-MiniLM-L6-v2
- **Vector Store**: FAISS
- **UI**: Chainlit
- **Document Processing**: LangChain's document loaders and text splitters

## 📋 Prerequisites

- Python 3.8+
- 16GB+ RAM recommended
- Sufficient storage space for model and dependencies

## 🚀 Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/healthwhiz.git
cd healthwhiz
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

4. Download the Llama 2 model:
```bash
# The model will be downloaded automatically during first run
# or follow specific instructions for manual download
```

## 💾 Data Preparation

1. Place your medical PDF documents in the `data/` directory

2. Create the vector database:
```bash
python ingest.py
```

## 🎯 Usage

1. Start the Chainlit server:
```bash
chainlit run model.py
```

2. Open your browser and navigate to `http://localhost:8000`

3. Start chatting with HealthWhiz!

## 📁 Project Structure

```
healthwhiz/
├── data/                   # Medical PDF documents
├── vectorstore/           # FAISS vector database
├── model.py              # Main application logic
├── ingest.py            # Vector database creation
├── requirements.txt     # Project dependencies
└── README.md           # Project documentation
```

## ⚙️ Configuration

Key configuration parameters in `model.py`:
- `max_new_tokens`: Controls response length (default: 512)
- `temperature`: Controls response randomness (default: 0.5)
- `chunk_size`: Document splitting size (default: 500)
- `chunk_overlap`: Overlap between splits (default: 50)

## 🎯 Performance

- Processes over 100 medical inquiries with 80% accuracy
- Average response time: 2-3 seconds
- Context-aware responses based on provided medical documentation

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🙏 Acknowledgments

- Thanks to Meta for releasing Llama 2
- The Langchain community for their excellent framework
- Chainlit team for the chat interface
- HuggingFace community for the embeddings model

## ⚠️ Disclaimer

This chatbot is for informational purposes only and should not replace professional medical advice. Always consult with qualified healthcare providers for medical decisions.
