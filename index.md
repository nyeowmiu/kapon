---
title: Kapon Hindi Tapon
---

<h1>Latest Posts</h1>

{% for post in site.posts %}
  <div class="post-preview">
    <h2>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>
    <p class="post-meta">
      {{ post.date | date: "%B %d, %Y" }}
    </p>
    {{ post.excerpt | markdownify }} {# Displays a snippet of the post #}
    <a href="{{ post.url | relative_url }}">Read More &rarr;</a>
  </div>
  <hr> {# Optional: Adds a horizontal line between posts #}
{% endfor %}
