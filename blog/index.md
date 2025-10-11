---
layout: default
title: Blog
---

<section class="shell">
  <div class="card primary-card">
    <h1>Blog</h1>
    <p>Hier verschijnen al mijn notities en verhalen. Selecteer een stuk hieronder om te lezen.</p>

    {% if site.posts and site.posts != empty %}
      <ul>
        {% for post in site.posts %}
          <li>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            <span>— {{ post.date | date: "%d %b %Y" }}</span>
          </li>
        {% endfor %}
      </ul>
    {% else %}
      <p>Nog geen posts gepubliceerd.</p>
    {% endif %}
  </div>
</section>
