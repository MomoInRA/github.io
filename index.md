---
layout: default
title: "Momo in RA"
---

<h1>最新文章</h1>
<ul>
  {% for post in paginator.posts %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>

<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}">← 上一頁</a>
  {% endif %}
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}">下一頁 →</a>
  {% endif %}
</div>
