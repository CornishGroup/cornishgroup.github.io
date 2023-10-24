---
title: "CsYb - Cornish Labs"
layout: textlay
excerpt: "CsYb - Cornish Labs"
sitemap: false
permalink: /csyb
---

# CsYb molecules

CsYb info here...

### Lab publications
#### Papers
{% assign csyb_papers = site.data.publist | where:"lab", "csyb" %}
{% assign paper_counter = csyb_papers.size %}

{% for publi in csyb_papers %}

  \[{{ paper_counter }}\] {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

  {% assign paper_counter = paper_counter | minus:1 %}

{% endfor %}

<p> &nbsp; </p>
#### PhD theses
{% assign combined_members = site.data.team_members | concat: site.data.alumni %}
{% assign csyb_theses = combined_members | where:"thesis_lab", "csyb" %}
{% assign thesis_by_year = csyb_theses | sort: "thesis_year" | reverse %}

{% for publi in thesis_by_year %}
  {% if publi.thesis_link %}
  {{publi.name}}: [_{{publi.thesis_title}}_ ({{publi.thesis_year}})]({{publi.thesis_link}})
  {% endif %}
{% endfor %}