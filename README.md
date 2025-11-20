# 📄 AI CV Parser — Mistral + FastAPI + LangChain + Streamlit

An **AI-powered Resume (CV) Parser** built using **Mistral-Nemo-Instruct**, **FastAPI**, **LangChain**, and **Streamlit**.  
The system extracts structured information (Name, Email, Skills, Experience, Education) from PDF resumes using a powerful LLM and returns clean JSON output.

---

## 🚀 Features

- 🔍 Extracts key CV information automatically  
- ⚡ FastAPI backend exposed via ngrok  
- 🧠 Mistral-Nemo-Instruct 2407 for accurate extraction  
- 🧩 JSON output via LangChain Structured Output Parser  
- 📤 Upload a PDF → Receive clean structured JSON  
- 🌐 Streamlit UI for user-friendly interaction  
- 🔐 Secured with Bearer Token  

---

## 🏗️ System Architecture

[User] → [Streamlit App] → [FastAPI Endpoint (/parse_cv)] → [Mistral Model]
         ↑                     ↓
         └────────────── ngrok Public URL ───────────────┘

---

## 📂 Project Structure

├── app.py                   # FastAPI backend  
├── streamlit_app.py         # Streamlit UI  
├── README.md                # Documentation  
├── requirements.txt         # Dependencies  
└── assets/                  # Optional screenshots  

---

## 🧰 Requirements

- Python 3.10+  
- GPU recommended (optional)  
- ngrok account for public API  

---

## 🔧 Installation

### 1️⃣ Clone the repo
git clone https://github.com/your-username/ai-cv-parser.git
cd ai-cv-parser

### 2️⃣ Install dependencies
pip install -r requirements.txt

### 3️⃣ Add your tokens
Inside `app.py`:
NGROK_TOKEN = "YOUR_NGROK_TOKEN"
API_KEY = "secret123"

### 4️⃣ Run FastAPI backend
python app.py

You will get a public URL like:
https://xxxx.ngrok-free.app

### 5️⃣ Configure Streamlit
Inside `streamlit_app.py`:
API_URL = "https://xxxx.ngrok-free.app/parse_cv"

Then run:
streamlit run streamlit_app.py

---

## 📡 API Documentation

### POST /parse_cv

#### 🔐 Header
Authorization: Bearer secret123

#### 📤 Request
multipart/form-data:
  file: <your_cv.pdf>

#### 📥 Example Response
{
  "parsed_cv": {
    "full_name": "John Doe",
    "email": "john@example.com",
    "education": "BSc Computer Science - MIT (2020)",
    "skills": ["Python", "Machine Learning", "SQL"],
    "experience": "Data Scientist at OpenAI (2020–2023)"
  }
}

---

## 🖥️ Streamlit App

📁 Upload CV → 🧠 AI Parser → 📦 JSON Output

---

## 📸 Screenshots (Optional)

![Streamlit UI](assets/streamlit.png)
![JSON Output](assets/json_output.png)

---

## 🤝 Contributing

Pull requests are welcome — especially for adding new extracted fields or improving the UI.

---

## 📜 License

Distributed under the **MIT License**.

---

## ⭐ Support

If you like this project, don't forget to star ⭐ the repository!
