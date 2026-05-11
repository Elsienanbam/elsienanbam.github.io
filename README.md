# Elsie David — Portfolio Site

Static site, no build step. Open `index.html` in a browser to preview locally.

## Structure

```
Portfolio/
├── index.html              # Landing page
├── assets/
│   └── styles.css          # Shared styles (case studies + landing)
├── case-studies/
│   ├── unbarred.html       # RAG / applied ML
│   ├── habitat.html        # Causal inference
│   └── lead-scoring.html   # Analytics / experimentation
└── README.md               # This file
```

## Local preview

```bash
# From the Portfolio folder
python3 -m http.server 8000
# Then open http://localhost:8000
```

Or just double-click `index.html`.

## Deployment (GitHub Pages — recommended)

1. Create a new public repo on GitHub (e.g. `elsiedavid.github.io` for a root URL, or any name for a project URL).
2. From this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin git@github.com:<your-username>/<repo>.git
   git push -u origin main
   ```
3. In repo Settings → Pages → Source: `main` branch, root folder. Save.
4. Site is live at `https://<your-username>.github.io/<repo>/` in ~1 minute.

Optional: point a custom domain (e.g. `elsiedavid.com`) at the GitHub Pages site by adding a `CNAME` file and configuring DNS.

## What's still TODO

Each case study has yellow `TODO` callouts marking the spots that need real content from the project repos. Search the HTML files for `class="todo"` to find them.
