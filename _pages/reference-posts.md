---
layout: page
title: "Reference Posts"
permalink: /reference-posts/
---

Here are some reference posts for future use:

<ul>
  {% for post in site.posts %}
    {% if post.path contains '_reference_posts' %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
