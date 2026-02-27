# Senior Product Leader — Personal Site

A clean, static personal website for a Senior Product Manager seeking Senior Director / Group PM opportunities. Built with HTML and CSS only — no frameworks, no build step.

---

## Local Preview

Serve the root directory with any static file server:

```bash
# Python (built-in — recommended)
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000) in a browser.

If Python isn't available:

```bash
# Node.js (install once with: npm install -g http-server)
npx http-server . -p 8000
```

---

## Deploy to GitHub Pages

### Option 1 — Push `master` branch (simplest)

1. Go to your repo on GitHub.
2. Click **Settings → Pages**.
3. Under **Source**, select **Deploy from a branch**.
4. Choose `master` (or `main`) and `/ (root)`.
5. Click **Save**.

Your site will be live at `https://<your-github-username>.github.io/<repo-name>/` within a minute or two.

### Option 2 — Custom domain

1. Complete Option 1 above.
2. In **Settings → Pages → Custom domain**, enter your domain (e.g. `yourname.com`).
3. Add a `CNAME` file at the root of the repo with your domain on one line:
   ```
   yourname.com
   ```
4. Update your DNS with a CNAME record pointing to `<username>.github.io`.

---

## File Structure

```
/
├── index.html                              # Home page
├── styles.css                              # All styles (single file)
├── resume/
│   └── index.html                         # Resume page
├── case-studies/
│   ├── index.html                         # Case studies listing
│   ├── cost-continuity/index.html         # Case study 1
│   ├── bid-coordination/index.html        # Case study 2
│   └── ai-workflow-friction/index.html    # Case study 3
├── contact/
│   └── index.html                         # Contact page
├── assets/
│   ├── favicon.ico                        # [PLACEHOLDER] Replace with real favicon
│   ├── resume.pdf                         # [PLACEHOLDER] Replace with real PDF
│   └── og-image.png                       # [PLACEHOLDER] Replace with social preview image
├── sitemap.xml                            # SEO sitemap
├── robots.txt                             # SEO robots
└── README.md                              # This file
```

---

## How to Update Content

### Replace placeholders

Search the HTML files for these strings and replace with real values:

| Placeholder               | Replace with                        |
|---------------------------|-------------------------------------|
| `Your Name`               | Your actual name                    |
| `you@example.com`         | Your email address                  |
| `https://linkedin.com/in/your-profile` | Your LinkedIn URL    |
| `https://example.com`     | Your actual domain (in sitemap.xml, robots.txt, og:url tags) |
| `Company Name A / B / C`  | Real company names or descriptions  |
| `University Name`         | Your school                         |
| `[Field of Study]`        | Your degree field                   |
| `Year of graduation`      | Your graduation year                |

### Replace asset placeholders

| File                   | What to do                                                    |
|------------------------|---------------------------------------------------------------|
| `assets/favicon.ico`   | Generate a favicon at [favicon.io](https://favicon.io) and drop it here |
| `assets/resume.pdf`    | Export your resume as PDF and rename it `resume.pdf`         |
| `assets/og-image.png`  | Create a 1200×630 px image for social sharing previews        |

### Edit page content

Each page is a self-contained HTML file. Open it in any text editor and edit the text directly. The structure is semantic and clearly labeled with comments.

### Add a new case study

1. Create a new folder under `case-studies/`, e.g. `case-studies/new-project/`.
2. Copy an existing `case-studies/*/index.html` file into the new folder.
3. Update the title, meta description, og: tags, and body content.
4. Add a card for it in `index.html` (the home page cards section) and `case-studies/index.html`.
5. Update `sitemap.xml` with the new URL.

### Update sitemap domain

Open `sitemap.xml` and `robots.txt` and replace `https://example.com` with your real domain before deploying.

---

## Design Assumptions

- **Color accent:** Muted slate blue (`#3B6E8C`). Change `--color-accent` and `--color-accent-dark` in `styles.css` to use a different accent.
- **Typography:** System font stack (`-apple-system, BlinkMacSystemFont, Segoe UI, ...`). No external font requests — fast and private.
- **Layout:** Max content width 840px, centered. Mobile-first responsive.
- **Accessibility:** Semantic HTML, ARIA labels on nav and sections, `aria-current="page"` on active nav links, visible focus indicators, color contrast meets WCAG AA.
- **No JavaScript** used anywhere on the site.
