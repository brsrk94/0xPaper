# 0xPaper

Minimal Hugo website for personal blogs and research notes.

## Live Sections
- About Me
- Writings
- Researches

## Tech Stack
- Hugo (extended)
- Custom theme: `themes/catppuccin-minimal`

## Local Development
1. Install Hugo (extended).
2. Start local server:

```bash
hugo server -D
```

3. Open `http://localhost:1313/`.

## Create Content
New writing:

```bash
hugo new writings/my-post.md
```

New research:

```bash
hugo new researches/my-research.md
```

## Research Paper Download Links
For downloadable papers and resume:
- Put files in `static/researches/`
- Reference them in markdown front matter, for example:

```toml
paper_download = "/researches/research-one.pdf"
paper_url = "https://example.com"
```

## Build

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
This repo includes a GitHub Actions workflow at `.github/workflows/hugo.yml`.

After pushing to GitHub:
1. Go to **GitHub repo → Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.
3. Push to `main` branch; workflow builds and deploys automatically.

## Git Setup
If not initialized yet:

```bash
git init
git branch -M main
git remote add origin https://github.com/brsrk94/0xPaper.git
git add .
git commit -m "Initial 0xPaper Hugo site"
git push -u origin main
```
