---
layout: page
title: Poems
---

<table>
    {% for poem in site.poem %}
    <tr>
        <td class="align-content-left"> {{poem.title}} </td>
        <td class="align-content-right"><a href="{{poem.url}}">{{ poem.content | strip_html | truncate: 35 }}</a></td>
    </tr>
    {% endfor %}
</table>
