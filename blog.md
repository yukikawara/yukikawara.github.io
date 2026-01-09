---
layout: page
title: ブログ
permalink: /blog/
---

<div class="blog-posts">
  {% for post in site.posts %}
    <article class="post-preview">
      <h2>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h2>

      <p class="post-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">
          {{ post.date | date: "%Y年%m月%d日" }}
        </time>
        {% if post.author %}
          • {{ post.author }}
        {% endif %}
      </p>

      {% if post.excerpt %}
        <div class="post-excerpt">
          {{ post.excerpt | strip_html | truncate: 200 }}
        </div>
      {% endif %}

      <p><a href="{{ post.url | relative_url }}">続きを読む →</a></p>
    </article>

    {% unless forloop.last %}<hr>{% endunless %}
  {% endfor %}

  {% if site.posts.size == 0 %}
    <p>まだブログ記事がありません。</p>
  {% endif %}
</div>