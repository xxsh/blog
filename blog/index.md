---
layout: default
title: 博客
permalink: /blog/
---

<h1>{{ page.title }}</h1>

<div class="post-list">
  {% for post in site.posts %}
    <article class="post-preview">
      <h2>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </h2>
      <time datetime="{{ post.date | date_to_xmlschema }}">
        {{ post.date | date: "%Y-%m-%d" }}
      </time>
      {% if post.description %}
        <p>{{ post.description }}</p>
      {% endif %}
    </article>
  {% endfor %}
</div>

