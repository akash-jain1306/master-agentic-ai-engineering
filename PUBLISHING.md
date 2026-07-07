# Publishing Guide

Use this guide to publish the course repository to GitHub.

## 1. Create the GitHub Repository

Create an empty GitHub repository named:

```text
master-agentic-ai-engineering
```

Recommended settings:

- Visibility: Public if you want this to become a portfolio artifact
- Initialize with README: No
- Add `.gitignore`: No
- Add license: Choose deliberately before publishing

## 2. Connect Local Repo to GitHub

From this local repository:

```bash
git remote add origin https://github.com/YOUR_USERNAME/master-agentic-ai-engineering.git
git branch -M main
git push -u origin main
```

If you use SSH:

```bash
git remote add origin git@github.com:YOUR_USERNAME/master-agentic-ai-engineering.git
git branch -M main
git push -u origin main
```

## 3. GitHub Repository Setup

After pushing:

- Add a concise repository description.
- Add topics such as `ai-engineering`, `llm`, `agents`, `rag`, `mcp`, `langgraph`, `crewai`, `openai`.
- Enable Issues.
- Enable Discussions if you want to track questions and reflections.
- Pin the repository on your GitHub profile.

## 4. Publishing Quality Checklist

Before announcing the repo:

- The main README explains the purpose and learning path.
- `COURSE.md` explains how to study the course.
- `PROGRESS.md` shows what is complete and what is planned.
- `resources/` credits external resources.
- At least one chapter has complete theory, exercises, labs, solutions, and interview prep.
- At least one project has setup instructions and evaluation cases.

## 5. Important Copyright Note

Do not copy paid course scripts, transcripts, slides, or proprietary exercise text into this repository. Use public resources for references and write original explanations, labs, exercises, and projects.

