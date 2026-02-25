# 0xPaper

Minimal Hugo website for personal blogs and research notes.

## Live Sections
- About Me
- Writings
- Researches

> **Highlight**: Use the `dracula` syntax theme for all embedded code snippets so the README matches the site’s dark palette.

## Tech Stack
- Hugo (extended)
- Custom theme: `themes/catppuccin-minimal`

## Local Development
> **Recommended**: Install Hugo Extended and keep the dev server running with the dracula-inspired output.
1. Install Hugo (extended).
2. Start local server:

```bash
hugo server -D
```

3. Open `http://localhost:1313/`.

## Create Content
> **Tip**: New posts inherit the dracula-highlighted theme automatically.
New writing:

```bash
hugo new writings/my-post.md
```

New research:

```bash
hugo new researches/my-research.md
```

## Research Paper Download Links
> **Reminder**: Keep paper assets under `static/researches/` so Hugo serves them with the dracula-style UI.
For downloadable papers and resume:
- Put files in `static/researches/`
- Reference them in markdown front matter, for example:

```toml
paper_download = "/researches/research-one.pdf"
paper_url = "https://example.com"
```

## Build
> **Build Note**: Use Hugo’s minify flag before deploying so the dracula-tinted assets stay compact.

```bash
hugo --minify
```

Output is generated in `public/`.

## Folder Structure
```text
.
├── archetypes/
├── content/
│   ├── about/
│   ├── writings/
│   └── researches/
├── static/
│   ├── images/
│   └── researches/
├── themes/
│   └── catppuccin-minimal/
├── .github/
│   └── workflows/
│       └── hugo.yml
├── hugo.toml
└── README.md
```

## Deploy to GitHub Pages
> **Deploy**: Let the workflow in `.github/workflows/hugo.yml` push dracula-branded content to `gh-pages`.
This repo includes a GitHub Actions workflow at `.github/workflows/hugo.yml`.

After pushing to GitHub:
1. Go to **GitHub repo → Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.
3. Push to `main` branch; workflow builds and deploys automatically.

## Git Setup
> **Git tip**: Keep your commits descriptive so the dracula history stays readable.
If not initialized yet:

```bash
git init
git branch -M main
git remote add origin https://github.com/brsrk94/0xPaper.git
git add .
git commit -m "Initial 0xPaper Hugo site"
git push -u origin main
```
