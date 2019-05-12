---
layout: page
title: Health
---

{% for post in site.categories.Health limit:3 %}
  <article class="post">
    <h1 class="post-title-category">
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </h1>
    {% assign ncut = 300 %}
    {% assign words = post.content | strip_newlines | markdownify | strip_html | truncate: ncut, "" | number_of_words | decrement %}
    {{ post.content | strip_newlines | markdownify | strip_html | truncatewords: words, " (...)" }}
    <p><a class="post-more" href="{{ post.url }}">Read more</a></p>
  </article>
{% endfor %}

<h4><a href="/archive#health">See other health articles on the archive</a></h4>
