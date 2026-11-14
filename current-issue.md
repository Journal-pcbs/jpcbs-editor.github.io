---
title: Current Issue
permalink: /current-issue/
---
{% assign cv = site.current_issue.volume %}{% assign ci = site.current_issue.issue %}
# Current issue: Volume {{ cv }}, Issue {{ ci }}
<ul class="list">
{% assign arts = site.articles | sort: 'date' | reverse %}{% assign n = 0 %}
{% for a in arts %}{% if a.volume == cv and a.issue == ci %}{% assign n = n | plus: 1 %}
<li><a href="{{ a.url | relative_url }}">{{ a.title }}</a><br><span class="meta">{% for au in a.authors %}{{ au.name }}{% unless forloop.last %}, {% endunless %}{% endfor %} &middot; {{ a.type | default: "Original Research Article" }}{% if a.doi %} &middot; DOI {{ a.doi }}{% endif %}</span></li>
{% endif %}{% endfor %}
{% if n == 0 %}<li>This issue is in preparation. Published articles will be listed here.</li>{% endif %}
</ul>
