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
</div>
<div class="divider">
  <div class="tick"></div>
  <h2>Shop the essentials</h2>
  <div class="rule"></div>
</div>
<div class="shop-thumbs">
  <a class="thumb-card" href="https://hardensystems.gumroad.com/l/MES?layout=profile" target="_blank" rel="noopener">
   <div class="thumb-img"><img src="{{ '/assets/Minimalist%20MES%20METHOD%20Logo%20on%20Navy%20Background.jpg' | relative_url }}" style="width:100%;height:100%;object-fit:cover;border-radius:4px"></div>
    <div class="thumb-title">MES Method</div>
   <div class="thumb-sub">12-week fitness program</div>
  </a>
<a class="thumb-card" href="https://www.amazon.com/Battle-Mind-Amber-Harden/dp/B0H3F2VDJC/" target="_blank" rel="noopener">
  <div class="thumb-img"><img src="{{ '/assets/BOTM%20Sq.png' | relative_url }}" style="width:100%;height:100%;object-fit:cover;border-radius:4px"></div>
    <div class="thumb-title">Battle of the Mind</div>
    <div class="thumb-sub">Amber's Devotional</div>
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
  {% assign thumb = item.thumbnail %}
  {% if item.video_id and item.platform == "YouTube" %}{% assign thumb = "https://img.youtube.com/vi/" | append: item.video_id | append: "/hqdefault.jpg" %}{% endif %}
  <a class="latest-item" href="{% if item.external_url %}{{ item.external_url }}{% else %}{{ item.url | relative_url }}{% endif %}"{% if item.external_url %} target="_blank" rel="noopener"{% endif %}>
    {% if thumb %}<img class="latest-thumb" src="{% unless thumb contains 'http' %}{{ thumb | relative_url }}{% else %}{{ thumb }}{% endunless %}" alt="">{% endif %}
    <div class="latest-text">
      <span class="title">{{ item.title }}</span>
      <span class="tag">{% if item.tags %}{{ item.tags | first }}{% endif %}{% if item.platform %} &middot; {{ item.platform }}{% endif %}</span>
    </div>
  </a>
  {% endfor %}
  {% if items.size == 0 %}
  <p class="empty-note">New content is in the works — check back soon.</p>
  {% endif %}
</div>

{% if items.size > 6 %}
<div style="text-align:center;margin-top:20px">
  <a class="btn" href="{{ '/archive/' | relative_url }}">View More</a>
</div>
{% endif %}
