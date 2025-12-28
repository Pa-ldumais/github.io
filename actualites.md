---
layout: default
title: Actualités
description: Découvrez les dernières nouvelles et conseils TI de Solud, ancrés dans la région de La Tuque.
---

<section class="actualites-section">
  <div class="container">
    <div class="section-header">
      <h1>Actualités et articles</h1>
      <p class="section-description">Découvrez les dernières nouvelles et conseils TI de Solud, ancrés dans la région de La Tuque.</p>
    </div>

    {% if site.posts.size > 0 %}
    <div class="blog-grid">
      {% for post in site.posts %}
      <article class="blog-card">
        <div class="blog-card-content">
          <h2 class="blog-title">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h2>
          <p class="blog-meta">
            <time datetime="{{ post.date | date_to_xmlschema }}">
              {{ post.date | date: "%d %B %Y" }}
            </time>
          </p>
          <p class="blog-excerpt">{{ post.excerpt | strip_html | truncate: 150 }}</p>
          <a href="{{ post.url | relative_url }}" class="blog-link">
            Lire l'article →
          </a>
        </div>
      </article>
      {% endfor %}
    </div>
    {% else %}
    <div class="no-posts">
      <p>Aucun article disponible pour le moment. Revenez bientôt pour découvrir nos dernières actualités!</p>
    </div>
    {% endif %}
  </div>
</section>

<style>
.actualites-section {
  padding: 4rem 0;
  min-height: 60vh;
}

.section-header {
  text-align: center;
  margin-bottom: 3rem;
}

.section-header h1 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  color: #1a1a1a;
}

.section-description {
  font-size: 1.1rem;
  color: #666;
  max-width: 600px;
  margin: 0 auto;
}

.blog-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.blog-card {
  background: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  overflow: hidden;
}

.blog-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.15);
}

.blog-card-content {
  padding: 1.5rem;
}

.blog-title {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
}

.blog-title a {
  color: #1a1a1a;
  text-decoration: none;
  transition: color 0.3s ease;
}

.blog-title a:hover {
  color: #0066cc;
}

.blog-meta {
  font-size: 0.9rem;
  color: #888;
  margin-bottom: 1rem;
}

.blog-excerpt {
  color: #555;
  line-height: 1.6;
  margin-bottom: 1rem;
}

.blog-link {
  display: inline-block;
  color: #0066cc;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
}

.blog-link:hover {
  color: #004999;
}

.no-posts {
  text-align: center;
  padding: 3rem;
  background: #f5f5f5;
  border-radius: 8px;
  color: #666;
}

@media (max-width: 768px) {
  .section-header h1 {
    font-size: 2rem;
  }
  
  .blog-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
}
</style>
