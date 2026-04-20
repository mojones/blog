# Project Summary

Set up a minimal Markdown-first blog for GitHub Pages in this repository.

## Generator choice

Chose Jekyll because it is the simplest fit for GitHub Pages and supports a straightforward writing workflow based on Markdown files with front matter.

## Site structure

- `_posts/` contains blog posts in `YYYY-MM-DD-title.md` format
- `_layouts/` contains minimal page and post templates
- `assets/css/style.css` contains a lightweight custom minimalist theme
- `index.md` lists published posts
- `about.md` provides a basic static page
- `_config.yml` configures the site for deployment at `/blog/` on `https://preliminarywork.com`

## Deployment

- Initialized this directory as a git repository
- Created GitHub repo `mojones/blog`
- Pushed the site to the `main` branch
- Added a GitHub Actions workflow at `.github/workflows/pages.yml`
- Configured GitHub Pages to publish with the workflow
- Confirmed the site is live at `https://preliminarywork.com/blog/`

## Authoring workflow

To publish a new post:

1. Add a Markdown file to `_posts/`
2. Include front matter with at least a `title`
3. Commit and push to `main`

GitHub Actions builds and deploys the site automatically, so no local install is required for publishing.

## Local development

Local preview is optional. Ruby, Bundler, and Jekyll are not currently installed on this machine, so local serving was not run. If local preview is needed later, install Ruby and Bundler, then run `bundle install` and `bundle exec jekyll serve`.
