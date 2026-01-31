---
layout: default
title: Blog
---

# Blog
<div class="post-index">
  {% for post in site.posts %}
    <article class="post-card">
      <div class="post-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%-d %B %Y" }}</time>
        {% if post.tags and post.tags.size > 0 %}
          <span class="meta-sep">•</span>
          <span class="tag-label">Tags</span>
          <ul class="tag-list">
            {% for tag in post.tags %}
              <li>{{ tag }}</li>
            {% endfor %}
          </ul>
        {% endif %}
      </div>
      <h2 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      {% if post.excerpt %}
        <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 180 }}</p>
      {% endif %}
      <a class="post-read" href="{{ post.url | relative_url }}">Read post →</a>
    </article>
  {% endfor %}
</div>
