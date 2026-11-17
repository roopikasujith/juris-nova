# Juris Nova ⚖️

### AI-Driven Legal Compliance and Document Automation for Startups

Juris Nova is a web-based platform that brings legal and business support for early-stage Indian startups into one place. Many startups have no in-house legal team and cannot easily afford legal consultation, which leads to missed compliance deadlines, unclear contracts and uncertainty about government schemes. Juris Nova combines AI-assisted tools with transparent rule-based features to help founders.

> ⚠️ **Disclaimer:** Juris Nova provides information and decision support only. It is not legal, tax or financial advice and does not replace a qualified legal professional.

---

## ✨ Features

### Working in the current prototype (Phase 1)

- 🔐 User registration, login and startup profile management
- 🏛️ Rule-based government scheme matcher (JSON rules, with pass/fail shown for each condition)
- 📅 Compliance calendar with next due dates and days remaining (GST, ROC, PF and more)
- 💬 Source-grounded legal Q&A with citations (basic keyword retrieval, optional Mistral API)

### Planned

- 📚 Hybrid retrieval (FAISS + BM25 + cross-encoder reranking) with an answer verification step
- 🌐 Regional-language support and a local Ollama fallback
- 📄 Legal document summarizer and risk analyzer (OCR + clause classification)
- 📈 Startup success predictor with explainable factors (SHAP)
- 📝 Document generator for NDAs, MoUs, RTI requests and pitch decks
- 🔔 Automated deadline reminders

---

## 🛠️ Tech Stack

| Area | Technologies |
|------|--------------|
| Backend | Python, Flask |
| Database | SQLAlchemy (SQLite in development, PostgreSQL for deployment) |
| Frontend | Server-rendered HTML templates, CSS |
| Security | Werkzeug password hashing, Flask sessions, CSRF protection |
| AI / ML | Mistral (with Ollama fallback), FAISS, BM25, Tesseract OCR, XGBoost, Random Forest |

---

## 🏗️ Architecture

The system is modular, with four layers:

1. **Presentation layer:** web frontend (login, profile, dashboard, scheme matcher, compliance calendar, legal Q&A)
2. **Application layer:** Flask backend (authentication, profile management, rule engine, module integration)
3. **AI / ML layer:** RAG-based Q&A, evaluation agent, document analysis, success predictor, document generator
4. **Data layer:** relational database, JSON rule files, legal source documents and vector index

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/roopikasujith/juris-nova.git
cd juris-nova
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Set environment variables

```bash
# Example (use your own values; never commit real keys)
export SECRET_KEY="your-secret-key"
export DATABASE_URL="sqlite:///app.db"
export MISTRAL_API_KEY="your-mistral-api-key"   # optional
```

### 4. Run the app

```bash
python app.py
```

Then open `http://localhost:5000` in your browser.

---

## 🗺️ Roadmap

Planned from July 2026 to January 2027:

- [x] Literature survey and problem analysis
- [x] Requirement gathering and scope finalization
- [x] Technology research and system design
- [x] Database, AI and UI/UX model design
- [ ] RAG Q&A and document analysis
- [ ] Startup success predictor and scheme matcher
- [ ] Frontend and dashboard development
- [ ] Integration and testing
- [ ] Document generator and reminders
- [ ] Documentation and phase review

---

## 👩‍💻 Team

B.Tech Computer Science and Engineering, SCMS School of Engineering and Technology (APJ Abdul Kalam Technological University)

- Roopika Sujith
- Rushdha Mariyam M
- Sandra Subramanian
- Shana Thayyil

**Project Guide:** Ms. Reeny Zackarias, Assistant Professor, Department of Computer Science and Engineering

---

## 📬 Contact

[Roopika Sujith on LinkedIn](https://www.linkedin.com/in/roopika-sujith-4bb688331)
