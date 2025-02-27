---
layout: home
title: Home
---

## Latest Articles

{% for post in site.posts limit:5 %}
  <div class="post-preview">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p class="post-meta">{{ post.date | date: "%B %d, %Y" }}</p>
    <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    <a href="{{ post.url | relative_url }}">Read more...</a>
  </div>
  <hr>
{% endfor %}

{% if site.posts.size > 5 %}
  <a href="/blog" class="all-posts-link">View all articles →</a>
{% endif %}