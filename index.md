---
layout: default
title: Welkom
---

# Hoi 👋

Hier deel ik korte stukjes in het **Nederlands (NL)**: dagelijkse notities, observaties en mini-verhalen.

- Alle berichten: **[Blog](/blog/)**  
- Over mij: **[Over](/about)**

## Laatste berichten

{% assign latest = site.posts | slice: 0, 6 %}
{% for post in latest %}
- {{ post.date | date: "%d %b %Y" }} — [{{ post.title }}]({{ post.url }}){% if post.lang %} ({{ post.lang | upcase }}){% endif %}
{% endfor %}
