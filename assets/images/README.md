# Story Images

Place hero images for stories in this directory.

## Naming Convention
Use the story filename (without .md): `story_name.jpg`

Example: `the_ruins_of_exactitude.jpg`

## Adding Images to Stories

In story front matter:
```markdown
---
title: The Ruins of Exactitude
date: 2026-01-08
excerpt: Brief description
image: /assets/images/the_ruins_of_exactitude.jpg
---
```

Then in the story content, add at the top:
```markdown
![Story title]({{ page.image | relative_url }})
```

## Image Guidelines
- Format: JPG or PNG
- Size: 1200px wide recommended
- Style: Atmospheric, cinematic, literary
- For AI generation: Use Midjourney, DALL-E, or similar
