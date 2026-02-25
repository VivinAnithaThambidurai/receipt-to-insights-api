# receipt-to-insights-api

Backend API that converts receipt uploads into structured data and spending insights.

---

## 🚀 Tech Stack
- Python 3
- FastAPI
- Uvicorn (ASGI server)
- Git + GitHub

---

## 📦 Setup (Local Development)

1) Clone the repository
git clone https://github.com/VivinAnithaThambidurai/receipt-to-insights-api.git
cd receipt-to-insights-api

2) Create virtual environment
python3 -m venv venv

3) Activate virtual environment

Mac/Linux:
source venv/bin/activate

Windows:
venv\Scripts\activate

4) Install dependencies
pip install -r requirements.txt

---

## ▶ Run the Server
uvicorn app.main:app --reload --reload-exclude venv

Server runs at:
http://127.0.0.1:8000

---

## 📘 API Documentation (Swagger UI)
Open in browser:
http://127.0.0.1:8000/docs

---

## 📡 Available Endpoints

GET /health  
Returns:
{ "status": "ok" }

POST /receipts/upload  
- Accepts file upload (multipart/form-data)  
- Returns filename and content type  

Example Response:
{
  "filename": "receipt.pdf",
  "content_type": "application/pdf"
}

---

## 🛠 Development Workflow

After making changes:
git add .
git commit -m "Describe your change"
git push

---

## 📌 Project Goal

Build a production-style backend that:
1. Accepts receipt uploads
2. Extracts receipt text (OCR)
3. Parses structured data
4. Stores in database
5. Generates spending insights
