---
layout: default
title: "Guias de Compra e Tutoriais de Ferramentas"
description: "Dicas de uso, manutenção, segurança e guias completos para ajudar você a escolher e utilizar suas ferramentas."
permalink: /guias/
---

<div class="site-content">
  <div class="post-content">

    <h1>Guias e Tutoriais de Ferramentas</h1>

    <p>
      Aprenda a escolher, manusear com segurança e tirar o máximo
      proveito das suas ferramentas elétricas e a bateria.
    </p>

    <h2 id="artigos-guias" class="guides-section-title">
      Todos os Guias e Dicas Práticas
    </h2>

    {% assign guias_posts = site.posts | where_exp: "post", "post.category == 'guias' or post.categories contains 'guias'" %}

    <div class="reviews-grid guides-posts-grid">

      {% if guias_posts.size > 0 %}

        {% for post in guias_posts %}

          <article class="review-card">

            <a href="{{ post.url | relative_url }}" class="review-img-wrapper">

              {% if post.image and post.image != "" %}
                <img
                  src="{{ post.image | relative_url }}"
                  alt="{{ post.title }}"
                  loading="lazy">
              {% else %}
                <img
                  src="{{ '/assets/images/logo.png' | relative_url }}"
                  alt="{{ post.title }}"
                  loading="lazy">
              {% endif %}

            </a>

            <div class="home-post-body">

              <span class="home-post-badge">Guias</span>

              <h3 class="home-post-title">
                <a href="{{ post.url | relative_url }}">
                  {{ post.title }}
                </a>
              </h3>

              <div class="home-post-date">
                Por {{ post.author | default: "Equipe de Análises" }}
                • {{ post.date | date: "%d/%m/%Y" }}
              </div>

            </div>

          </article>

        {% endfor %}

      {% else %}

        <p class="guides-empty-state">
          Em breve novos artigos publicados.
        </p>

      {% endif %}

    </div>

  </div>
</div>
