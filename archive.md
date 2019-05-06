---
layout: page
title: Archive
---

<h3 id="tech" class="archive-categories">Tech</h3>

{% for post in site.categories.Tech offset:3 %}
  <article class="post archive-post">
    <h1 class="post-title">
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </h1>
  </article>
{% endfor %}

<h3 id="finance" class="archive-categories">Finance</h3>

{% for post in site.categories.Finance offset:3 %}
  <article class="post archive-post">
    <h1 class="post-title">
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </h1>
  </article>
{% endfor %}

<h3 id="health" class="archive-categories">Health</h3>

{% for post in site.categories.Health offset:3 %}
  <article class="post archive-post">
    <h1 class="post-title">
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </h1>
  </article>
{% endfor %}
