# Personal Blog

This is my personal blog built with [Jekyll](https://jekyllrb.com/), a static site generator. The blog features articles on various topics and is designed to be simple, fast, and easy to maintain.

## Project Setup

Make sure you have Ruby and Bundler installed, then:

```bash
# Install dependencies
$ bundle install
```

## Running the Blog Locally

```bash
# Start the Jekyll server
$ bundle exec jekyll serve

# Start with draft posts enabled
$ bundle exec jekyll serve --drafts
```

The blog will be available at `http://localhost:4000`

## Adding New Posts

Create new markdown files in the `_posts` directory using the following filename format:

```
YYYY-MM-DD-title-of-post.md
```

Make sure to include the proper front matter at the top of your post:

```yaml
---
layout: post
title: "Your Post Title"
date: YYYY-MM-DD HH:MM:SS +/-TTTT
categories: [category1, category2]
tags: [tag1, tag2]
---
```

## Project Structure

- `_posts/` - Blog post markdown files
- `_layouts/` - HTML layouts for posts and pages
- `_includes/` - Reusable HTML components
- `assets/` - Static assets (CSS, images, etc.)
- `_config.yml` - Site configuration

## License

This project is open source and available under the MIT license.
