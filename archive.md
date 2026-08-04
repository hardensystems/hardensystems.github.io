---
title: All Content
layout: default
permalink: /archive/
---
<h1 class="page-title">All Content</h1>
<p class="page-sub">Everything, newest first.</p>

<div class="latest-list">
  {% assign items = site.content | sort: "date" | reverse %}
  {% for item in items %}
  <a class="latest-item" href="{% if item.external_url %}{{ item.external_url }}{% else %}{{ item.url | relative_url }}{% endif %}"{% if item.external_url %} target="_blank" rel="noopener"{% endif %}>
    <span class="title">{{ item.title }}</span>
    <span class="tag">{% if item.tags %}{{ item.tags | first }}{% endif %}{% if item.platform %} &middot; {{ item.platform }}{% endif %} &middot; {{ item.date | date: "%b %-d, %Y" }}</span>
  </a>
  {% endfor %}
  {% if items.size == 0 %}
  <p class="empty-note">Nothing published yet.</p>
  {% endif %}
</div>
