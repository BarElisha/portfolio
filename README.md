# Ballgorithm - AI Video Analysis System

Ballgorithm is an AI-powered backend system that processes football match videos, segments them into short clips, summarizes each segment using OpenAI's GPT-4, analyzes the summaries for tactical insights, and produces structured outputs like PDF and PPTX files.

## 🧠 Features
- Segment video files into 10-second chunks
- Generate textual summaries using LLM (GPT-4)
- Analyze summaries for tactical patterns and confidence scores
- Fetch external data (e.g., team info) via a configurable API gateway
- Export insights as PDF or PowerPoint slides
- Docker-ready deployment

## 📁 Project Structure
```
app/
├── ai/
│   ├── video_segmenter.py
│   ├── segment_summarizer.py
│   ├── text_analyzer.py
│   └── render_outputs.py
├── gateway/
│   └── gateway_connector.py
├── models.py
├── config.py
├── jwt_utils.py
...
```

## ⚙️ Setup

### Prerequisites
- Python 3.10+
- PostgreSQL
- Docker (optional but recommended)
- OpenAI API Key (save in `.env` as `OPENAI_API_KEY`)

### Installation

```bash
pip install -r requirements.txt
cp .env.template .env
flask db upgrade
flask run
```

### With Docker
```bash
docker-compose up --build
```

## 🧪 Running Tests
```bash
python tests/test_endpoints.py
```

## 📦 Outputs
- JSON (insights + probabilities)
- PDF reports
- PPTX slide decks

## 🔒 Security
- JWT-based auth
- SQLAlchemy ORM (no raw SQL)
- File validation for uploads
- Placeholder-based queries to prevent SQL injection

## 🧰 Authors
Built by Bar Elisha and OpenAI Backend AI Assistant.