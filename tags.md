---
layout: default
title: Tags
permalink: /tags/
---

# Tags

{% assign sorted_tags = site.tags | sort %}
{% for tag in sorted_tags %}
  {% assign tag_name = tag[0] %}
  {% assign tag_posts = tag[1] %}
  
## {{ tag_name }}

{% for post in tag_posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) - *{{ post.date | date: "%B %d, %Y" }}*
{% endfor %}

{% endfor %}
