---
title: Content
layout: default
permalink: /lucas-harden/content/
---
<h1 class="page-title">Content</h1>
<p class="page-sub">Everything filed by topic. New pieces get tagged and added here as they're made.</p>

<div class="doors">
  <a class="door" href="{{ '/lucas-harden/content/topics/diy/' | relative_url }}">
    <h3>DIY & Home Repair</h3>
  </a>
  <a class="door" href="{{ '/lucas-harden/content/topics/recipes/' | relative_url }}">
    <h3>Homemade Recipes</h3>
  </a>
  <a class="door" href="{{ '/lucas-harden/content/topics/fitness/' | relative_url }}">
    <h3>Fitness</h3>
  </a>
  <a class="door" href="{{ '/lucas-harden/content/topics/finance/' | relative_url }}">
    <h3>Finance</h3>
  </a>
  <a class="door" href="{{ '/lucas-harden/content/topics/review/' | relative_url }}">
    <h3>Reviews</h3>
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
  {% assign thumb = item.thumbnail %}
  {% if item.video_id and item.platform == "YouTube" %}{% assign thumb = "https://img.youtube.com/vi/" | append: item.video_id | append: "/hqdefault.jpg" %}{% endif %}
  <a class="latest-item" href="{% if item.external_url %}{{ item.external_url }}{% else %}{{ item.url | relative_url }}{% endif %}"{% if item.external_url %} target="_blank" rel="noopener"{% endif %}>
    {% if thumb %}<img class="latest-thumb" src="{% unless thumb contains 'http' %}{{ thumb | relative_url }}{% else %}{{ thumb }}{% endunless %}" alt="">{% endif %}
    <div class="latest-text">
      <span class="title">{{ item.title }}</span>
      <span class="tag">{% if item.tags %}{{ item.tags | join: ", " }}{% endif %}</span>
    </div>
  </a>
  {% endfor %}
  {% if items.size == 0 %}
  <p class="empty-note">Nothing published yet — first pieces are on the way.</p>
  {% endif %}
</div>
