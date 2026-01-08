---
exclude: true
---

# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

This is a Jekyll-based static site hosting short stories by Julio. The site uses GitHub Pages for automatic deployment at https://thinmanj.github.io/dog-years-stories/

## Architecture

**Static Site Generator**: Jekyll with tale theme (remote_theme: chesterhow/tale)
**Content Model**: Stories are stored as markdown files in `_stories/` collection
**Deployment**: GitHub Pages (automatic on push to main branch)
**Repository**: thinmanj/dog-years-stories

### Directory Structure

- `_stories/` - Story content files (markdown with YAML front matter)
- `_config.yml` - Jekyll configuration, defines stories collection and baseurl
- `index.md` - Homepage with Liquid template to list all stories
- `about.md` - About page with site description
- `tags.md` - Tags page listing stories by tag
- `assets/images/` - Hero images for stories

### Stories Collection

Stories are Jekyll collection items with custom permalink structure `/stories/:title/`. Each story file requires YAML front matter with:
- `title` - Story title
- `date` - Publication date (YYYY-MM-DD)
- `excerpt` - Brief description for listing page
- `image` - Path to hero image (optional, e.g., `/assets/images/story_name.jpg`)
- `tags` - Array of tags (optional, e.g., `[AI, technology, dystopia]`)
- `layout` - Auto-assigned as "post" via defaults

## Development Workflow

### Adding New Stories

1. Create a new markdown file in `_stories/` with front matter:
```markdown
---
title: Story Title
date: YYYY-MM-DD
excerpt: Brief description for the index page
image: /assets/images/story_name.jpg
tags: [AI, technology, dystopia]
---

![Story Title]({{ page.image | relative_url }})

# Story Title

Story content here...
```

2. Generate a hero image:
   - Use AI tools (Bing Image Creator, Leonardo.ai, Midjourney)
   - Save as `assets/images/story_name.jpg` (matching story filename)
   - Aim for atmospheric, cinematic style (1200px wide recommended)

3. Story filename should be lowercase with underscores (e.g., `story_name.md`)
4. Commit and push - GitHub Pages automatically rebuilds and deploys

### Testing Locally

GitHub Pages uses Jekyll, so local testing requires Jekyll installation:
```bash
bundle exec jekyll serve
```

### Deployment

No build commands needed. Push to `main` branch triggers automatic GitHub Pages deployment.

## Content Guidelines

Stories follow a literary style inspired by Borges, exploring themes of time, memory, technology, and the human condition. Use markdown formatting for structure (headers, emphasis) but keep formatting minimal to preserve readability.
