
# HRise - HR Management System

HRise is a lightweight, Flask-based system for securely managing employee records, file uploads, permission roles, email notifications, and administrative workflows. It is designed to operate with a static HTML front-end and a flexible backend database (SQLite by default).

## 🧠 Features
- Secure file upload system with admin-only deletion
- Email sending with custom message + file attachment (via SMTP)
- Role-based access control (admin/user)
- Login with bcrypt-encrypted passwords
- Request form with backend approval process
- Notifications, duplicate file prevention, and audit logging
- Pop-up mail body input before sending
- Full support for future expansion (e.g., JWT, PostgreSQL)

## 📁 Project Structure
```
hrise/
├── app.py
├── templates/
│   └── *.html
├── static/
│   ├── style.css
│   └── *.js
├── uploads/
├── database.db
└── utils/
    ├── email_utils.py
    ├── file_utils.py
    └── auth_utils.py
```

## ⚙️ Setup

### Prerequisites
- Python 3.10+
- Flask
- SQLite (default, PostgreSQL optional)
- SMTP Email Account (e.g., Gmail with App Password)

### Installation

```bash
pip install -r requirements.txt
python app.py
```

## 🧪 Admin Workflow
- Login via `/login`
- Access upload, delete, view, send interfaces
- Create users via DB or admin interface
- Track all actions via audit log table

## 🔐 Security
- Bcrypt password hashing
- Duplicate file detection (by hash)
- Role verification on sensitive actions
- Safe filenames (via `secure_filename`)

## 📦 Outputs
- Uploaded files directory
- Email delivery confirmation
- Request table for user onboarding
- JSON export support (planned)

## 🧰 Authors
Built by Bar Elisha with assistance from ChatGPT (OpenAI) as backend planner and code generator.
