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

<button class="email-badge" onclick="document.getElementById('email-popup').classList.toggle('open')">20% OFF MES METHOD</button>

<div id="email-popup" class="email-popup">
<button class="email-popup-close" onclick="document.getElementById('email-popup').classList.remove('open')">&times;</button>
<div id="mlb2-44596719" class="ml-form-embedContainer ml-subscribe-form ml-subscribe-form-44596719">
<div class="ml-form-align-left">
<div class="ml-form-embedWrapper embedForm" style="width:100%">
<div class="ml-form-embedBody ml-form-embedBodyDefault row-form" style="padding:0">
<div class="ml-form-embedContent">
<h4 style="font-family:var(--serif);color:var(--ink);font-size:19px;font-weight:600;margin:0 0 8px">Get 20% Off MES Method</h4>
<p style="font-family:var(--sans);color:var(--text-soft);font-size:13px;margin:0 0 14px">Join the list and get your discount code instantly.</p>
</div>
<form class="ml-block-form" action="https://assets.mailerlite.com/jsonp/2562136/forms/195144779019847586/subscribe" data-code="" method="post" target="_blank">
<div class="ml-form-formContent">
<div class="ml-form-fieldRow ml-last-item">
<div class="ml-field-group ml-field-email ml-validate-email ml-validate-required">
<input aria-label="email" aria-required="true" type="email" class="form-control" name="fields[email]" placeholder="Email" autocomplete="email" style="font-family:var(--sans);border:1px solid var(--line);border-radius:4px;padding:10px;width:100%;box-sizing:border-box">
</div>
</div>
</div>
<input type="hidden" name="ml-submit" value="1">
<div class="ml-form-embedSubmit">
<button type="submit" class="primary" style="background:var(--ink);color:#EFEDE6;font-family:var(--mono);font-size:13px;border:none;border-radius:4px;padding:10px;width:100%;cursor:pointer">Subscribe</button>
</div>
<input type="hidden" name="anticsrf" value="true">
</form>
</div>
<div class="ml-form-successBody row-success" style="display:none;padding:0">
<div class="ml-form-successContent">
<h4 style="font-family:var(--serif);color:var(--ink);font-size:19px;font-weight:600;margin:0 0 8px">Here's your code!</h4>
<p style="font-family:var(--sans);color:var(--text-soft);font-size:14px;margin:0">Use code WELCOME20 at checkout for 20% off.</p>
</div>
</div>
</div>
</div>
</div>

<script>
function ml_webform_success_44596719() {
var $ = ml_jQuery || jQuery;
$('.ml-subscribe-form-44596719 .row-success').show();
$('.ml-subscribe-form-44596719 .row-form').hide();
}
</script>
<script src="https://groot.mailerlite.com/js/w/webforms.min.js?v83147fa8ce2d95cb73ece7f28b469519" type="text/javascript"></script>

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
<div class="doors">
  <a class="door" href="{{ '/lucas-harden/content/' | relative_url }}">
    <h3>Content</h3>
    <span class="sub">DIY, recipes, fitness, finance</span>
  </a>
  <a class="door" href="{{ '/amber-harden/' | relative_url }}">
    <h3>Amber Harden</h3>
    <span class="sub">Devotional · Face Painting</span>
  </a>
</div>
<p style="color:var(--text-soft);font-size:13px;margin-top:24px">Some links above are affiliate/referral links — using them may earn me a commission or reward at no extra cost to you.</p>
