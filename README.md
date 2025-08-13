# Chat with Multiple PDFs using Google Gemini API (📄)

Upload multiple PDFs and ask questions about their content. The app uses Google’s Gemini API for understanding, FAISS for semantic search, and Streamlit for a clean, interactive UI.

## Features (🚀)
- Upload one or multiple PDF files
- Automatically extract text from all PDFs
- Split text into chunks for efficient retrieval
- Create embeddings with Google Generative AI (e.g., text-embedding-004)
- Store and search embeddings with FAISS
- Ask natural-language questions; if the answer isn’t in your PDFs, the app replies “No”

## Tech Stack (🛠️)
- Python 3.10+
- Streamlit (Web UI)
- PyPDF2 (PDF text extraction)
- LangChain (chaining & prompts)
- Google Generative AI (Gemini for LLM and embeddings)
- FAISS (vector search)
- python-dotenv (environment variables)

## Project Structure (📂)
```
.
├── app.py              # Main Streamlit app
├── requirements.txt    # Python dependencies
├── README.md           # Project documentation
├── .env                # API key storage (not committed)
└── faiss_index/        # Local FAISS index (generated at runtime)
```

## Installation (📦)
1) Clone the repository
```
git clone https://github.com/yourusername/chat-with-pdf.git
cd chat-with-pdf
```

2) Create & activate a virtual environment
```
python -m venv venv
# On Windows
venv\Scripts\activate
# On macOS/Linux
source venv/bin/activate
```

3) Install dependencies
```
pip install -r requirements.txt
```

4) Create a .env file and add your Google API key
```
GOOGLE_API_KEY=your_google_api_key_here
```
- Get a key from Google AI Studio: https://aistudio.google.com/app/apikey
- Ensure the Gemini API is enabled for your account/project

## Usage (▶️)
Run the Streamlit app:
```
streamlit run app.py
```

Then:
1) Upload one or more PDFs from the sidebar
2) Click “Submit and Process” to extract, chunk, embed, and index
3) Ask questions in the input field
4) Receive answers based only on your uploaded PDFs (or “No” if not found)

## Example (📌)
- Question: “What is the total invoice amount in document 1?”
- Reply: “₹25,000” (if present in the PDFs)
- Reply: “No” (if not found in the PDFs)

## Notes (⚠️)
- Gemini/Generative AI must be enabled for your API key
- The FAISS index is saved locally in faiss_index/
- Large PDFs may take longer to process
- Do not commit your .env file to version control

## License (📜)
MIT License — free to use and modify.
