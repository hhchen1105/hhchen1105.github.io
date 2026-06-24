# Hung's Notes

This repository hosts my personal blog, built with Jekyll and published through GitHub Pages.

The blog is intended as a public notebook for collecting and organizing thoughts on computer science education, artificial intelligence, technology, research culture, and related current issues. Some posts may be polished essays, while others may remain exploratory notes. The goal is not to present every article as a final conclusion, but to keep a durable and searchable record of ongoing thinking.

## Purpose

This blog serves several purposes:

1. To preserve thoughts in a more searchable and maintainable form than social media posts.
2. To provide a place for short essays, teaching reflections, research comments, and technology critiques.
3. To allow ideas to evolve from rough notes into more polished articles.
4. To keep ownership of the writing archive outside closed social platforms.

## Repository Structure

```text
.
├── _config.yml          # Jekyll site configuration
├── index.md            # Homepage
├── _posts/             # Blog posts
├── assets/             # CSS, images, and other static files
├── Gemfile             # Ruby dependencies
├── Gemfile.lock        # Locked dependency versions
└── README.md           # This file
```

Blog posts should be placed under `_posts/` with filenames in the following format:

```text
YYYY-MM-DD-title.md
```

For example:

```text
_posts/2026-06-24-little-censor-within.md
```

## Daily Writing Workflow

### 1. Create a new post

Create a new Markdown file under `_posts/`:

```bash
vim _posts/2026-06-24-new-post-title.md
```

Use this basic structure:

```markdown
---
layout: default
title: "New Post Title"
date: 2026-06-24
categories: [教育札記]
tags: [AI, 教育]
---

This is a draft note.
```

### 2. Preview the site locally

Run:

```bash
bundle exec jekyll serve
```

Then open:

```text
http://127.0.0.1:4000/
```

If the site does not update correctly, stop the server with `Ctrl-C` and restart it.

For a cleaner rebuild:

```bash
rm -rf _site .jekyll-cache
bundle exec jekyll serve
```

### 3. Review the post

Before publishing, check:

* Is the title clear？
* Is the post intended as a polished essay or an exploratory note？
* Are categories and tags appropriate？
* Are links working？
* Is the tone suitable for public reading？
* If AI tools were used for editing, does the final article still reflect my own judgment and responsibility？

### 4. Commit the changes and publish to GitHub

After reviewing the local preview:

```bash
git status
git add .
git commit -m "Add new blog post"
git push
```

GitHub Pages will rebuild and publish the site automatically (this may take a few minutes).


## Maintenance Notes

Files that should usually be tracked in git:

```text
_config.yml
Gemfile
Gemfile.lock
index.md
_posts/
assets/
README.md
```

Files that should usually not be tracked:

```text
_site/
.jekyll-cache/
.sass-cache/
.bundle/
vendor/
```
