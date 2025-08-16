---
layout: default
title: "Momo in RA"
---

<h2>📝 最新文章</h2>

<ul class="post-list">
  {% for post in site.posts limit: 10 %}
    <li class="post-item">
      {% if post.image %}
        <a href="{{ post.url | relative_url }}" class="thumb-wrap" aria-label="{{ post.title }}">
          <img
            src="{{ site.baseurl }}{{ post.image }}"
            alt="{{ post.title }}"
            class="post-thumb"
            loading="lazy"
            width="240" height="160">
        </a>
      {% endif %}
      <div class="post-info">
        <h3 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
        <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 120 }}</p>
      </div>
    </li>
  {% endfor %}
</ul>
