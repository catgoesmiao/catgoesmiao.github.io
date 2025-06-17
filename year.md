---
layout: default
---

<h1>posts from {{ page.year }}</h1>

<ul>
  {% assign filtered_posts = site.posts | where_exp: "post", "post.date | date: '%Y' == page.year" %}
  
  {% if filtered_posts.size > 0 %}
    {% for post in filtered_posts %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title | downcase }}</a>
        <span class="date">- {{ post.date | date: "%b %d" }}</span>
      </li>
    {% endfor %}
  {% else %}
    <p>no posts found for {{ page.year }}. check back later!</p>
  {% endif %}
</ul>
