---
title: "Homemade Recipes"
layout: default
permalink: /lucas-harden/content/topics/recipes/
---
<h1 class="page-title">Homemade Recipes</h1>
<p class="page-sub">Things I've made from scratch — hair products, electrolyte mixes, and more.</p>

<div class="latest-list">
  {% assign items = site.content | where_exp: "item", "item.tags contains 'recipes'" | sort: "date" | reverse %}
  {% for item in items %}
  <a class="latest-item" href="{{ item.url | relative_url }}">
    <span class="title">{{ item.title }}</span>
    <span class="tag">{{ item.date | date: "%b %Y" }}</span>
  </a>
  {% endfor %}
  {% if items.size == 0 %}
  <p class="empty-note">Nothing filed here yet — more is on the way.</p>
  {% endif %}
</div>
