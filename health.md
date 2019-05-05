---
layout: page
title: Health
---

<div class="posts">
  {% for post in site.categories.haircare limit:6 %}
  <div class="post">
    {% for tags in post.tags %}
      <h3 class="post-tags">{{ post.tags }}</h3>
    {% unless forloop.last %}{% endunless %}
    {% endfor %}
    <h1 class="post-title">
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>
    {% assign ncut = 300 %}
    {% assign words = post.content | strip_newlines | markdownify | strip_html | truncate: ncut, "" | number_of_words | decrement %}
    {{ post.content | strip_newlines | markdownify | strip_html | truncatewords: words, " (...)" }}
    <p><a class="post-more" href="{{ post.url }}">Read more</a></p>
  </div>
  {% endfor %}
</div>
