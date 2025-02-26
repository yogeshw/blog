---
layout: default
title: Home
---

<div class="home">
  <section class="featured-posts">
    <h2>Latest Posts</h2>
    <div class="post-grid">
      {% for post in site.posts limit:6 %}
        <article class="post-card">
          {% if post.coverImage %}
          <div class="post-card-image">
            <img src="{{ post.coverImage | relative_url }}" alt="{{ post.title }}">
          </div>
          {% endif %}
          <div class="post-card-content">
            <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
            <div class="post-meta">
              <time>{{ post.date | date: "%B %-d, %Y" }}</time>
              {% if post.readingTime %}
              <span class="reading-time">{{ post.readingTime }}</span>
              {% endif %}
            </div>
            <p class="excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
            <div class="post-tags">
              {% for tag in post.tags %}
                <a href="{{ '/tags/' | relative_url }}#{{ tag }}" class="tag">{{ tag }}</a>
              {% endfor %}
            </div>
          </div>
        </article>
      {% endfor %}
    </div>
  </section>
</div>