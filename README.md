# 📄 AI CV Parser — Mistral + FastAPI + LangChain + Streamlit

An **AI-powered Resume (CV) Parser** built using **Mistral-Nemo-Instruct**, **FastAPI**, **LangChain**, and **Streamlit**.  
The system extracts structured information (Name, Email, Skills, Experience, Education) from PDF resumes using a powerful LLM and returns clean JSON output.

---

## ⚡ Features

-  Extracts key CV information automatically  
-  FastAPI backend exposed via ngrok  
-  Mistral-Nemo-Instruct 2407 for accurate extraction  
-  JSON output via LangChain Structured Output Parser  
-  Upload a PDF → Receive clean structured JSON  
-  Streamlit UI for user-friendly interaction  
-  Secured with Bearer Token  

---

## 📂 Project Structure

| File / Folder            | Description                                                |
|--------------------------|------------------------------------------------------------|
| AI_CV_Parser_API.ipynb   | Jupyter Notebook containing backend (FastAPI + LLM)        |
| app.py                   | Streamlit app for uploading CVs + showing parsed JSON      |
| README.md                | Project documentation                                      |
| demo.mp4                 | Video demo of the system in action                         |
| assets/                  | UI and output screenshots                                  |

---

#### 📥 Example Response
```json
{
  "parsed_cv": {
    "full_name": "John Doe",
    "email": "john@example.com",
    "education": "BSc Computer Science - MIT (2020)",
    "skills": ["Python", "Machine Learning", "SQL"],
    "experience": "Data Scientist at OpenAI (2020–2023)"
  }
}
```
---

## 🖥️ Streamlit App

📁 Upload CV → 🧠 AI Parser → 📦 JSON Output

---

## 📸 Screenshots

![Streamlit UI](assets/streamlit.png)
![JSON Output](assets/json_output.png)
