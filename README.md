# Dog Years

Short stories by Julio exploring time, memory, technology, and the human condition.

**Live site:** https://thinmanj.github.io/dog-years-stories/

## Published Stories

- [The Ruins of Exactitude](https://thinmanj.github.io/dog-years-stories/stories/the_ruins_of_exactitude/) - A traveler visits abandoned AI infrastructure

## Adding Stories

1. Create a new file in `_stories/` with front matter:
   ```markdown
   ---
   title: Story Title
   date: 2026-01-08
   excerpt: Brief description
   image: /assets/images/story_name.jpg
   tags: [AI, technology, dystopia]
   ---
   
   ![Story Title]({{ page.image | relative_url }})
   
   # Story Title
   
   Story content here...
   ```

2. Generate a hero image:
   - Use AI tools (Bing Image Creator, Leonardo.ai, Midjourney)
   - Save as `assets/images/story_name.jpg` (matching filename)
   - Aim for atmospheric, cinematic style

3. Commit and push - it will appear automatically on the site

## Theme

Site uses the [tale](https://github.com/chesterhow/tale) Jekyll theme for clean, literary typography.

## Contact

thinmanj@gmail.com
