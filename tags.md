---
layout: default
title: Tags
permalink: /tags
---

<h1 class="page-title">$ ls ./tags</h1>

{% assign tags = site.tags | sort %}
{% for tag in tags %}
<div class="tag-group" id="{{ tag[0] }}">
  <h2 class="tag-name"><span>#</span>{{ tag[0] }} <small style="color:var(--text-dim);font-size:0.75rem;">({{ tag[1].size }} posts)</small></h2>
  <ul class="category-posts">
    {% for post in tag[1] %}
    <li>
      <time>{{ post.date | date: "%b %d, %Y" }}</time>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
  </ul>
</div>
{% endfor %}
