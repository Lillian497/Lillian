---
layout: default
title: 首頁
---
<div class="container">
  <h1>{{ site.title }}</h1>
  <p class="muted">{{ site.description }}</p>
</div>

<ul class="post-list container">
  {% for post in site.posts %}
    <li class="post-item">
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p class="meta">{{ post.date | date: "%Y-%m-%d" }}
        {% if post.categories and post.categories.size > 0 %}
          ·
          {% for c in post.categories %}
            <a class="chip" href="{{ '/categories/' | append: c | append: '.html' | relative_url }}">{{ c }}</a>{% unless forloop.last %}、{% endunless %}
          {% endfor %}
        {% endif %}
      </p>
      {% if post.excerpt %}<p class="excerpt">{{ post.excerpt | strip_html | truncate: 120 }}</p>{% endif %}
    </li>
  {% endfor %}
</ul>
