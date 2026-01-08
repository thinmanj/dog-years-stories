---
layout: default
title: Dog Years
---

# Dog Years

*Short stories exploring time, memory, technology, and the human condition.*

---

## Stories

{% for story in site.stories %}
### [{{ story.title }}]({{ story.url | relative_url }})
*{{ story.date | date: "%B %d, %Y" }}*

{{ story.excerpt }}

[Read more →]({{ story.url | relative_url }})

---
{% endfor %}

---

*By Julio | [thinmanj@gmail.com](mailto:thinmanj@gmail.com)*
