---
layout: page
title: Archive
---

<h3 id="tech">Tech</h3>

{% for post in site.categories.Tech offset:3 %}
  <article class="post archive-post">
    <h1 class="post-title">
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </h1>
  </article>
{% endfor %}
