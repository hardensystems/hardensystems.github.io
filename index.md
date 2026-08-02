---
title: Home
layout: default
---
<div class="hero">
  <h1>Harden Systems</h1>
  <p>Build once, benefit forever.</p>
</div>

<div class="doors">
  <a class="door" href="{{ '/lucas-harden/' | relative_url }}">
    <h3>Lucas Harden</h3>
    <span class="sub">Systems · Faith · Finance</span>
  </a>
  <a class="door" href="{{ '/amber-harden/' | relative_url }}">
    <h3>Amber Harden</h3>
    <span class="sub">Devotional · Face Painting</span>
  </a>
  <a class="door" href="{{ '/kids/' | relative_url }}">
    <h3>Kids</h3>
    <span class="sub">Family</span>
  </a>
</div>

<div class="divider">
  <div class="tick"></div>
  <h2>Shop the essentials</h2>
  <div class="rule"></div>
</div>

<div class="shop-thumbs">
  <a class="thumb-card" href="https://hardensystems.gumroad.com/l/MES?layout=profile" target="_blank" rel="noopener">
    <div class="thumb-img">Photo coming soon</div>
    <div class="thumb-title">MES Method</div>
    <div class="thumb-sub">12-week fitness system</div>
  </a>
  <a class="thumb-card" href="{{ '/amber-harden/' | relative_url }}">
    <div class="thumb-img">Photo coming soon</div>
    <div class="thumb-title">Amber's Devotional</div>
    <div class="thumb-sub">Illustrated devotional book</div>
  </a>
</div>

<div class="divider">
  <div class="tick"></div>
  <h2>Latest</h2>
  <div class="rule"></div>
</div>

<div class="latest-list">
  {% assign items = site.content | sort: "date" | reverse %}
  {% for item in items limit: 6 %}
  <a class="latest-item" href="{{ item.url | relative_url }}">
    <span class="title">{{ item.title }}</span>
    <span class="tag">{% if item.tags %}{{ item.tags | first }}{% endif %}</span>
  </a>
  {% endfor %}
  {% if items.size == 0 %}
  <p class="empty-note">New content is in the works — check back soon.</p>
  {% endif %}
</div>
