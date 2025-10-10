---
layout: default
title: Blog
---

## Alle berichten
{% for post in site.posts %}
- {{ post.date | date: "%d %b %Y" }} — [{{ post.title }}]({{ post.url | relative_url }}){% if post.lang %} ({{ post.lang | upcase }}){% endif %}
{% endfor %}
