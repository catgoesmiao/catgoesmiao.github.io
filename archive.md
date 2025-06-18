---
layout: default
title: all posts
permalink: /archive/
---

<h1>all posts</h1>
<ul>
{% assign currentYear = site.time | date: '%Y' | plus: 0 %}
{% assign maxYear = currentYear | plus: 1 %}

{% for year in (2020..maxYear) reversed %}
  {% assign yearHasPosts = false %}
  {% for post in site.posts %}
    {% assign postYear = post.date | date: '%Y' | plus: 0 %}
    {% if postYear == year %}
      {% assign yearHasPosts = true %}
    {% endif %}
  {% endfor %}
  
  {% if yearHasPosts or year == 2025 %}
    <li><a href="/blog/{{ year }}">{{ year }}</a></li>
  {% endif %}
{% endfor %}
</ul>
