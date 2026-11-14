---
title: Archive
permalink: /archive/
---
# Archive
{% assign arts = site.articles | sort: 'date' | reverse %}
{% assign groups = arts | group_by_exp: "a", "a.volume | append: '.' | append: a.issue" %}
{% for g in groups %}{% assign f = g.items | first %}
## Volume {{ f.volume }}, Issue {{ f.issue }} ({{ f.date | date: '%Y' }})
<ul class="list">{% for a in g.items %}<li><a href="{{ a.url | relative_url }}">{{ a.title }}</a><br><span class="meta">{% for au in a.authors %}{{ au.name }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span></li>{% endfor %}</ul>
{% else %}No issues have been published yet.{% endfor %}
