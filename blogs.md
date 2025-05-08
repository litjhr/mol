---
layout: default
title: Blogs
---

{% assign collection_name = "blogs" %}  
<h1>{{ collection_name | capitalize }}</h1> 
<ul>
  {% assign filtered_items = site[collection_name] | where_exp: "item", "item.path contains 'x_' and item.path ends_with '.md'" %}
  {% for item in filtered_items %}
    <li><a href="{{ item.url | relative_url }}">{{ item.title }}</a></li>
  {% for %}
</ul>
