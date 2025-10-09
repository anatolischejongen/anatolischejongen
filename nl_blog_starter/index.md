---
layout: default
title: Welkom
---

# Hoi 👋

Burada **Hollands (NL)** kısa yazılar paylaşıyorum: günlük notlar, gözlemler, mini hikâyeler.

- Tüm yazılar: **[Blog](/blog/)**  
- Hakkımda: **[About](/about)**

## Son yazılar

{% assign latest = site.posts | slice: 0, 6 %}
{% for post in latest %}
- {{ post.date | date: "%d %b %Y" }} — [{{ post.title }}]({{ post.url }}){% if post.lang %} ({{ post.lang | upcase }}){% endif %}
{% endfor %}
