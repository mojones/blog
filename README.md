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

You can generate a correctly dated post file with:

```bash
bin/new-post "My New Post"
```

That creates `_posts/YYYY-MM-DD-my-new-post.md` with starter front matter.

## Images

Put images under `assets/images/`.

Examples:

- `assets/images/my-photo.jpg`
- `assets/images/posts/all-life-related/diagram.png`

Reference images with `relative_url` so they work both locally and on GitHub Pages:

```html
<img src="{{ '/assets/images/my-photo.jpg' | relative_url }}" alt="Short description of image">
```

For captions, use `<figure>` and `<figcaption>`:

```html
<figure>
  <img src="{{ '/assets/images/posts/example/photo.jpg' | relative_url }}" alt="Short description of image">
  <figcaption>This is the caption.</figcaption>
</figure>
```

The stylesheet includes default figure and caption styling.

## Local preview

Local preview is optional. GitHub Actions can build and deploy the site without any local Ruby install.

If you want a local preview without installing Ruby on the host, use Docker:

```bash
bin/preview
```

That serves the site at `http://127.0.0.1:4000/` using `_config.local.yml`, so local links work from the site root instead of `/blog/`.

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

## Deployment notes

- `_config.yml` sets `baseurl: "/blog"` for project-page deployment.
- If you later decide the blog should live at the root domain instead, move this Jekyll site into `mojones.github.io` and change `baseurl` to `""`.
