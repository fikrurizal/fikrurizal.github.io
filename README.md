# fikrurizal.github.io

Source for [fikrurizal.github.io](https://fikrurizal.github.io), the personal academic website of M. Fikru Rizal.

The site is built with Jekyll and hosted by GitHub Pages from the `master` branch.

## Editing Content

Most site content lives in these files and folders:

* `_pages/about.md` - homepage content
* `_pages/research.md` - research overview
* `_pages/cv.md` - CV page
* `_posts/` - blog posts
* `_publications/` - publication entries
* `_talks/` - talk and presentation entries
* `_teaching/` - teaching entries
* `_config.yml` - site metadata, profile links, and Jekyll configuration

Uploaded PDFs and other downloadable assets can go in `files/`. Images used by the site can go in `images/`.

## Running Locally

Install Ruby and Bundler, then run:

```bash
bundle install
bundle exec jekyll serve -l -H localhost
```

The local site will be available at `http://localhost:4000`.

## Deployment

GitHub Pages is configured to build and publish the site from the repository's `master` branch. Commit changes and push them to GitHub:

```bash
git push origin master
```

After the push, GitHub Pages rebuilds the public site at [https://fikrurizal.github.io](https://fikrurizal.github.io).
