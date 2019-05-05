---
layout: page
title: Tech
---

{% for post in site.categories.Tech %}
  <article class="post">
    <h1 class="post-title">
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </h1>
    {% assign ncut = 300 %}
    {% assign words = post.content | strip_newlines | markdownify | strip_html | truncate: ncut, "" | number_of_words | decrement %}
    {{ post.content | strip_newlines | markdownify | strip_html | truncatewords: words, " (...)" }}
    <p><a class="post-more" href="{{ post.url }}">Read more</a></p>
  </article>
{% endfor %}
