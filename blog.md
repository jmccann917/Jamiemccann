---
layout: default
title: Ashes & Ink
permalink: /blog/
is_blog_index: true
---

<div class="blog-intro">
  Welcome to <em>Ashes & Ink</em> — where stories burn slow and love leaves a scar.
</div>

{% comment %}
  List of posts (simple version). If you prefer to list elsewhere, remove this block.
{% endcomment %}
<div class="blog-list">
  {% for post in site.posts %}
    <article class="post-card">
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p class="meta">{{ post.date | date: "%B %d, %Y" }}</p>
      <p class="excerpt">{{ post.excerpt | strip_html | truncate: 180 }}</p>
      <a href="{{ post.url | relative_url }}" class="read-more">Read post →</a>
    </article>
  {% endfor %}
</div>
