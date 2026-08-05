---
title: "Finance"
layout: default
permalink: /lucas-harden/content/topics/finance/
---
<h1 class="page-title">Finance</h1>
<p class="page-sub">Debt-free strategies, budgeting systems, and building financial freedom.</p>

<div class="latest-list">
  {% assign items = site.content | where_exp: "item", "item.tags contains 'finance'" | sort: "date" | reverse %}
  {% for item in items %}
  {% assign thumb = item.thumbnail %}
  {% if item.video_id and item.platform == "YouTube" %}{% assign thumb = "https://img.youtube.com/vi/" | append: item.video_id | append: "/hqdefault.jpg" %}{% endif %}
  <a class="latest-item" href="{% if item.external_url %}{{ item.external_url }}{% else %}{{ item.url | relative_url }}{% endif %}"{% if item.external_url %} target="_blank" rel="noopener"{% endif %}>
    {% if thumb %}<img class="latest-thumb" src="{% unless thumb contains 'http' %}{{ thumb | relative_url }}{% else %}{{ thumb }}{% endunless %}" alt="">{% endif %}
    <div class="latest-text">
      <span class="title">{{ item.title }}</span>
      <span class="tag">{{ item.date | date: "%b %Y" }}</span>
    </div>
  </a>
  {% endfor %}
  {% if items.size == 0 %}
  <p class="empty-note">Nothing filed here yet — more is on the way.</p>
  {% endif %}
</div>
