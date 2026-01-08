---
layout: home
title: Dog Years
---

# Dog Years

*Short stories exploring time, memory, technology, and the human condition.*

---

## Stories

{% for story in site.stories %}
### [{{ story.title }}]({{ story.url }})
*{{ story.date | date: "%B %d, %Y" }}*

{{ story.excerpt }}

[Read more →]({{ story.url }})

---
{% endfor %}

---

*By Julio | [thinmanj@gmail.com](mailto:thinmanj@gmail.com)*
