# CLAUDE.md — Portfolio Site Context

## Project Summary
Static HTML/CSS personal portfolio for Suchithra Balakrishnan (Data Scientist & Analytics Engineer).
Hosted on GitHub Pages at `https://suchithrabalakrishnan.github.io`.

**No frameworks. No npm. No build step.** Pure HTML + CSS + minimal inline JS only.

---

## File Structure
```
├── index.html        # Home page (hero + contact section)
├── about.html        # Bio, skills, work experience, resume link
├── portfolio.html    # Project card grid
├── blog.html         # Blog post list
├── css/
│   └── style.css     # Single shared stylesheet — ALL styles live here
├── assets/
│   └── images/       # Headshot, project images (add files here)
└── CLAUDE.md         # This file
```

---

## Design Tokens (css/style.css `:root`)
| Variable             | Value     | Purpose              |
|----------------------|-----------|----------------------|
| `--color-bg`         | `#ffffff` | Page background      |
| `--color-bg-alt`     | `#f8fafc` | Alternate sections   |
| `--color-text`       | `#1e293b` | Body text            |
| `--color-text-muted` | `#64748b` | Secondary text       |
| `--color-accent`     | `#3b82f6` | Links, buttons, tags |
| `--font-family`      | Inter     | Google Fonts         |

---

## How to Add a Project Card (portfolio.html)
Copy this block and paste it inside `<div class="cards-grid">`:

```html
<div class="card">
  <h3>Project Title</h3>
  <p class="card-description">
    2–3 sentence description of the project and what it demonstrates.
  </p>
  <div class="card-tags">
    <span class="tag">Python</span>
    <span class="tag">SQL</span>
  </div>
  <div class="card-links">
    <a href="https://github.com/..." target="_blank" rel="noopener noreferrer">View on GitHub</a>
    <a href="https://..." target="_blank" rel="noopener noreferrer">Read Write-up</a>
  </div>
</div>
```

---

## How to Add a Blog Post (blog.html)
Copy this block and paste it inside `<div class="post-list">`:

```html
<div class="post-item">
  <p class="post-date">Month Year</p>
  <a class="post-title" href="https://medium.com/..." target="_blank" rel="noopener noreferrer">
    Post Title
  </a>
  <p class="post-excerpt">
    2–3 sentence summary of the article.
  </p>
  <a class="post-read-more" href="https://medium.com/..." target="_blank" rel="noopener noreferrer">Read more &rarr;</a>
</div>
```

---

## Placeholders to Update Before Publishing
- `your@email.com` in `index.html` — replace with real email
- GitHub/LinkedIn URLs — confirm handles are correct
- Experience entries in `about.html` — fill in real company names, roles, dates, bullets
- `/assets/resume.pdf` — add the actual PDF file to `assets/`
- Location placeholder in `about.html` — fill in `[City, Country]`
- Headshot: uncomment the `<div class="hero-image">` block in `index.html` and add `assets/images/headshot.jpg`
- Copyright year — update annually

---

## Deployment
1. Push all files to `main` branch of `suchithrabalakrishnan/suchithrabalakrishnan.github.io`
2. Go to repo Settings → Pages → Source: `main` branch, `/ (root)`
3. Site goes live at `https://suchithrabalakrishnan.github.io`

Custom domain (future): Add 4 GitHub DNS A records in Porkbun, then set custom domain in repo Settings → Pages.
