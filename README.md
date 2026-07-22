# 📄 GenDoc-AI-Studio

## AI-Powered Document Generation Platform

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.104+-green.svg)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/React-18.0+-blue.svg)](https://reactjs.org/)
[![Tailwind](https://img.shields.io/badge/Tailwind-3.3+-cyan.svg)](https://tailwindcss.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen.svg)]()

---

## 🚀 Overview

**GenDoc-AI-Studio** is an intelligent document generation platform that combines **Google's Gemini AI** with **Retrieval-Augmented Generation (RAG)** to automatically create professional business documents from structured inputs. The system transforms raw data into polished contracts, invoices, policies, proposals, compliance reports, and technical manuals with minimal human intervention.

> **🎓 Educational Project:** This is a practice project developed to demonstrate full-stack development skills, AI integration, and modern software architecture. Not intended for production use.

---

## ✨ Key Features

### 🤖 **Smart Document Generation**
- Generate 6+ document types: Contracts, Invoices, Policies, Proposals, Compliance Reports, Technical Manuals
- AI-powered content enhancement using Gemini API
- Context-aware content generation
- Real-time document preview and editing
- Batch document generation

### 📋 **Template Management**
- 50+ Professional templates across 6 categories
- Dynamic variable substitution using Jinja2
- Template version control
- Custom template creation and editing
- Category-based organization
- Template preview and testing

### 🧠 **RAG-Powered Knowledge Base**
- Upload and process multiple document formats (PDF, DOCX, TXT)
- Intelligent text chunking and embedding generation
- Semantic search for relevant context
- Vector database integration (ChromaDB)
- Enhanced document generation with retrieved knowledge
- Context-aware content enrichment

### 📄 **PDF Generation & Export**
- Professional PDF rendering with ReportLab
- Brand customization (logo, colors, fonts)
- Multiple export formats (PDF, DOCX, HTML)
- Batch document generation
- Download and sharing capabilities
- Print-ready output

### 🎨 **Modern User Interface**
- Clean, professional dashboard with real-time stats
- Drag-and-drop template builder
- Real-time content preview
- Dark/Light mode support
- Responsive design (works on all devices)
- Interactive charts and analytics
- Progress tracking during generation
- Toast notifications for user feedback

### 👥 **User Management**
- Secure authentication with JWT
- User roles (Admin, Manager, Editor, Viewer)
- Document ownership and access control
- Activity logging and audit trails
- Profile management
- Password reset functionality

---

## 🏗️ Technology Stack

### **Backend Technologies**
| Technology | Purpose | Version |
|------------|---------|---------|
| **Python** | Programming Language | 3.10+ |
| **FastAPI** | Web Framework | 0.104.0+ |
| **SQLAlchemy** | ORM | 2.0.23+ |
| **PostgreSQL** | Database | 14+ |
| **Jinja2** | Template Engine | 3.1.2+ |
| **ReportLab** | PDF Generation | 4.0.7+ |
| **ChromaDB** | Vector Database | 0.4.22+ |
| **Sentence Transformers** | Embeddings | 2.2.2+ |
| **Gemini API** | LLM Integration | 0.3.2+ |
| **Redis** | Caching | 6.0+ |
| **Celery** | Async Tasks | 5.3.4+ |

### **Frontend Technologies**
| Technology | Purpose | Version |
|------------|---------|---------|
| **React** | UI Framework | 18.2.0+ |
| **Vite** | Build Tool | 4.5.0+ |
| **Redux Toolkit** | State Management | 1.9.7+ |
| **Tailwind CSS** | Styling | 3.3.6+ |
| **Framer Motion** | Animations | 10.16.5+ |
| **Recharts** | Data Visualization | 2.8.0+ |
| **React PDF** | PDF Rendering | 7.2.0+ |
| **Axios** | API Calls | 1.6.2+ |
| **React Hook Form** | Form Management | 7.47.0+ |
| **Socket.io Client** | WebSocket Support | 4.5.4+ |

### **DevOps & Tools**
- **Docker** & **Docker Compose** (Containerization)
- **Git** (Version Control)
- **GitHub Actions** (CI/CD)
- **Alembic** (Database Migrations)
- **Pytest** (Testing)
- **Black** & **Flake8** (Code Quality)
- **ESLint** & **Prettier** (Frontend Linting)

---

## 📊 Project Structure

---

## 🚀 Quick Start

### **Prerequisites**

Before you begin, ensure you have the following installed:

- **Python** 3.10 or higher
- **Node.js** 18.0 or higher
- **PostgreSQL** 14 or higher
- **Redis** 6.0 or higher (optional for caching)
- **Git** (for version control)
- **Docker** (optional, for containerization)

### **Environment Setup**

1. **Clone the repository:**
```bash
git clone https://github.com/vishakha2121/GenDoc-AI-Studio.git
cd GenDoc-AI-Studio

# Navigate to backend directory
cd backend

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up database
createdb gen_doc_db
alembic upgrade head
python app/database/init_db.py

# Run the server
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

# Server runs at: http://localhost:8000
# API docs at: http://localhost:8000/docs

# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Run development server
npm run dev

# Server runs at: http://localhost:5173