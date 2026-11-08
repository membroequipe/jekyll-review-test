---
layout: default
title: "Guias de Compra e Tutoriais de Ferramentas"
description: "Dicas de uso, manutenção, segurança e guias completos para ajudar você a escolher e utilizar suas ferramentas."
permalink: /guias/
---

<div class="site-content">
  <div class="post-content">

  <style>
  h1 {
    line-height: 1.2 !important;
  }
</style>

    <h1>Guias e Tutoriais de Ferramentas</h1>
    <p>Aprenda a escolher, manusear com segurança e tirar o máximo proveito das suas ferramentas elétricas e a bateria. Os guias são organizados por aplicação e complementam os reviews individuais.</p>
    <nav class="category-jump-links" aria-label="Categorias de ferramentas">
      <a href="{{ '/furadeiras/' | relative_url }}">Furadeiras</a>
      <a href="{{ '/parafusadeiras/' | relative_url }}">Parafusadeiras</a>
      <a href="{{ '/comparativos/' | relative_url }}">Comparativos</a>
    </nav>
    <p>Para encontrar análises de produtos, comece pela categoria adequada: <a href="{{ '/furadeiras/' | relative_url }}">furadeiras e furadeiras/parafusadeiras</a> ou <a href="{{ '/parafusadeiras/' | relative_url }}">parafusadeiras dedicadas</a>. As duas categorias não são equivalentes: algumas ferramentas combinam perfuração e parafusamento, enquanto outras são projetadas principalmente para apertar fixadores.</p>

    <h2 id="artigos-guias" style="margin-top: 2rem;">Todos os Guias e Dicas Práticas</h2>
    
    {% assign guias_posts = site.posts | where_exp: "post", "post.category == 'guias' or post.categories contains 'guias'" %}
    
    <div class="reviews-grid" style="margin-top: 1.5rem;">
      {% if guias_posts.size > 0 %}
        {% for post in guias_posts %}
          <article class="review-card">
            <a href="{{ post.url | relative_url }}" class="review-img-wrapper">
              {% if post.image and post.image != "" %}
                <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" loading="lazy">
              {% else %}
                <img src="{{ '/assets/images/logo.png' | relative_url }}" alt="{{ post.title }}" loading="lazy">
              {% endif %}
            </a>

            <div class="home-post-body">
              <span class="home-post-badge">Guias</span>
              <h3 class="home-post-title">
                <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
              </h3>
              <div class="home-post-date">
                Por {{ post.author | default: "Equipe de Análises" }} • {{ post.date | date: "%d/%m/%Y" }}
              </div>
            </div>
          </article>
        {% endfor %}
      {% else %}
        <p style="grid-column: 1 / -1; color: #64748b; text-align: center; padding: 30px 0;">Em breve novos artigos publicados.</p>
      {% endif %}
    </div>

  </div>
</div>
