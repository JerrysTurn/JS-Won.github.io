# JS-Won.github.io

Personal blog of Jaeseog Won, built with [Jekyll](https://jekyllrb.com/) and the [Chirpy theme](https://github.com/cotes2020/jekyll-theme-chirpy), deployed to GitHub Pages at <https://js-won.github.io>.

## Local development

Requires Ruby 3.x and Bundler.

```bash
bundle install
bundle exec jekyll serve   # http://127.0.0.1:4000
```

## Writing posts

Add Markdown files to `_posts/` named `YYYY-MM-DD-title.md`. Pushing to `main` triggers the GitHub Actions workflow that builds and deploys the site.
