---
exclude: true
---

# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

This is a Jekyll-based static site hosting short stories by Julio. The site uses GitHub Pages for automatic deployment at https://thinmanj.github.io/dog-years-stories/

## Architecture

**Static Site Generator**: Jekyll with Minima theme
**Content Model**: Stories are stored as markdown files in `_stories/` collection
**Deployment**: GitHub Pages (automatic on push to main branch)
**Repository**: thinmanj/dog-years-stories

### Directory Structure

- `_stories/` - Story content files (markdown with YAML front matter)
- `_config.yml` - Jekyll configuration, defines stories collection
- `index.md` - Homepage with Liquid template to list all stories

### Stories Collection

Stories are Jekyll collection items with custom permalink structure `/stories/:title/`. Each story file requires YAML front matter with:
- `title` - Story title
- `date` - Publication date (YYYY-MM-DD)
- `excerpt` - Brief description for listing page
- `layout` - Auto-assigned as "post" via defaults

## Development Workflow

### Adding New Stories

1. Create a new markdown file in `_stories/` with front matter:
```markdown
---
title: Story Title
date: YYYY-MM-DD
excerpt: Brief description for the index page
---

Story content here...
```

2. Story filename should be lowercase with underscores (e.g., `story_name.md`)
3. Commit and push - GitHub Pages automatically rebuilds and deploys

### Testing Locally

GitHub Pages uses Jekyll, so local testing requires Jekyll installation:
```bash
bundle exec jekyll serve
```

### Deployment

No build commands needed. Push to `main` branch triggers automatic GitHub Pages deployment.

## Content Guidelines

Stories follow a literary style inspired by Borges, exploring themes of time, memory, technology, and the human condition. Use markdown formatting for structure (headers, emphasis) but keep formatting minimal to preserve readability.
