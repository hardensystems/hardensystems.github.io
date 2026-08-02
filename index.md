---
title: Home
layout: default
---
<div class="hero">
  <div class="eyebrow">Systems for the body, the budget, and the build</div>
  <h1>Harden Systems</h1>
  <p>DIY, homemade recipes, fitness, and finance — built once, useful for years.</p>
</div>

<div class="doors">
  <a class="door" href="{{ '/lucas-harden/' | relative_url }}">
    <div class="num">01</div>
    <h3>Lucas Harden</h3>
    <span class="sub">DIY · finance · fitness</span>
  </a>
  <a class="door" href="{{ '/amber-harden/' | relative_url }}">
    <div class="num">02</div>
    <h3>Amber Harden</h3>
    <span class="sub">Devotional</span>
  </a>
  <a class="door" href="{{ '/kids/' | relative_url }}">
    <div class="num">03</div>
    <h3>Kids</h3>
    <span class="sub">Family</span>
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
