---
title: Shop
layout: default
---
<h1 class="page-title">Shop</h1>
<p class="page-sub">Everything I use, build, and recommend.</p>

{% assign featured_items = site.shop | where: "featured", true %}
{% if featured_items.size > 0 %}
<div class="divider">
  <div class="tick"></div>
  <h2>Featured</h2>
  <div class="rule"></div>
</div>
<div class="shop-grid">
  {% for item in featured_items %}
  <a class="shop-card" href="{{ item.url }}" target="_blank" rel="noopener">
    <div class="shop-card-img"><img src="{{ item.logo | relative_url }}"></div>
    <div class="shop-card-title">{{ item.title }}</div>
    <div class="shop-card-sub">{{ item.description }}</div>
  </a>
  {% endfor %}
</div>
{% endif %}

{% assign regular_items = site.shop | where_exp: "item", "item.featured != true" %}
{% assign grouped = regular_items | group_by: "category" %}
{% for group in grouped %}
<div class="divider">
  <div class="tick"></div>
  <h2>{{ group.name }}</h2>
  <div class="rule"></div>
</div>
<div class="shop-grid">
  {% for item in group.items %}
  <a class="shop-card" href="{{ item.url }}" target="_blank" rel="noopener">
    <div class="shop-card-img"><img src="{{ item.logo | relative_url }}"></div>
    <div class="shop-card-title">{{ item.title }}</div>
    <div class="shop-card-sub">{{ item.description }}</div>
  </a>
  {% endfor %}
</div>
{% endfor %}

<p style="color:var(--text-soft);font-size:13px;margin-top:8px">Some links above are affiliate/referral links — using them may earn me a commission or reward at no extra cost to you.</p>
