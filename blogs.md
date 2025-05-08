---
layout: default
title: Blogs
---

<h1>Blogs</h1>
<ul>
  {% assign filtered_blogs = site.blogs | where_exp: "blog", "blog.path contains 'x_' and blog.path ends_with '.md'" %}
  {% for blog in filtered_blogs %}
    <li><a href="{{ blog.url | relative_url }}">{{ blog.title }}</a></li>
  {% endfor %}
</ul>
