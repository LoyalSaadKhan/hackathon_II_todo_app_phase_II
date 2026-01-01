# Todo App – Phase II

**A Full-Stack Web Application with Authentication**

Phase II of **"The Evolution of Todo: From CLI to Distributed Cloud-Native Systems"** transforms a single-user CLI todo app into a secure, multi-user, full-stack web application with authentication, persistent storage, and a modern frontend.

---

## 🚀 Overview

This project demonstrates real-world full-stack application architecture using modern tools and best practices. Each authenticated user manages a private task list backed by a serverless PostgreSQL database and a secure REST API.

---

## ✨ Features

- User registration & login (email/password)
- Secure JWT-based authentication
- Private task lists per user
- Create, read, update, and delete todos
- Mark tasks as complete or incomplete
- Responsive, modern UI

---

## 🛠 Tech Stack

### Frontend
- **Framework:** Next.js (App Router)
- **Language:** TypeScript (strict)
- **Styling:** Tailwind CSS
- **Authentication:** Better Auth

### Backend
- **Framework:** FastAPI
- **Language:** Python 3.11+
- **ORM:** SQLModel (async)
- **Auth:** JWT verification

### Database
- **PostgreSQL:** Neon (serverless)

---

## 📦 Prerequisites

- Node.js 18+
- Python 3.11+
- npm / pnpm / yarn
- pip / uv
- Neon PostgreSQL account

---

## ⚙️ Installation

### 1️⃣ Clone the Repository

```bash
git clone <repository-url>
cd Todo_App
```

---

### 2️⃣ Backend Setup

```bash
cd backend
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env
```

Edit `.env` with your credentials.

---

### 3️⃣ Frontend Setup

```bash
cd frontend
npm install   # or pnpm install
cp .env.example .env.local
```

---

## 🔐 Environment Variables

### Backend (`.env`)

```env
DATABASE_URL=postgresql+asyncpg://user:password@host.neon.tech/db?sslmode=require
BETTER_AUTH_SECRET=your-secret
CORS_ORIGINS=http://localhost:3000
```

### Frontend (`.env.local`)

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
BETTER_AUTH_SECRET=your-secret
BETTER_AUTH_URL=http://localhost:3000
```

---

## ▶️ Running the App

### Start Backend

```bash
cd backend
uvicorn src.main:app --reload --port 8000
```

### Start Frontend

```bash
cd frontend
npm run dev
```

Visit: **http://localhost:3000**

---

## 🧩 Project Structure

```
Todo_App/
├── frontend/
├── backend/
├── specs/
├── README.md
```

---

## 🔌 API Overview

| Method | Endpoint | Description |
|------|---------|-------------|
| GET | /api/tasks | List user tasks |
| POST | /api/tasks | Create task |
| PUT | /api/tasks/{id} | Update task |
| DELETE | /api/tasks/{id} | Delete task |
| PATCH | /api/tasks/{id}/complete | Toggle status |

All endpoints require `Authorization: Bearer <JWT>`.

---

## 🏗 Architecture

```
Next.js (UI)
   ↓
Better Auth (JWT)
   ↓
FastAPI (REST API)
   ↓
Neon PostgreSQL
```

---

## 🔒 Security

- JWT-secured API
- User-level data isolation
- Password hashing via Better Auth
- Ownership verification on all endpoints

---

## 📚 Development Approach

This project follows **spec-driven development** using Spec-Kit Plus.

---

## 🧭 Roadmap

**Phase III (Planned):**
- Real-time updates
- Team collaboration
- AI-assisted task management
- Cloud-native deployment

---

## 📄 License

Educational project for learning modern full-stack development.

---

## 📌 Version

- Phase: II
- Version: 1.0.0
- Date: December 2025
