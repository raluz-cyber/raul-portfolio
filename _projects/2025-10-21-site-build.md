---
layout: project
title: "Portfolio Site Build (Jekyll + GitHub Pages)"
date: 2025-10-21
tags: [coding]
summary: "Data-driven portfolio using a Jekyll collection, accessible HTML/CSS, and zero-JS core. Built in Codespaces; deploys on GitHub Pages."
role: "Architecture, templates, CSS, CI/deploy"
tech: ["Jekyll", "Liquid", "HTML", "CSS", "GitHub Pages", "Codespaces"]
hero_image: "/assets/img/projects/site-build/MainPageCreation-img.png"
gallery:
  - "/assets/img/projects/site-build/MainPageCreation-img.png"
links:
  repo: "https://github.com/raluz-cyber/raul-portfolio"
  demo: "https://raluz-cyber.github.io/raul-portfolio/"
  doc: "/assets/docs/site-architecture.pdf"
featured: true
---

### Goal
Ship a clean, multi-page portfolio I can update by adding Markdown files—no touching code for new projects.

### Approach
- **Jekyll + GitHub Pages** with the `github-pages` gem so dev = prod.
- **Collections**: `_projects/` drives the Projects list and detail pages.
- **Pure HTML/CSS**: modern, responsive layout with grid/flex; no JS required.
- **Accessibility**: semantic headings, skip link, visible focus, alt text, contrast ≥ 4.5:1.
- **SEO**: `jekyll-seo-tag`, auto `sitemap.xml` via `jekyll-sitemap`, and `robots.txt`.

### Structure (high level)
### Key features
- **Home**: hero + featured projects auto-pulled via `featured: true`.
- **Projects**: card grid (title, summary, tags, image) via an include.
- **Project detail**: hero image, meta (date/role/tech), body, gallery, links.
- **About**: inline resume link above a visible Download button (PDF path configurable).
- **Gallery**: responsive, lazy-loaded images—CSS only.
- **Contact**: `mailto:` + socials.

### Tooling & Dev
- **Codespaces** local preview:  
  `bundle exec jekyll serve --host 0.0.0.0 --port 4000`
- **Base URL**: empty for dev; `/raul-portfolio` for GitHub Pages deploy.
- Keep one terminal for the server; a second for `git add/commit/push`.

### Deployment (project site)
1. Set in `_config.yml` for prod:
   ```yaml
   url: "https://raluz-cyber.github.io"
   baseurl: "/raul-portfolio"
