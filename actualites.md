---
layout: default
title: Actualités
---

<section class="slide-up">
<h2>Actualités et articles</h2>
<p>Découvrez les dernières nouvelles et conseils TI de Solud, ancrés dans la région de La Tuque.</p>

<ul class="blog-list">
  {% for post in site.posts %}
  <li class="card fade-in">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p class="meta">{{ post.date | date: "%d %B %Y" }}</p>
    <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
    <a href="{{ post.url | relative_url }}" class="btn">Lire</a>
  </li>
  {% endfor %}
</ul>
</section>
