---
title: Lucas Harden
layout: default
---
<div class="shop-header">
<h1 class="page-title">Lucas Harden</h1>
<p class="page-sub">My gift is administration. I build systems, leverage them as assets, and share solutions.</p>

<div class="social-row">
  <a href="https://youtube.com/@hardensystems" target="_blank" rel="noopener" aria-label="YouTube"><i class="fa-brands fa-youtube"></i></a>
  <a href="https://facebook.com/hardensystems" target="_blank" rel="noopener" aria-label="Facebook"><i class="fa-brands fa-facebook"></i></a>
  <a href="https://tiktok.com/@hardensystems" target="_blank" rel="noopener" aria-label="TikTok"><i class="fa-brands fa-tiktok"></i></a>
  <a href="https://instagram.com/hardensystems" target="_blank" rel="noopener" aria-label="Instagram"><i class="fa-brands fa-instagram"></i></a>
  <a href="https://x.com/hardensystems" target="_blank" rel="noopener" aria-label="X"><i class="fa-brands fa-x-twitter"></i></a>
  <a href="https://pinterest.com/hardensystems" target="_blank" rel="noopener" aria-label="Pinterest"><i class="fa-brands fa-pinterest"></i></a>
  <a href="https://linkedin.com/in/hardensystems" target="_blank" rel="noopener" aria-label="LinkedIn"><i class="fa-brands fa-linkedin"></i></a>
</div>
</div>

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

<div class="divider">
  <div class="tick"></div>
  <h2>Looking for something else?</h2>
  <div class="rule"></div>
</div>
<a class="door" href="{{ '/lucas-harden/content/' | relative_url }}" style="display:block;max-width:400px">
  <h3>Content</h3>
  <span class="sub">DIY, recipes, fitness, finance</span>
</a>

<p style="color:var(--text-soft);font-size:13px;margin-top:24px">Some links above are affiliate/referral links — using them may earn me a commission or reward at no extra cost to you.</p>
