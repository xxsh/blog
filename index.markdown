---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Sun Hao's Blog
---

<div class="posts">
  <h1>最新文章</h1>
  
  {% for post in site.posts %}
    <article class="post-preview">
      <h2>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      <div class="post-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">
          {{ post.date | date: "%Y-%m-%d" }}
        </time>
      </div>
      {% if post.description %}
        <p class="post-description">{{ post.description }}</p>
      {% endif %}
      {% if post.excerpt %}
        <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
      {% endif %}
      <a href="{{ post.url | relative_url }}" class="read-more">阅读全文 &raquo;</a>
    </article>
  {% endfor %}
</div>
