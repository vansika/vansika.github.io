---
layout: page
title: Poetry
---

<ul>
  {% for post in site.poems %}
    <li itemscope>
       <a href="{{ site.github.url }}{{ post.url }}">{{ post.title }}</a>
    </li>

{% endfor %}

</ul>
