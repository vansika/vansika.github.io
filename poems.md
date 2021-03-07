---
layout: page
title: Poems
---

<table>
    {% for poem in site.poems %}
    <tr>
        <td> {{poem.title}} </td>
        <td><a href="{{poem.url}}">{{ poem.content | strip_html | truncate: 35 }}</a></td>
    </tr>
    {% endfor %}
</table>
