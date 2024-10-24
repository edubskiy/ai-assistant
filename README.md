# AICA v1 - AI Assistant (Team Proxima)

## Vision
Meet our next-generation AI Assistant - a breakthrough in intelligent customer support automation. Powered by state-of-the-art machine learning, it masters the art of data classification across any domain. Whether handling customer inquiries, technical issues, or complex requests, our assistant delivers precise, contextual responses while continuously learning and improving. It's not just a support tool; it's your intelligent partner in delivering exceptional customer experiences.

## Overview
AICA AI Assistant:
- Processes and classifies user requests with high accuracy
- Provides automated responses to FAQs
- Resolves common technical issues
- Intelligently routes complex cases to human operators
- Continuously learns from interactions

## Demo Access
- API Documentation: http://176.114.66.132:8000/docs
- UI Interface: http://89.169.151.229/

## Quick Start

```bash
# 1. Clone Repository
git clone https://github.com/proxima-ai-hub/ai-assistant.git

# 2. Install LLama3.1
cd ai-assistant
curl -fsSL https://ollama.com/install.sh | sh
ollama create temp0:latest -f Modefile

# 3. Install Dependencies
pip install poetry
poetry install

# 4. Install Uvicorn
pip install uvicorn

# 5. Start Qdrant
docker compose up qdrant -d

# 6. Launch Backend
uvicorn app:app --host 0.0.0.0 --port 8000

# 7. Launch Frontend
cd frontend
npm build && npm start
```

## Tech Stack
- Frontend: AngularJS
- Backend: FastAPI, LLAMA 3.1:8B
- Database: Qdrant, Redis
- ML Tools: LangGraph, SentenceTransformer

## Branching Strategy

- Main: `main` (always deployable)
- Features: `feature/description`
- Bugfixes: `bugfix/id-description`
- Hotfixes: `hotfix/description`
- Experiments: `experiment/description`

Development follows trunk-based workflow with frequent integration into main branch.
