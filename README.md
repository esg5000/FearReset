# Fear Reset AI

A personal self-help web app for fear-of-heights work: guided recall, rewind visualization, bilateral stimulation, height ladder, body mapping, self-hypnosis, dream rehearsal, and an AI coach.

## Deploy to Vercel

1. Push this repo to GitHub (see below).
2. Import the repo at [vercel.com/new](https://vercel.com/new).
3. Add an environment variable:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** your Anthropic API key (`sk-ant-…`)
4. Deploy. No build command or output directory needed — Vercel serves `index.html` and the `/api/chat` serverless function automatically.

Users do not need to enter an API key in the app when the server variable is set.

## Local development

```bash
npm i -g vercel
vercel dev
```

Copy `.env.example` to `.env.local` and set `ANTHROPIC_API_KEY` for the AI coach locally.

## GitHub

```bash
git init
git add .
git commit -m "Initial commit: Fear Reset AI"
gh repo create FearReset --public --source=. --push
```

Or create the repo manually on GitHub, then:

```bash
git remote add origin https://github.com/YOUR_USERNAME/FearReset.git
git push -u origin main
```

## Project structure

| Path | Purpose |
|------|---------|
| `index.html` | Full single-page app |
| `api/chat.js` | Vercel serverless proxy for Anthropic (keeps API key off the client) |
| `vercel.json` | Security headers |

## Privacy

Session data is stored in the browser (`localStorage`). Nothing is sent to a server except AI coach requests.

## Disclaimer

This is a personal self-help tool, not therapy or medical care.
