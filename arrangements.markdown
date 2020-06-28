---
layout: page
title: Arrangements
permalink: /arrangements/
---
 
I've written {{ site.arrangements.size }} arrangements for the Yale Precision Marching Band so far. More to come!

{% assign sorted_arrangements = (site.arrangements | sort: 'date') | reverse %}

<table>
    {% for x in sorted_arrangements %}
    <tr>
        <td>
            <strong>{{x.title}}</strong> by {{x.composer}}
        </td>
        <td>
            <a href="{{ x.src }}" target="_blank">PDF</a>
        </td>
        <td>
            {% if x.link %}
            <a href="{{ x.link }}" target="_blank">Listen</a>
            {% else %}
            -
            {% endif %}
        </td>
    </tr>
    {% endfor %}
</table>
<p> Virtual recordings were made using <a href="https://www.noteperformer.com/" target="_blank">NotePerfomer 3</a>.</p>