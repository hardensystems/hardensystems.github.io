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
  <a class="latest-item" href="{{ item.url | relative_url }}">
    <span class="title">{{ item.title }}</span>
    <span class="tag">{{ item.date | date: "%b %Y" }}</span>
  </a>
  {% endfor %}
  {% if items.size == 0 %}
  <p class="empty-note">Nothing filed here yet — more is on the way.</p>
  {% endif %}
</div>
