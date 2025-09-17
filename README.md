# Financial-Document-Q-A-Assistant-
🤖 AI-powered Financial Document Q&amp;A Assistant using Streamlit &amp; Ollama. Upload PDF/Excel financial statements, extract metrics, and ask questions in natural language. Features local LLM processing, interactive dashboards, and conversational AI for financial analysis. No cloud required! 💼📊

A Streamlit web application that processes financial documents (PDF/Excel) and provides intelligent Q&A using local AI models through Ollama.
🎯 What This Application Does
This app allows you to:

Upload PDF or Excel financial documents
Extract text and financial data automatically
Ask questions about your financial documents in natural language
Get AI-powered answers using local language models
View interactive dashboards with your financial data

Simple Process Flow
graph LR
    A[📄 Upload Document] --> B[🔍 Extract Data]
    B --> C[💾 Store in Memory]
    C --> D[❓ Ask Question]
    D --> E[🤖 AI Processing]
    E --> F[💬 Get Answer]

📦 Dependencies and Their Functions

Core Libraries

| Library        | Version  | Purpose            | What It Does in Our App |
|----------------|----------|--------------------|--------------------------|
| streamlit      | 1.28.1   | Web Framework      | Creates the web interface, handles file uploads, displays results |
| pandas         | 2.1.3    | Data Analysis      | Reads Excel files, processes spreadsheet data |
| PyPDF2         | 3.0.1    | PDF Processing     | Extracts text content from PDF documents |
| openpyxl       | 3.1.2    | Excel (.xlsx)      | Reads modern Excel file formats |
| xlrd           | 2.0.1    | Excel (.xls)       | Reads older Excel file formats |
| requests       | 2.31.0   | HTTP Client        | Communicates with Ollama AI service |
| nltk           | 3.8.1    | Text Processing    | Tokenizes text, removes stop words |
| plotly         | 5.17.0   | Visualizations     | Creates interactive charts and graphs |
| numpy          | 1.25.2   | Numerical Operations | Supports data calculations |
| textstat       | 0.7.3    | Text Statistics    | Analyzes document readability |
| python-dotenv  | 1.0.0    | Environment Variables | Manages configuration settings |

🛠️ Setup Instructions

### Step 1: Prerequisites
Required Python Version: 3.8 - 3.11 (Recommended: 3.10)
```bash
# Check your Python version
python --version
```
### Step 2: Clone or Download
```bash
# If using Git
git clone https://github.com/your-username/financial-qa-assistant.git
cd financial-qa-assistant

# Or download and extract the ZIP file
```
Step 3: Install Python Dependencies
```bash
# Install all required packages
pip install -r requirements.txt


# Alternative using conda:
# Create conda environment (recommended)
conda create -n financial-qa python=3.10 -y
conda activate financial-qa

# Install packages
pip install -r requirements.txt
```
Step 4: Download NLTK Data
```bash
# Download required language processing data
python -c "import nltk; nltk.download('punkt'); nltk.download('stopwords')"

```
Step 5: Install and Setup Ollama
```bash
For Windows:

Download Ollama from https://ollama.ai/download

Install the downloaded file

Open Command Prompt and run:

ollama pull llama2


For Linux/macOS:

# Install Ollama
curl -fsSL https://ollama.ai/install.sh | sh

# Pull the AI model
ollama pull llama2

# Start Ollama service (keep this running)
ollama serve
```

Step 6: Verify Ollama Installation
```bash
# Check if Ollama is working
ollama list

# Test with a simple question
ollama run llama2 "Hello, how are you?"
```
📝 Usage
📂 Step 1: Upload Document

Click "Choose a financial document" in the sidebar

Select a PDF or Excel file containing financial data

Click "Process Document" button

Wait for processing to complete ✅

💬 Step 2: Ask Questions

Go to the Q&A Chat tab

Type your question in the text box

Click "Ask" button or use quick question buttons

View the AI-generated response

📊 Step 3: Explore Data

Dashboard tab: View charts and extracted metrics

Document Content tab: See the raw extracted text

💡 Example Questions You Can Ask
📈 Revenue and Sales

"What was the total revenue for last quarter?"

"Show me all revenue sources mentioned"

"What are the sales figures by month?"

💸 Expenses and Costs

"What are the main expense categories?"

"Calculate the total operating expenses"

"What was spent on marketing?"

📊 Financial Analysis

"What is the profit margin?"

"Calculate the net income"

"What's the debt-to-equity ratio?"

"Show me the financial trends"

📝 General Questions

"Summarize the key financial highlights"

"What are the biggest financial risks mentioned?"

"Compare this quarter to last quarter"
