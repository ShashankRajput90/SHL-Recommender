# SHL Assessment Recommendation Agent

A conversational AI agent that helps hiring managers find relevant SHL assessments.

## Local Setup

```bash
python -m venv .venv
.venv\Scripts\activate        # Windows
pip install -r requirements.txt
```

## Running Locally

```bash
# 1. Build the FAISS index (only needed once)
python embeddings/build_index.py

# 2. Start the API server
uvicorn app.main:app --reload
```

## API Endpoints

- `GET  /health` — Health check
- `POST /chat`   — Conversational recommendation endpoint
- `GET  /docs`   — Interactive Swagger UI

## Environment Variables

Create a `.env` file:
```
GROQ_API_KEY=your_key_here
```
