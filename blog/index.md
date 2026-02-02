---
title: Blog
layout: page
---

<div class="blog-list">
  {% for post in site.blog %}
    <article class="blog-card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="post-meta">{{ post.date | date: "%B %d, %Y" }}</p>
      <p>{{ post.excerpt | strip_html | truncate: 140 }}</p>
    </article>
  {% endfor %}
</div>
