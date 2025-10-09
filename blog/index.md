---
layout: default
title: Blog
---

## Blog yazıları

{% for post in site.posts %}
- {{ post.date | date: "%d %b %Y" }} — [{{ post.title }}]({{ post.url }}){% if post.lang %} ({{ post.lang | upcase }}){% endif %}
{% endfor %}
