---
layout: default
title: all posts
permalink: /archive/
---

<h1>all posts</h1>
<ul>
## by year

{% assign current_year = site.time | date: '%Y' | plus: 0 %}
{% assign max_year = current_year | plus: 1 %}

{% for year in (2020..max_year) reversed %}
  {% assign year_has_posts = false %}
  {% for post in site.posts %}
    {% assign post_year = post.date | date: '%Y' | plus: 0 %}
    {% if post_year == year %}
      {% assign year_has_posts = true %}
    {% endif %}
  {% endfor %}
  
  {% if year_has_posts or year == 2025 %}
- [{{ year }}](/blog/{{ year }})
  {% endif %}
{% endfor %}
</ul>
