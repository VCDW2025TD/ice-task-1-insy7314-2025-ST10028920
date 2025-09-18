# ICE Task 1 – INSY7314 – SecureBlog (HTTPS/TLS)

## 📌 Overview
This project demonstrates how to enable **SSL/TLS (HTTPS)** in a full-stack application with a **Node.js backend (Express)** and a **Vite React frontend**.  
It uses self-signed certificates for local development only.

## 🗂️ Project Structure
SecureBlog/
backend/ # Express API (secured with HTTPS)
ssl/ # Self-signed dev certificates (ignored in git)
server.js
app.js
frontend/ # Vite + React app (served over HTTPS)
ssl/ # Same dev certificates (copied from backend)
vite.config.js
ssl_research.md # Research summary on SSL/TLS
reflection.md # Reflection questions answered
.gitignore # Ensures .pem, node_modules, dist, .env are ignored

## 🚀 How to Run

### Backend
```bash
cd backend
npm install
npm run dev
Visit: https://localhost:5000/health

👉 Accept the browser warning for the self-signed certificate.

Expected response:
{ "status": "ok", "https": true }
Frontend:
cd frontend
npm install
npm run dev
Visit: https://localhost:5173

👉 Accept the browser warning for the self-signed certificate.
You should see the Vite + React starter page.

📄 Deliverables

ssl_research.md → 4–6 sentence summary of SSL/TLS importance.

reflection.md → Reflection answers on HTTPS setup, issues, and production deployment.

HTTPS enabled on both backend and frontend.

⚠️ Notes

Self-signed certs are for development only.

In production, a trusted CA (e.g., Let’s Encrypt) must be used.

---

### Next Step for You
1. Open **PowerShell**  
2. Run:
```powershell
cd $HOME\SecureBlog
notepad README.md
Paste the above text → Save → Close

Commit + push:
git add README.md
git commit -m "docs: add project README"
git push
