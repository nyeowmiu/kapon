---
layout: default # Or whatever layout your homepage uses
title: Kapon Hindi Tapon
---

<h1>Latest Posts</h1>

#Displays a snippet of the post
{% for post in site.posts %}
  <div class="post-preview">
    <h2>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>
    <p class="post-meta">
      {{ post.date | date: "%B %d, %Y" }}
    </p>
     {{ post.excerpt | markdownify }} 
    <a href="{{ post.url | relative_url }}">Read More &rarr;</a>
  </div>
  [comment]: # (Optional: Adds a horizontal line between posts)
  <hr> 
{% endfor %}
