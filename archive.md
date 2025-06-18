---
layout: default
title: all posts
permalink: /archive/
---

<h1>all posts</h1>
<ul>

 <div id="2025">
## 2025 posts
{% assign posts_2025 = site.posts | where_exp: "post", "post.date contains '2025'" %}
{% for post in posts_2025 %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%b %d, %Y" }}
{% else %}
empty...
{% endfor %}
</div>

</ul>
