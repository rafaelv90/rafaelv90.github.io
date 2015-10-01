---
layout: blog
title: Blog
permalink: /blog/
---

<div class="post-list">
  {% for post in site.posts %}
    <div class="post">
      <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      <p class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</p>
      <p class="excerpt">{{ post.excerpt | strip_html }}</p>
    </div>
    <div class="separator"></div>
  {% endfor %}
</div>
