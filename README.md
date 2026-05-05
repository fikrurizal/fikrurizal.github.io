# M. Fikru Rizal Academic Website

Source for [fikrurizal.github.io](https://fikrurizal.github.io), the personal academic website of M. Fikru Rizal.

## Architecture

This site is built with [Quarto](https://quarto.org/) and publishes static HTML to GitHub Pages. Quarto is used because the site is primarily academic content: Markdown/Quarto pages, a simple notes/blog section, clean navigation, and minimal dependencies. This replaces the previous Jekyll theme with a smaller Markdown-first structure that is easier to maintain without editing HTML or Ruby templates.

## Repository Structure

- `_quarto.yml` - site configuration, navigation, footer, output settings
- `index.qmd` - home page
- `cv.qmd` - CV page
- `research.qmd` - research overview
- `_content/` - reusable Markdown lists for publications, working papers, and projects
- `notes.qmd` - notes/blog listing page
- `notes/` - individual notes, each in its own folder
- `contact.qmd` - contact page
- `styles.css` - small custom stylesheet
- `.github/workflows/publish.yml` - GitHub Pages deployment workflow

## Required Software

Install Quarto from <https://quarto.org/docs/download/>.

No Node.js, Ruby, Bundler, or paid services are required for routine editing.

## Preview Locally

From the repository root:

```bash
quarto preview
```

This starts a local preview server and watches for changes.

To render the static site without starting a preview server:

```bash
quarto render
```

The rendered site is written to `docs/`, which is ignored locally because GitHub Actions rebuilds it for deployment.

## Edit Pages

Most content can be edited directly in these Markdown/Quarto files:

- Home: `index.qmd`
- CV: `cv.qmd`
- Research: `research.qmd`
- Contact: `contact.qmd`

Research lists are split into reusable Markdown files:

- Publications: `_content/publications.md`
- Working papers: `_content/working-papers.md`
- Projects: `_content/projects.md`

## Add a Note or Blog Post

Create a new folder inside `notes/`, then add an `index.qmd` file. For example:

```text
notes/my-new-note/index.qmd
```

Use this metadata at the top:

```yaml
---
title: "My New Note"
date: "2026-05-05"
categories: [health economics, policy]
draft: false
description: "One sentence summary for listings and search engines."
---
```

Write the post below the metadata using Markdown. Set `draft: true` while drafting if you do not want the post published.

## Add a Downloadable PDF CV

Create `assets/files/`, place the PDF there, and add a link near the top of `cv.qmd`, for example:

```markdown
[Download CV](assets/files/cv.pdf)
```

## Deploy to GitHub Pages

The included GitHub Actions workflow renders the site with Quarto and deploys it to GitHub Pages.

In the GitHub repository settings:

1. Go to **Settings > Pages**.
2. Set **Build and deployment** to **GitHub Actions**.
3. Push changes to the `master` branch.

The workflow will publish the rendered site to <https://fikrurizal.github.io>.
