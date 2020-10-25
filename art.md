---
layout: page
title: Art
---

<ul>
  {% for post in site.paintings %}
    <li itemscope>
       <a href="{{ site.github.url }}{{ post.url }}">{{ post.title }}</a>
    </li>

{% endfor %}

</ul>
