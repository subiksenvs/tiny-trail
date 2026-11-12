# Tiny Trail Journal

Keep a searchable journal with mood tags, prompts, and weekly reflections.

## Features
- Flask JSON API and SQLite persistence for create, edit, delete, search, and summary.
- Responsive workspace UI with editable saved records.
- Domain-specific AI coach: deterministic demo mode by default; optional server-side OpenAI Responses API.
- Environment configuration; no API key is committed.

## Run locally
```powershell
py -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
Copy-Item .env.example .env
python app.py
```
Open http://127.0.0.1:5000. Add OPENAI_API_KEY to `.env` to enable live coaching.

## API
`GET /api/items?q=...`, `POST /api/items`, `PUT /api/items/:id`, `DELETE /api/items/:id`, `GET /api/summary`, `POST /api/coach`.

Stack: Flask 3 · SQLite · Python.
