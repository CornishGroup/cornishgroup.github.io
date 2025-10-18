---
title: "Atomic BEC"
layout: textlay
excerpt: "Atomic BEC"
sitemap: false
permalink: /atomicbec
---

# Atomic BEC

Coming soon...

### Lab publications
#### Papers
{% assign atomicbec_papers = site.data.publist | where:"lab", "atomicbec" %}
{% assign paper_counter = atomicbec_papers.size %}

{% for publi in atomicbec_papers %}

  \[{{ paper_counter }}\] {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

  {% assign paper_counter = paper_counter | minus:1 %}

{% endfor %}

<p> &nbsp; </p>
#### PhD theses
{% assign combined_members = site.data.team_members | concat: site.data.alumni %}
{% assign atomicbec_theses = combined_members | where:"thesis_lab", "atomicbec" %}
{% assign thesis_by_year = atomicbec_theses | sort: "thesis_year" | reverse %}

{% for publi in thesis_by_year %}
  {% if publi.thesis_link %}
  {{publi.name}}: [_{{publi.thesis_title}}_ ({{publi.thesis_year}})]({{publi.thesis_link}})
  {% endif %}
{% endfor %}
