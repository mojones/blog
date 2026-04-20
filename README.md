# Preliminary Work Blog

Minimal Markdown-first blog for GitHub Pages.

## Why Jekyll

Jekyll is the best fit here because GitHub Pages supports it directly, GitHub recommends it for Pages, and the authoring model is just Markdown files plus a small amount of front matter.

Official references:

- https://docs.github.com/github/working-with-github-pages/about-github-pages-and-jekyll
- https://docs.github.com/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll

## Writing

Add posts to `_posts/` using filenames like `YYYY-MM-DD-title.md`.

Example:

```md
---
title: New Note
---
This is a post written in Markdown.
```

## Local preview

Local preview is optional. GitHub Actions can build and deploy the site without any local Ruby install.

If you want local preview, install Ruby and Bundler, then run:

```bash
bundle install
bundle exec jekyll serve
```

## GitHub Pages setup

1. Create a repository for this blog, for example `mojones/blog`.
2. Push this directory to the repo on the `main` branch.
3. In the repo settings, set Pages to use `GitHub Actions` as the source.
4. The site will publish at `https://preliminarywork.com/blog/` because the root custom domain is already attached to `mojones.github.io`.

## Notes

- `_config.yml` sets `baseurl: "/blog"` for project-page deployment.
- If you later decide the blog should live at the root domain instead, move this Jekyll site into `mojones.github.io` and change `baseurl` to `""`.
