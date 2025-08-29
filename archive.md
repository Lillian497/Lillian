---
layout: default
title: Archive
permalink: /archive/
---
<main class="container">
  <h1>文章歸檔</h1>
  {% assign years = site.posts | group_by_exp:'post', 'post.date | date: "%Y"' %}
  {% for y in years %}
  <section class="year-block">
    <h2 class="year">{{ y.name }}</h2>
    <ul class="timeline">
      {% for post in y.items %}
      <li class="tl-item">
        <span class="date">{{ post.date | date: "%m-%d" }}</span>
        <a class="title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
        {% if post.categories and post.categories.size > 0 %}
        <span class="cats">
          {% for c in post.categories %}
            <a class="chip small" href="{{ '/categories/' | append: c | append: '.html' | relative_url }}">#{{ c }}</a>
          {% endfor %}
        </span>
        {% endif %}
      </li>
      {% endfor %}
    </ul>
  </section>
  {% endfor %}
</main>
