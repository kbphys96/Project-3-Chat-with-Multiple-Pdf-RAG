# 📄 Chat with Multiple PDFs using Google Gemini API

This project allows you to **upload multiple PDF documents** and **ask questions** about their content.  
It uses **Google Gemini API** for text understanding and **FAISS** for semantic search to retrieve relevant chunks from the PDFs.  
The app is built with **Streamlit** for an interactive UI.

---

## 🚀 Features
- Upload one or multiple PDF files.
- Extract text automatically from all PDFs.
- Split text into chunks for efficient search.
- Embed text using **Google Generative AI embeddings**.
- Store and retrieve embeddings with **FAISS**.
- Ask natural language questions — if the answer is not in the PDF, the app replies with **"No"**.

---

## 🛠️ Tech Stack
- **Python 3.10+**
- [Streamlit](https://streamlit.io/) - Web UI
- [PyPDF2](https://pypi.org/project/PyPDF2/) - PDF text extraction
- [LangChain](https://www.langchain.com/) - Chaining & prompt handling
- [Google Generative AI](https://cloud.google.com/vertex-ai/generative-ai) - Embeddings & LLM
- [FAISS](https://github.com/facebookresearch/faiss) - Vector search
- [python-dotenv](https://pypi.org/project/python-dotenv/) - Environment variables

---

## 📂 Project Structure
.
├── app.py # Main Streamlit app
├── requirements.txt # Python dependencies
├── README.md # Project documentation
└── .env # API key storage (not pushed to GitHub)

yaml
Copy
Edit

---

## 📦 Installation
1️⃣ Clone the repository:
```bash
git clone https://github.com/yourusername/chat-with-pdf.git
cd chat-with-pdf
2️⃣ Create & activate a virtual environment:

bash
Copy
Edit
python -m venv venv
# On Windows
venv\Scripts\activate
# On Mac/Linux
source venv/bin/activate
3️⃣ Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
4️⃣ Create a .env file and add your Google API Key:

env
Copy
Edit
GOOGLE_API_KEY=your_google_api_key_here
▶️ Usage
Run the Streamlit app:

bash
Copy
Edit
streamlit run app.py
Steps inside the app:

Upload one or more PDFs from the sidebar.

Click "Submit and Process" to extract & store text.

Ask questions in the text input field.

Get answers based only on your uploaded PDFs.

📌 Example Prompt
Question: "What is the total invoice amount in document 1?"
Reply: "₹25,000" (If present in PDF)
Reply: "No" (If not found in PDF)

⚠️ Notes
Make sure your Google Cloud account has Generative AI API enabled.

FAISS index is stored locally in the folder faiss_index/.

For large PDFs, processing time might take a few seconds.

📜 License
This project is licensed under the MIT License — feel free to use and modify.