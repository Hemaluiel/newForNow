# FinSight — Bank Statement Analyzer

A full-stack web app to analyze bank statements with AI.
**Stack:** Python + FastAPI (backend) · HTML/CSS/JS (frontend) · SQLite (database) · Claude AI

---

## Project structure

```
bankanalyzer/
├── backend/
│   ├── main.py            ← FastAPI app (all backend logic)
│   └── requirements.txt   ← Python dependencies
├── frontend/
│   ├── index.html         ← Login / Register page
│   └── dashboard.html     ← Main dashboard (upload, charts, history)
├── .env.example           ← Environment variables template
└── README.md
```

---

## Features

- **PDF parsing** — pdfplumber extracts text from digital PDFs (not scanned)
- **AI analysis** — Claude categorizes debits, finds top 5, writes insights
- **Dashboard** — doughnut chart, horizontal bar chart, metric cards, top 5 list
- **History** — every analysis is saved; click to reload any past result
- **Deploy-anywhere** — single Python file backend, no complex infra needed

---

## Notes

- Scanned/image PDFs won't work — only text-based PDFs (standard bank exports)
- SQLite is zero-config and works on all platforms; swap for PostgreSQL for scale
- The Anthropic API key is used server-side — never exposed to the browser
