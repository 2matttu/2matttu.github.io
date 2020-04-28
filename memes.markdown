---
layout: page
title: Memes
permalink: /memes
---

{% assign sorted_memes = (site.memes | sort: 'date') | reverse %}
{% for meme in sorted_memes %}
---
---
# *{{ meme.date | date: '%B %d, %Y' }}* - Posted to **{{ meme.group }}**
{% if meme.link %}
<a href="{{ meme.link }}">Source</a>
{% endif %}
![meme]({{meme.src}} "meme")

{% endfor %}