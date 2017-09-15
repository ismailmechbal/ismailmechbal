---
layout: page
title: Ismail Mechbal - Product Engineer
---
<h1 class="f1 mv0">Ismail Mechbal</h1>
<h3 class="f3 fw3 mb0">A passionate nurse that likes elevating patient's well being</h3>
<p class="f3">Love to be helping changes in how Healthcare is delivered to citizens</p>
<ul class="links f3">
  {% for socialmedia in site.data.socialmedia %}
    <li class="pv2">
      <a href="{{ socialmedia.url }}" class="link pointer dim" title="{{ socialmedia.name }}">
        {{ socialmedia.name }}
      </a>
    </li>
  {% endfor %}
</ul>