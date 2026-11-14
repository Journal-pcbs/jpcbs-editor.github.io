---
title: Home
---
<h1>Journal of Pharmaceutical Chemistry and Biosciences</h1>
<p class="lede">An independent scholarly journal for research in pharmaceutical chemistry, drug discovery and the biosciences.</p>
<p><a class="btn" href="{{ '/author-guidelines/' | relative_url }}">Submit a manuscript</a><a class="btn alt" href="{{ '/current-issue/' | relative_url }}">Read the current issue</a></p>

## Aims and scope
JPCBS publishes work that connects chemistry with biological and pharmaceutical questions, and encourages exchange among researchers, academics and students.
<ul class="scope">
<li>Pharmaceutical and medicinal chemistry</li><li>Drug discovery and drug design</li><li>Pharmaceutical analysis</li><li>Synthetic and natural product chemistry</li><li>Marine natural products</li><li>Pharmacology and biological evaluation</li><li>Biochemistry and molecular biosciences</li><li>Formulation and drug delivery</li><li>Polymer chemistry and pharmaceutical applications</li><li>Computational chemistry and molecular modelling</li>
</ul>

## Article types
Original research articles, review articles, short communications and research communications. Every submission goes through editorial screening and peer review ([policy]({{ '/publication-ethics/' | relative_url }})).

## Latest articles
<ul class="list">
{% assign latest = site.articles | sort: 'date' | reverse %}
{% for a in latest limit: 5 %}<li><a href="{{ a.url | relative_url }}">{{ a.title }}</a><br><span class="meta">{% for au in a.authors %}{{ au.name }}{% unless forloop.last %}, {% endunless %}{% endfor %} &middot; Vol. {{ a.volume }}({{ a.issue }}), {{ a.date | date: '%Y' }}</span></li>
{% else %}<li>The first issue is in preparation. Accepted articles will appear here as soon as they are published.</li>{% endfor %}
</ul>
