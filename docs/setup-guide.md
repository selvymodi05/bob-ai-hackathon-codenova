# Setup Guide

> **This file is read by the automated evaluation pipeline. Be precise and complete.**

## Prerequisites

Before you begin, ensure you have the following installed:

- [ ] Python 3.11+
- [ ] Git
- [ ] An IBM Cloud account with watsonx.ai access
- [ ] IBM Bob

## Environment Variables

Copy `.env.example` to `.env` and fill in the values:

```bash
cp .env.example .env

| Variable | Description | Required |
|---|---|---|
| `WATSONX_API_KEY` | Your IBM watsonx.ai API key | Yes |
| `WATSONX_PROJECT_ID` | Your watsonx.ai project ID | Yes |
| `DATABASE_URL` | PostgreSQL connection string | Yes |
| `SLACK_WEBHOOK_URL` | Slack webhook for alerts | No |

## Installation

For your project, keep the variables that your actual code needs.

⚠️ **Never put the actual API key/password in GitHub.** Put only the variable names in `.env.example`; keep the real `.env` local.

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/selvymodi05/bob-ai-hackathon-codenova.git
cd bob-ai-hackathon-codenova
```bash


# 2. Install backend dependencies
[your command — e.g.: pip install -r requirements.txt]

# 3. Install frontend dependencies (if applicable)
[your command — e.g.: cd frontend && npm install]

# 4. Set up the database (if applicable)
[your command — e.g.: python manage.py migrate]
```

## Running the Application

```bash
# Start the backend
[your command — e.g.: uvicorn app.main:app --reload]

# Start the frontend (in a separate terminal, if applicable)
[your command — e.g.: cd frontend && npm run dev]
```

The application will be available at: `http://localhost:[PORT]`

## Running Tests

```bash
[your test command — e.g.: pytest tests/ -v]
```

## Quick Demo (Optional)

If you have a demo script or sample data to showcase the project quickly:

```bash
[e.g.: python demo/seed_demo_data.py]
[e.g.: open http://localhost:8000/demo]
```

## Troubleshooting

| Issue | Solution |
|---|---|
| [e.g., `ModuleNotFoundError`] | [e.g., Run `pip install -r requirements.txt` again] |
| [e.g., Database connection refused] | [e.g., Ensure PostgreSQL is running: `docker compose up db`] |
| [e.g., watsonx.ai 401 error] | [e.g., Check `WATSONX_API_KEY` in your `.env` file] |
