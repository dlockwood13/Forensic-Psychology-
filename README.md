# Forensic-Psychology-
# ⚓ Anchor — A Forensic Psychology Practitioner Companion (UK)

> A pocket handbook and practitioner toolkit for UK forensic psychologists.
> Mobile-first, offline-capable, privacy-respecting. Your data never leaves your device.

[![Live demo](https://img.shields.io/badge/demo-live-2c5f7c?style=flat-square)](https://dlockwood13.github.io/anchor/)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](LICENSE)
![Status](https://img.shields.io/badge/status-v1.0-success?style=flat-square)

![Anchor screenshot](assets/og-image.png)

## What it is

Anchor is a single-page web application (PWA) that combines:

- A **14-chapter handbook** covering the UK forensic psychology journey — from MSc through HCPC registration to growing into the role.
- A **practitioner toolkit** — CPD logger, supervision log, risk formulation builder, reflection journal, report templates, and a searchable reference index.
- A **visual qualification flowchart** showing Route A (university doctorate) and Route B (BPS Stage 2 + trainee post) converging at HCPC registration.

Designed for **everyday use on a phone** — calm typography, large tap targets, native-feeling navigation.

## Who it's for

- MSc forensic psychology students mapping the road ahead
- Trainee forensic psychologists building portfolios
- Assistant psychologists preparing for Stage 2 / DForenPsy applications
- Qualified practitioners wanting a frictionless CPD / supervision log
- Anyone curious about the UK forensic psychology pathway

## Features

| Tool | What it does |
| --- | --- |
| 📚 **CPD Logger** | HCPC-aligned entries with hours, type, standard, outcomes. CSV export for audit. |
| 💬 **Supervision Log** | Clinical, managerial, peer, group, external sessions with searchable history. |
| 🧩 **Formulation Builder** | 5Ps framework + static/dynamic factors, risk scenarios, management plan. Generates copy-ready text. |
| 📓 **Reflection Journal** | Brief Gibbs-style entries with mood tracking. |
| 📄 **Report Templates** | Skeletons for court reports, risk assessments, clinical letters, parole reports. |
| 🔍 **Reference Index** | Searchable, filtered cards for assessment tools, frameworks, legislation, bodies, settings, programmes. |

## Privacy

- **No accounts, no servers, no analytics.**
- All data lives in your browser's `localStorage`, on the device you use.
- Clearing your browser data or switching devices will not carry data across — use **Export All Data** regularly to keep a backup.
- Never enter identifiable client information. Use initials or case codes.

## Tech stack

- **Vanilla HTML / CSS / JavaScript** — no frameworks, no build step
- **CSS Custom Properties** for theming
- **localStorage** for persistence
- **Service Worker** for offline use
- **Web App Manifest** for installable PWA

Designed for **GitHub Pages** — drop into a repo, enable Pages, done.

## Getting started

### Run locally

Clone the repo and open `index.html` in a browser, or serve from any static server:

\`\`\`bash
git clone https://github.com/dlockwood13/anchor.git
cd anchor
# Serve with any static server (e.g. Python)
python3 -m http.server 8080
# Visit http://localhost:8080
\`\`\`

### Deploy to GitHub Pages

1. Push to a GitHub repo (e.g. `anchor` or `Forensic-Psychology-`)
2. Repo Settings → Pages → Build from `main` branch, root folder
3. Wait ~30 seconds. Visit `https://<your-username>.github.io/<repo-name>/`

### Install as a PWA

- **iOS Safari:** Share → Add to Home Screen
- **Android Chrome:** ⋮ menu → Install app
- **Desktop Chrome/Edge:** Install icon in the address bar

## Project structure

\`\`\`
anchor/
├── index.html              # Shell (loads CSS + JS modules)
├── manifest.webmanifest    # PWA manifest
├── service-worker.js       # Offline cache
├── assets/                 # Icons, OG image
├── styles/                 # Tokens, base, components, views
├── scripts/                # App logic (modular)
│   └── tools/              # One file per tool
└── data/                   # Chapter content, reference data, templates
\`\`\`

See [STRUCTURE.md](STRUCTURE.md) for a full breakdown.

## Customising

### Change the colour palette
Edit `styles/tokens.css`. All colours are CSS variables (`--primary`, `--accent`, chapter pastels).

### Add or edit a chapter
Open `data/chapters.js`. Each chapter is an object with `id`, `color`, `title`, `tag`, and `html` (template string).

### Add reference entries
Open `data/reference.js`. Each entry has `cat`, `name`, `desc`.

### Add a new report template
Open `data/templates.js`. Each template has a `title` and an array of `[fieldId, fieldLabel]` pairs.

## Roadmap

- [ ] Onboarding flow for first launch
- [ ] Dark mode toggle
- [ ] Streak tracking for reflection / CPD
- [ ] Push notifications (weekly reflection reminders)
- [ ] Custom chapter editing (Notion-style)
- [ ] Multi-language support

## Disclaimer

Anchor is a **reference and personal practitioner tool**, not legal or professional advice. Always verify current requirements with the HCPC, BPS, and your employer. Registration rules, pay bands, and guidelines change.

## Contributing

Spotted something out of date or wrong? Open an issue or PR. Forensic psychology evolves quickly — this handbook is meant to be a living document.

## License

MIT — see [LICENSE](LICENSE).

## Credits

Built by [Dan Lockwood](https://danlockwood.co.uk) · 2026
