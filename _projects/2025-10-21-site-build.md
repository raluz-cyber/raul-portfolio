---
layout: project
title: "Portfolio Site Build (Jekyll + GitHub Pages)"
date: 2025-10-21
tags: [coding]
summary: "Data-driven portfolio with Jekyll collections, accessible HTML/CSS, and zero-JS core. Built and previewed in Codespaces, deployed on GitHub Pages."
role: "Architecture, templates, CSS, CI/deploy"
tech: ["Jekyll", "Liquid", "HTML", "CSS", "GitHub Pages", "Codespaces"]
hero_image: "/assets/img/projects/site-build/hero.png"
gallery:
  - "/assets/img/projects/site-build/hero.png"
  - "/assets/img/projects/site-build/layouts.jpg"
  - "/assets/img/projects/site-build/cards.jpg"
links:
  repo: "https://github.com/<your-username>/raul-portfolio"
  demo: "https://<your-username>.github.io/raul-portfolio/"
  doc: "/assets/docs/site-architecture.pdf"
featured: true
---
### Goal
Ship a clean, multi-page portfolio that I can update just by adding Markdown files—no touching code for new projects.

### Approach
- **Jekyll + GitHub Pages** so the build matches production (uses `github-pages` gem).
- **Collections**: `_projects/` folder powers the Projects list and detail pages.
- **Pure HTML/CSS**: zero-JS core. Modern, responsive layout with CSS grid/flex.
- **Accessibility**: semantic headings, skip link, focus states, alt text, ≥4.5:1 contrast.
- **SEO**: `jekyll-seo-tag`, Open Graph/Twitter, `robots.txt`, auto `sitemap.xml`.

### Structure (high level)

### Key features
- **Home**: hero + featured projects auto-pulled via `featured: true`.
- **Projects**: grid of cards (title, summary, tags, image) using an include.
- **Project detail**: hero image, meta (date/role/tech), body, gallery, links.
- **About**: inline resume link above a visible Download button (PDF path configurable).
- **Gallery**: responsive, lazy-loaded images—CSS only.
- **Contact**: mailto + socials.

### Accessibility & SEO
- Skip link to `<main>`, visible focus rings, semantic sections, alt text fallbacks.
- `jekyll-seo-tag` for meta/OG/Twitter; `jekyll-sitemap` for sitemap; `robots.txt`.

### Tooling & Dev
- **Codespaces**: `bundle exec jekyll serve --host 0.0.0.0 --port 4000`.
- **Base URL**: empty for dev; `/raul-portfolio` for GitHub Pages project deploy.
- **One terminal** runs the server; second terminal for `git add/commit/push`.

### Deployment
1. Set `_config.yml` for prod:
   ```yaml
   url: "https://<your-username>.github.io"
   baseurl: "/raul-portfolio"
