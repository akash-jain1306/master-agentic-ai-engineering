# Setup

## Required Tools

- Git
- Python 3.11 or newer
- A code editor
- A GitHub account
- Terminal access

## Recommended Python Workflow

Use a virtual environment for each project:

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
```

## Environment Variables

Store secrets in `.env` files and never commit them.

Example:

```text
OPENAI_API_KEY=replace_me
```

The repository `.gitignore` already excludes `.env` files.

## Git Workflow

For each learning session:

```bash
git status
git add .
git commit -m "Complete chapter exercise"
git status
```

Use small commits. A strong portfolio shows the process, not only the final result.

