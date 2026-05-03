# PRD Agent
**A guided product thinking system for early-stage founders.**
Not a chatbot. A structured thinking tool that helps you clarify a rough idea and turn it into a real Product Requirements Document — through adaptive, stage-by-stage questioning.
🔗 **Live demo:** `https://anushka644.github.io/PRD-agent/`
---
## What it does
Most founders jump straight to solutions before understanding the problem. PRD Agent forces structured thinking through 7 stages:
**Problem → Users → Pain Points → Solution → Features → Metrics → Overview**
At each stage, the agent asks one sharp question at a time, pushes back on vague answers, and builds your PRD progressively in real time.
---
## Features
| Feature | Description |
|---|---|
| 🎯 **Guided PM mode** | Deep stage-by-stage thinking with follow-up probing |
| ⚡ **Founder mode** | Fast, assumptive questioning — confirms rather than asks |
| 📝 **Quick Draft mode** | Instant full PRD from a rough idea |
| 💡 **Aha moment** | AI-generated reframing sentence after users + problem are defined |
| 🧠 **Key Insight** | Non-obvious synthesis of what the product really is at completion |
| 📋 **Live PRD panel** | Updates in real time with confidence scoring per section |
| 🔍 **Reflection checkpoints** | Mid-session reviews to validate understanding |
| ↗️ **Rich HTML export** | AI-enriched, beautifully formatted PRD document (print to PDF) |
| 💾 **Session persistence** | All sessions saved to localStorage — resume any previous session |
| ✏️ **Editable product name** | Suggested by AI, editable inline from the first response |
---
## How to use
### Option 1 — Live (no install)
Visit the GitHub Pages link above. Works in any modern browser.
### Option 2 — Local
```bash
# Just download index.html and open it
open index.html
```
No server, no npm, no dependencies. Single HTML file.
---
## Tech stack
- **Vanilla HTML/CSS/JS** — zero build step, zero dependencies
- **Claude Sonnet 4** via Anthropic API (primary — works inside claude.ai)
- **Llama 3.3 70B** via Groq API (fallback — works when opened locally)
- **jsPDF** via CDN — for PDF rendering
- **Google Fonts** — Inter + DM Serif Display
---
## Architecture
Everything lives in a single `index.html` file:
```
index.html
├── CSS — light mode design system, component styles
├── HTML — header, stage rail, chat panel, PRD panel, sessions sidebar
└── JS
├── Stage system (7 stages, adaptive progression)
├── System prompts (Guided PM, Founder, Quick Draft)
├── API layer (Anthropic → Groq fallback)
├── PRD renderer (confidence scoring, flash updates)
├── Session persistence (localStorage)
└── Export (AI-enriched HTML document)
```
---
## API keys
The file includes a Groq API key for local use. To use your own:
1. Get a free key at [console.groq.com](https://console.groq.com)
2. Replace `GROQ_KEY` near the top of the script section in `index.html`
When running inside **claude.ai**, the Anthropic API is used automatically — no key needed.
---
## Screenshots
> <img width="2848" height="1344" alt="image" src="https://github.com/user-attachments/assets/b0c212cb-6be8-455e-8d37-f6c2f14b13f3" />
> <img width="2842" height="1358" alt="image" src="https://github.com/user-attachments/assets/aef7b063-54c4-4ea8-9b43-ebaee1a1fe50" />
---
## Roadmap
- [ ] Sharable PRD links
- [ ] Team collaboration mode
- [ ] Custom stage templates
- [ ] Notion / Linear export
---
## License
MIT — use it, fork it, build on it.
---
Built with [Claude](https://claude.ai) · Designed for founders who think before they build

