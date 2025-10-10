---
layout: default
title: Welkom
hero: true
hero_image: /assets/img/hero.svg
hero_title: Welkom
hero_subtitle: Mijn persoonlijke NL-blog
---

# Hoi 👋

Hier deel ik korte stukjes in het **Nederlands (NL)**: dagelijkse notities, observaties en mini-verhalen.

- Alle berichten: **[Blog]({{ '/blog/' | relative_url }})**  
- Over mij: **[Over]({{ '/about' | relative_url }})**

## Laatste berichten

{% assign latest = site.posts | slice: 0, 6 %}
{% for post in latest %}
- {{ post.date | date: "%d %b %Y" }} — [{{ post.title }}]({{ post.url | relative_url }}){% if post.lang %} ({{ post.lang | upcase }}){% endif %}
{% endfor %}
