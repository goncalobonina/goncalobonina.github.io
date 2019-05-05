---
layout: page
title: Archive
---

<h1 class="page-title">Tech</h1>

{% for post in site.categories.Tech offset:3 %}
  <article class="post">
    <h1 class="post-title">
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </h1>
  </article>
{% endfor %}
