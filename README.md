# bienkma.github.io

Personal homepage and notes, built with [Hugo](https://gohugo.io/) and the [hugo-researcher](https://github.com/ojroques/hugo-researcher) theme.

## Local development

Requires [Hugo Extended](https://gohugo.io/installation/).

```bash
git submodule update --init --recursive
hugo server -D
```

Open http://localhost:1313

## Add a post

Create a file under `content/posts/YYYY/slug.md`:

```markdown
+++
title = "Post title"
date = 2026-05-19
+++

Your content here.
```

## Deploy

Pushes to `master` deploy via GitHub Actions. In repository **Settings → Pages**, set **Source** to **GitHub Actions**.

## Layout

| Path | Purpose |
|------|---------|
| `content/_index.md` | Home — about |
| `content/notes/_index.md` | Curated links (`/notes/`) |
| `content/posts/` | Blog posts (`/posts/YYYY/slug/`) |
| `static/books/` | PDFs and downloads |
| `themes/researcher/` | Theme (git submodule) |
