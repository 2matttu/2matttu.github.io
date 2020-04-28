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
<!-- | [Dance Monkey]() by Tones and I | [PDF](#) | - |
| [break up with your girlfriend, i'm bored]() by Ariana Grande | [PDF](#) | - |
| [小苹果 (XiaoPingGuo / Little Apple)]() by 筷子兄弟 (Chopstick Bros.) | [PDF](#) | [Video](#)
| [DDU-DU DDU-DU]() by BLACKPINK | [PDF](#) | - |
| [Naruto Main Theme]() by Toshiro Masuda (composer) | [PDF](#) | - |
| [THE HERO !! ("One Punch Man" Opening)]() by JAM Project | [PDF](#) | - |
| [Jungle Japes (from Donkey Kong)]() by Grant Kirkhope (composer) | [PDF](#) | - | -->