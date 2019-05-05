---
layout: page
title: Archive
---

<h3>Tech</h3>

{% for post in site.categories.Tech offset:3 %}
  <article class="post">
    <h1 class="post-title archive-post-categories">
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </h1>
  </article>
{% endfor %}
