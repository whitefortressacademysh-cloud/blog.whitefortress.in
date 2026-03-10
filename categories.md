---
layout: default
title: Categories
permalink: /categories
---

<h1 class="page-title">$ ls ./categories</h1>

{% assign categories = site.categories | sort %}
{% for category in categories %}
<div class="category-group" id="{{ category[0] }}">
  <h2 class="category-name"><span>#</span>{{ category[0] }} <small style="color:var(--text-dim);font-size:0.75rem;">({{ category[1].size }} posts)</small></h2>
  <ul class="category-posts">
    {% for post in category[1] %}
    <li>
      <time>{{ post.date | date: "%b %d, %Y" }}</time>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
  </ul>
</div>
{% endfor %}
