---
title: "DIY & Home Repair"
layout: default
permalink: /lucas-harden/content/topics/diy/
---
<h1 class="page-title">DIY & Home Repair</h1>
<p class="page-sub">Fixes, builds, and projects around the house.</p>

<div class="latest-list">
  {% assign items = site.content | where_exp: "item", "item.tags contains 'diy'" | sort: "date" | reverse %}
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
