---
layout: default
title: Categories
permalink: /categories/
---
<main class="container">
  <h1>分類</h1>
  <ul class="cat-list">
    {% for c in site.categories %}
      {% assign cname = c[0] %}
      {% assign posts = c[1] %}
      <li>
        <a href="{{ '/categories/' | append: cname | append: '.html' | relative_url }}" class="chip">#{{ cname }}</a>
        <span class="muted">（{{ posts | size }} 篇）</span>
      </li>
    {% endfor %}
  </ul>
</main>
