# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build Commands

```bash
# Serve locally with live reload
bundle exec jekyll serve

# Install dependencies (if needed)
bundle install
```

## Architecture

This is a Jekyll static site for a personal blog/portfolio, deployed to GitHub Pages at neivin.com.

### Content Structure
- `_posts/` - Blog posts in Markdown (YYYY-MM-DD-title.md format)
- `_projects/` - Project showcase items (Jekyll collection)
- `pages/` - Static pages (about, archive, books, projects)

### Templates
- `_layouts/` - Page templates (default.html → post.html/page.html)
- `_includes/` - Reusable partials (head, header, footer)
- `_sass/` - SCSS partials imported by `css/main.scss`

### Key Files
- `_config.yml` - Jekyll configuration, site metadata, plugin settings
- `index.html` - Homepage with paginated blog posts
- `Gemfile` - Ruby dependencies (github-pages gem manages Jekyll version)
