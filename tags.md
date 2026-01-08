---
layout: default
title: Tags
permalink: /tags/
---

# Tags

{% assign all_tags = "" | split: "" %}
{% for story in site.stories %}
  {% if story.tags %}
    {% for tag in story.tags %}
      {% unless all_tags contains tag %}
        {% assign all_tags = all_tags | push: tag %}
      {% endunless %}
    {% endfor %}
  {% endif %}
{% endfor %}

{% assign sorted_tags = all_tags | sort %}
{% for tag in sorted_tags %}
## {{ tag }}

{% for story in site.stories %}
  {% if story.tags contains tag %}
- [{{ story.title }}]({{ story.url | relative_url }}) - *{{ story.date | date: "%B %d, %Y" }}*
  {% endif %}
{% endfor %}

{% endfor %}
