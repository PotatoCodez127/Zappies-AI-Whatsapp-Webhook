# 📱 Whatsapp Meta Webhook Middleware

A lightweight, production-ready Flask middleware designed to bridge Meta’s WhatsApp Business API with AI-powered bot backends.

## 💡 Purpose
This microservice acts as a dedicated webhook receiver, enabling:
- **Asynchronous Processing:** Uses Python threading to acknowledge incoming webhooks instantly, preventing connection timeouts with Meta's API.
- **Middleware Isolation:** Decouples your messaging interface from your core AI logic, allowing for independent scaling and maintenance.

## 🛠️ Tech Stack
- **Framework:** Flask (lightweight webhook handling)
- **Deployment:** Gunicorn (production WSGI server)
- **Containerization:** Docker-ready

## 🚀 Getting Started

### Prerequisites
- Python 3.10+
- A configured WhatsApp Business API account.

### Local Installation
1. Clone the repository and install dependencies:
```bash
   pip install -r requirements.txt
```
2. Create a .env file based on your credentials:
```bash
VERIFY_TOKEN=your_whatsapp_verify_token
ACCESS_TOKEN=your_whatsapp_access_token
```
3. 🐳 Running with Docker
```bash
docker build -t whatsapp-meta-webhook-middleware .
docker run -d -p 8000:8000 --env-file .env whatsapp-meta-webhook-middleware
```

## 🧹 Code Quality
This repository enforces modern Python standards:
- **Black:** Enforces PEP 8 code formatting.
- **Ruff:** Lightning-fast linting and import sorting.
