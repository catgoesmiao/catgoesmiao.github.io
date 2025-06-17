---
layout: default
title: All Posts
---
<h1>All Posts</h1>
<ul>
  {% for post in site.posts %}
    <li>
      [{{ post.date | date: "%Y" }}] 
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
