# CLAUDE.md

This file provides guidance for AI assistants working in this repository.

## Project Overview

**teacozy** is a static frontend web project. The codebase is in its initial scaffolding phase — the HTML and CSS files exist but are currently empty placeholders awaiting implementation.

## Repository Structure

```
teacozy/
├── CLAUDE.md               # This file
├── index.html              # Root HTML entry point
└── content/
    └── css/
        └── index.css       # Main stylesheet
```

## Tech Stack

- **HTML5** — primary markup
- **CSS3** — styling via `content/css/index.css`
- No JavaScript framework, build tool, or package manager is configured

## Development Workflow

There is no build step. This is a plain static site. To preview locally, serve the root directory with any static file server:

```bash
# Python (built-in)
python3 -m http.server 8000

# Node.js (if available)
npx http-server . -p 8000
```

Then open `http://localhost:8000` in a browser.

## Key Conventions

- File names use lowercase with no spaces (e.g., `index.html`, `index.css`)
- CSS lives under `content/css/`
- The single HTML entry point is `index.html` at the project root

## Testing

No test framework is configured. There are no automated tests.

## CI/CD

No CI/CD pipeline is configured.

## Git Branches

| Branch | Purpose |
|--------|---------|
| `master` | Stable / production state |
| `claude/*` | AI-driven feature/documentation branches |

## What Still Needs to Be Done

- Populate `index.html` with page structure
- Add styles to `content/css/index.css`
- Consider adding a `README.md` for human-facing project documentation
- Add `.gitignore` if build artifacts or editor files are introduced
- Add a `<title>` and meta tags to `index.html` once content is defined
