---
layout: default
title: All Posts
permalink: /archive/
---

<h1>all posts</h1>
<ul>
  {% for post in site.posts %}
    <li>
      [{{ post.date | date: "%Y" }}] 
      <a href="{{ post.url | relative_url }}">{{ post.title | downcase }}</a>
    </li>
  {% endfor %}
</ul>
