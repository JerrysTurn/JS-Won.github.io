# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

Personal blog for GitHub Pages (https://js-won-robotics.github.io), built with Jekyll and the [Chirpy theme](https://github.com/cotes2020/jekyll-theme-chirpy) via the chirpy-starter template. The theme itself lives in the `jekyll-theme-chirpy` gem — this repo only contains content and configuration, plus the `assets/lib` git submodule (chirpy-static-assets).

## Commands

```bash
bundle install              # install dependencies (requires Ruby 3.x)
bundle exec jekyll serve    # local preview at http://127.0.0.1:4000 with live reload
JEKYLL_ENV=production bundle exec jekyll build   # production build to _site/
tools/test.sh               # build + html-proofer validation (what CI runs)
```

After cloning, run `git submodule update --init` to fetch `assets/lib`.

## Deployment

Pushing to `main` triggers `.github/workflows/pages-deploy.yml`, which builds the site and deploys to GitHub Pages. The repo's Pages setting must be set to "GitHub Actions" as the source. Changes to `README.md`, `LICENSE`, and `.gitignore` do not trigger a deploy.

## Content structure

- `_posts/` — blog posts, named `YYYY-MM-DD-title.md`. Front matter requires `title` and `date` (with `+0900` offset since timezone is Asia/Seoul); `categories` (max 2 levels) and `tags` are optional. Post URLs are `/posts/:title/`.
- `_tabs/` — sidebar pages (About, etc.), ordered by the `order` front-matter key.
- `_config.yml` — site config (title, social links, analytics, comments). The bottom section marked "not recommended to be modified" should be left alone.
- `_data/` — overrides for theme data files (e.g. `contact.yml`, `share.yml`).
- Site avatar goes in `assets/` and is referenced via the `avatar` key in `_config.yml`.
