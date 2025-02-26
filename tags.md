---
layout: default
title: Topics
permalink: /tags/
---

<div class="tags-page">
  <h1>Topics</h1>
  
  {% assign tags = site.tags | sort %}
  <div class="tag-cloud">
    {% for tag in tags %}
      <a href="#{{ tag[0] }}" class="tag">{{ tag[0] }} ({{ tag[1].size }})</a>
    {% endfor %}
  </div>

  {% for tag in tags %}
    <section id="{{ tag[0] }}" class="tag-section">
      <h2>{{ tag[0] | capitalize }}</h2>
      <ul class="post-list">
        {% for post in tag[1] %}
          <li>
            <h3>
              <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            </h3>
            <div class="post-meta">
              <time>{{ post.date | date: "%B %-d, %Y" }}</time>
              {% if post.readingTime %}
              <span class="reading-time">{{ post.readingTime }}</span>
              {% endif %}
            </div>
            <p class="excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
          </li>
        {% endfor %}
      </ul>
    </section>
  {% endfor %}
</div>