# 🛡 File Upload & Virus Scan API
---

🚀 **Need a ready-to-deploy version?**

Includes Docker, setup guide, sample responses, and full API structure.

👉 [Buy it on Gumroad](https://talabov.gumroad.com/)

---

A Flask-based API that handles secure file uploads and performs file type validation. Designed for lightweight virus scanning pipelines — ClamAV integration placeholder included.

---

## ✅ Key Features

- 📤 Upload files via POST
- 🧠 Validate file types (only allow safe MIME types)
- ⛔ Reject dangerous file extensions (e.g., `.exe`, `.bat`)
- 🔒 Max upload size: 5MB
- 🧪 Modular Flask structure with endpoints in `routes/`
- 🐳 Docker-ready

---

## 🚀 Endpoint

### Upload & Scan File

**POST** `/upload`

**Request (form-data):**
- `file`: any file (txt, pdf, docx, xlsx, png, jpg)

**Responses:**

✅ **Success:**
```json
{
  "filename": "report.pdf",
  "status": "unknown",
  "details": "Virus scan skipped (ClamAV not available)"
}
```

❌ **Errors:**
```json
{ "error": "No file part" }

{ "error": "No selected file" }

{ "error": "File type not allowed" }

{ "error": "Forbidden file type" }

{ "error": "Error occurred while processing file." }
```

---

## ⚙️ Requirements

```bash
pip install -r requirements.txt
```

- Flask

---

## 🖥 How to Run

```bash
python app.py
```

Server runs at:
```
http://127.0.0.1:5000/
```

Or with Docker:
```bash
docker build -t file-upload-virus-api .
docker run -p 5000:5000 file-upload-virus-api
```

---

## 🧪 Example Screenshots

- ✅ Successful upload
- ⛔ File type rejected
- 🐞 Upload error simulation

> See `/screens/` for Postman previews

---

## 💼 Ready-to-Use Version

You can get a ZIP with full code, Dockerfile, and documentation:

👉 [Buy it on Gumroad](https://talabov.gumroad.com/)

---

## 📬 Contacts

- Email: talabov.ali72@gmail.com  
- Telegram: [@talabovali](https://t.me/talabovali)

---

**Need this in another language/stack (Node.js, Go, etc)?**  
Custom dev available — just reach out.
