---
layout: default
title: Welkom
---

<section class="hero shell">
  <h1>Korte verhalen, observaties en notities uit mijn dagboek</h1>
  <p>Ik schrijf elke week een nieuw stukje – over taal, migratie, cultuur en dagelijkse momenten. Pak er een koffie bij en blader door mijn notities.</p>
</section>

<section class="layout-panels">
  <aside class="card sidebar-nav">
    <h2>Verken</h2>
    <ul>
      <li><a href="{{ '/blog/' | relative_url }}">Blog<span>Korte notities, experimenten en verhalen</span></a></li>
      <li><a href="{{ '/about' | relative_url }}">Over<span>Wie ik ben en waarom ik schrijf</span></a></li>
      <li><a href="mailto:{{ site.email | default: 'said@example.com' }}">Contact<span>Stuur me een bericht of idee</span></a></li>
    </ul>
  </aside>

  <div class="card primary-card">
    <h2>Laatste notities</h2>
    <p>Een selectie van mijn recente stukken. Ik mik op heldere taal en warme toon – laat gerust weten wat je ervan vindt.</p>

    {% assign latest = site.posts | slice: 0, 4 %}
    {% if latest and latest != empty %}
      <div class="post-grid">
        {% for post in latest %}
          <a class="post-tile" href="{{ post.url | relative_url }}">
            <strong>{{ post.title }}</strong>
            <span>{{ post.date | date: "%d %b %Y" }}</span>
            {% if post.excerpt %}
              <span>{{ post.excerpt | strip_html | truncate: 100 }}</span>
            {% endif %}
          </a>
        {% endfor %}
      </div>
    {% else %}
      <div class="post-grid">
        <div class="post-tile">
          <strong>Je eerste post verschijnt hier</strong>
          <span>📆 Nog geen datum</span>
          <span>Schrijf een blogpost in `_posts/` om dit overzicht te vullen.</span>
        </div>
      </div>
    {% endif %}
  </div>
</section>

<section class="shell">
  <div class="card primary-card">
    <h2>Nieuwsbrief & updates</h2>
    <p>Wil je op de hoogte blijven? Ik ben een nieuwsbrief aan het voorbereiden met de mooiste fragmenten en nieuwe schetsen. Laat een seintje achter via <a href="mailto:{{ site.email | default: 'said@example.com' }}">mail</a> of stuur een DM op <a href="https://www.instagram.com/anatolischejongen" target="_blank" rel="noopener">Instagram</a>.</p>
  </div>
</section>
