🗒️ Invoice Extraction Platform

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-2.3.3-green.svg)](https://flask.palletsprojects.com/)
[![Streamlit](https://img.shields.io/badge/Streamlit-Latest-red.svg)](https://streamlit.io)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.12.0-orange.svg)](https://tensorflow.org)
[![Gemini AI](https://img.shields.io/badge/Gemini-AI-purple.svg)](https://ai.google.dev/)

An intelligent invoice data extraction platform that uses AI and computer vision to automatically extract structured data from invoice images. Features both traditional computer vision models and Google's Gemini AI for accurate field detection and data extraction.

✨ Features

- 🤖 Dual AI Extraction: Choose between traditional computer vision models or Google Gemini AI
- 📊 Visual Field Detection: Bounding box visualization for detected invoice fields
- 🔍 Smart Search: AI-powered search functionality to find specific invoice information
- 📤 Multiple Export Formats: JSON, CSV, YAML, XML, HTML, PNG, and Text exports
- 🖥️ Dual Interface: Both Flask web app and Streamlit interface available
- ⚡ Real-time Processing: Instant invoice processing and data extraction
- 🛡️ Fallback System: Automatic fallback to mock data when AI services are unavailable

🚀 Quick Start

⚠️ **FIRST TIME SETUP**: Run the secure setup script:
```bash
setup_secure.bat
```

Option 1: Streamlit Interface (Recommended)
```bash
cd app
start_app.bat
```
Access at: http://localhost:8501

Option 2: Flask Interface
```bash
cd app
run.bat
```
Access at: http://localhost:5000

Option 3: Manual Setup
```bash
# Install Python 3.10+
# Create virtual environment
python -m venv venv
venv\Scripts\activate

# Install dependencies
cd app
pip install -r requirements.txt

# Set up environment variables (see Configuration section)
# Run Streamlit app
streamlit run streamlit_app.py
```

📁 Project Structure

```
final_invoice/
├── 📁 app/                     # Main Streamlit application
│   ├── streamlit_app.py        # Primary Streamlit interface
│   ├── requirements.txt        # Python dependencies
│   ├── start_app.bat          # Quick start script
│   ├── run.bat                # Alternative run script
│   ├── 📁 uploads/            # Uploaded invoice images
│   └── 📁 static/             # CSS and JavaScript files
│
├── 📁 final_invoice_streamlit/ # Alternative Streamlit version
│   ├── streamlit_app.py        # Streamlit application
│   ├── model_detector.py       # Model detection utilities
│   ├── requirements.txt        # Dependencies
│   ├── run_app.bat            # Run script
│   └── start.bat              # Setup and run script
│
├── 📁 models/                  # TensorFlow models and training
│   ├── 📁 official/           # Official TensorFlow models
│   ├── 📁 research/           # Research models
│   └── 📁 saved_model/        # Trained model checkpoints
│
├── 📁 workspace/              # Training workspace
│   └── 📁 training_demo/      # Model training files
│
├── 📁 scripts/                # Utility scripts
│   ├── generate_train_record.py
│   ├── generate_test_record.py
│   └── model_main_tf2.py
│
├── 📁 restructured/           # Organized project structure
└── 📄 README.md               # This documentation
```

🔧 Configuration

⚠️ **SECURITY NOTICE**: If you're seeing this after a security alert, please read `API_SECURITY_GUIDE.md` immediately!

Environment Variables
1. Create a `.env` file in the project root:
```bash
GOOGLE_API_KEY=your_api_key_here
```
2. Never commit the `.env` file to version control
3. The `.env` file is already added to `.gitignore` for security

Supported File Formats
- Images: JPEG, JPG, PNG
- Documents: PDF (converted to images)

🎯 Usage

1. Upload Invoice: Drag and drop or select an invoice image
2. Choose Extraction Method:
   - Dataset Model: Traditional computer vision approach
   - Gemini AI: Advanced AI-powered extraction
3. View Results: Extracted data displayed in structured format
4. Visualize Fields: Show bounding boxes on detected fields
5. Search Data: Use AI search to find specific information
6. Export Results: Download in your preferred format

📊 Extracted Fields

- Company Name and Address
- Customer Name and Address  
- Invoice Number and Dates
- Line Items with quantities and prices
- Subtotal, Tax, and Total amounts
- Payment terms and due dates

🛠️ Technical Stack

- Backend: Python 3.10+, Flask 2.3.3
- Frontend: Streamlit, HTML/CSS/JavaScript
- AI/ML: TensorFlow 2.12.0, Google Gemini AI
- Image Processing: Pillow, OpenCV, pytesseract
- Data Processing: pandas, numpy
- Export: JSON, CSV, YAML, XML, HTML

📋 Requirements

- Python 3.10 or higher
- Windows OS (batch files provided)
- Internet connection (for Gemini AI)
- 4GB+ RAM recommended
- Modern web browser

🔍 Troubleshooting

Common Issues:

- Import Errors: Ensure all dependencies are installed via `pip install -r requirements.txt`
- API Errors: Check your GOOGLE_API_KEY environment variable
- Model Loading: The app will use fallback extraction if TensorFlow models aren't found
- File Upload: Ensure image files are in supported formats (JPEG, PNG)

📈 Performance

- Processing Time: 2-5 seconds per invoice
- Accuracy: 85-95% depending on image quality
- Supported Languages: English (primary), with basic multilingual support
- File Size Limit: Up to 10MB per image

🤝 Contributing

See [DEVELOPER_GUIDE.md](DEVELOPER_GUIDE.md) for development setup and contribution guidelines.

📚 Documentation

- [User Guide](USER_GUIDE.md) - Detailed usage instructions
- [Developer Guide](DEVELOPER_GUIDE.md) - Development and contribution guide
- [API Documentation](docs/api.md) - API reference (if applicable)

📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

🆘 Support

For issues and questions:
1. Check the [User Guide](USER_GUIDE.md)
2. Review [Troubleshooting](#-troubleshooting) section
3. Create an issue in the project repository

---

Made with ❤️ using Python, TensorFlow, and Google Gemini AI