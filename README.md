# 🏠 Lebanon Real Estate Investment Advisor

AI-powered RAG system for Lebanese real estate investment advice using semantic search and LLM.

## 🎯 Features

- ✅ Semantic search across 200+ Lebanese properties
- ✅ AI-powered investment recommendations
- ✅ Market insights from RAMCO quarterly reports
- ✅ Smart filtering (price, location, bedrooms, features)
- ✅ Beautiful web interface (Gradio)
- ✅ 100% FREE - No API costs

## 📊 Data Sources

- **Properties:** 200 Lebanese real estate listings (Beirut, Achrafieh, Byblos, etc.)
- **Market Reports:** 4 RAMCO quarterly reports (2013-2015)
- **Coverage:** Apartments, villas, penthouses across major Lebanese cities

## 🛠️ Technology Stack

- **Vector Database:** ChromaDB
- **Embeddings:** Sentence Transformers (free)
- **LLM:** TinyLlama-1.1B (free)
- **Interface:** Gradio
- **PDF Processing:** OCR with Tesseract + pdfplumber
- **Data Processing:** Pandas, NumPy

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- 4GB RAM minimum
- Google Colab (recommended) or local setup

### Installation

1. Clone the repository:
```bash
git clone https://github.com/YOUR_USERNAME/lebanon-real-estate-rag.git
cd lebanon-real-estate-rag
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run in Google Colab (Recommended):
- Open `lebanon_real_estate_rag.ipynb` in Google Colab
- Upload your data files when prompted
- Run all cells

## 📁 Project Structure
```
lebanon-real-estate-rag/
├── README.md
├── requirements.txt
├── lebanon_real_estate_rag.ipynb    # Main Colab notebook
├── data/
│   └── lebanon_properties.csv       # Sample property data
├── docs/
│   └── architecture.md              # System architecture
└── examples/
    └── sample_queries.md            # Example queries
```

## 💡 Usage Examples

### Property Search
```
"What are good apartments in Achrafieh under $400,000?"
```

### Investment Analysis
```
"Best 3-bedroom properties with parking and elevator"
```

### Market Insights
```
"What are the real estate market trends in Beirut?"
```

### District Comparison
```
"Compare properties in Achrafieh vs Byblos"
```

## 🎯 How It Works

1. **User Query** → Natural language question
2. **Vector Search** → Finds relevant properties and market reports
3. **Context Building** → Combines retrieved information
4. **AI Generation** → LLM creates intelligent recommendation
5. **Response** → Formatted answer with property details

## 📊 System Architecture
```
User Query
    ↓
Vector Database (ChromaDB)
    ├── Properties Collection (200 docs)
    └── Reports Collection (121 chunks)
    ↓
Retrieval (Semantic Search)
    ↓
Context Assembly
    ↓
LLM (TinyLlama)
    ↓
Formatted Response
```

## 🔧 Configuration

Edit these settings in the notebook:

- `n_results`: Number of properties to retrieve (default: 3)
- `max_new_tokens`: AI response length (default: 150)
- `chunk_size`: Report chunk size (default: 1000 chars)

## 📈 Performance

- **Response Time:** 30-60 seconds (with AI)
- **Search Accuracy:** Semantic matching
- **Cost:** $0.00 (100% free)
- **Scalability:** Handles 10,000+ properties

## 🐛 Troubleshooting

### PDF Extraction Issues
If PDFs don't extract text, they're likely scanned images. The system uses OCR automatically.

### Slow Responses
Reduce `max_new_tokens` or use the fast version (search only, no AI).

### Memory Issues
Close other notebooks, restart runtime, or use smaller batch sizes.

## 🚀 Future Enhancements

- [ ] Add more Lebanese property data
- [ ] Integrate live property feeds
- [ ] Price prediction model
- [ ] User authentication
- [ ] Save favorite properties
- [ ] Email alerts for new listings
- [ ] Mobile app version
- [ ] Deploy to production (Hugging Face Spaces)

## 📝 License

MIT License - Feel free to use and modify!

## 🤝 Contributing

Contributions welcome! Please:
1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📧 Contact

For questions or suggestions, please open an issue on GitHub.

## 🙏 Acknowledgments

- RAMCO Real Estate for market reports
- Lebanese real estate data providers
- Open-source community for amazing tools

---

**Built with ❤️ for the Lebanese real estate community**
