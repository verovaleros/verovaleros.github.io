---
layout: default
title: Blog
---

# Blog
{% for post in site.posts %}
  <div class="post">
    <p class="date"><small>{{ post.date | date: "%-d %B %Y" }} Tags: <em>{{ post.tags | join: "</em> - <em>" }}</em></small></p>
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
  </div>
{% endfor %}
