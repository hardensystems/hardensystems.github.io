---
title: Content
layout: default
permalink: /lucas-harden/content/
---
<h1 class="page-title">Content</h1>
<p class="page-sub">Everything filed by topic. New pieces get tagged and added here as they're made.</p>

<div class="doors">
  <a class="door" href="{{ '/lucas-harden/content/topics/diy/' | relative_url }}">
    <div class="num">1</div>
    <h3>DIY & Home Repair</h3>
  </a>
  <a class="door" href="{{ '/lucas-harden/content/topics/recipes/' | relative_url }}">
    <div class="num">2</div>
    <h3>Homemade Recipes</h3>
  </a>
  <a class="door" href="{{ '/lucas-harden/content/topics/fitness/' | relative_url }}">
    <div class="num">3</div>
    <h3>Fitness</h3>
  </a>
  <a class="door" href="{{ '/lucas-harden/content/topics/finance/' | relative_url }}">
    <div class="num">4</div>
    <h3>Finance</h3>
  </a>
</div>

<div class="divider">
  <div class="tick"></div>
  <h2>All content</h2>
  <div class="rule"></div>
</div>

<div class="latest-list">
  {% assign items = site.content | sort: "date" | reverse %}
  {% for item in items %}
  <a class="latest-item" href="{{ item.url | relative_url }}">
    <span class="title">{{ item.title }}</span>
    <span class="tag">{% if item.tags %}{{ item.tags | join: ", " }}{% endif %}</span>
  </a>
  {% endfor %}
  {% if items.size == 0 %}
  <p class="empty-note">Nothing published yet — first pieces are on the way.</p>
  {% endif %}
</div>
