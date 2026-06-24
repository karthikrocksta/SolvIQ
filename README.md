# SolvIQ — Real-Time Problem Solver

A multi-function AI-powered problem solver built for everyone — with voice input, user profiles, history export, and a live agent dashboard.

## Features

- **6 problem categories** — Life & Decisions, Tech & Coding, Health & Wellness, Creative & Writing, Legal & Financial, Math & Logic
- **Voice input** — speak your problem using the microphone button (Chrome/Edge)
- **User profiles** — create profiles with name, age group, and preferred tone; saved to localStorage
- **History export** — download your conversation history as JSON, Markdown, or CSV
- **Agent dashboard** — live metrics for 4 named AI agents (Advisor-1, DevBot-2, Wellness-3, Muse-4)
- **Multi-turn conversations** — full session memory within each category
- **Dark-mode interface** — clean, accessible dark UI

## Deploy to GitHub Pages

### One-time setup

1. **Fork or clone** this repository
2. Go to your repo → **Settings** → **Pages**
3. Under "Build and deployment", set **Source** to `GitHub Actions`
4. Add your Anthropic API key as a repository secret:
   - Go to **Settings** → **Secrets and variables** → **Actions**
   - Click **New repository secret**
   - Name: `ANTHROPIC_API_KEY`, Value: your key from [console.anthropic.com](https://console.anthropic.com)

> **Important:** The API key is used client-side in this demo. For production, proxy API calls through a backend server to keep your key secure.

### Push and deploy

```bash
git add .
git commit -m "Deploy SolvIQ"
git push origin main
```

GitHub Actions will automatically build and deploy. Your app will be live at:
`https://<your-username>.github.io/<repo-name>/`

## Local development

Just open `index.html` in Chrome or Edge. No build step needed — it's a single HTML file.

```bash
# Optional: serve locally
npx serve .
```

## Tech stack

- Vanilla HTML/CSS/JS — zero dependencies, zero build step
- Anthropic Claude API (`claude-sonnet-4-6`)
- Web Speech API for voice input
- LocalStorage for profiles

## Project structure

```
solviq/
├── index.html              # The entire app
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Pages auto-deploy
└── README.md
```

## License

MIT
