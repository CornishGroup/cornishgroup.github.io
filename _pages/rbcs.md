---
title: "RbCs - Cornish Labs"
layout: textlay
excerpt: "RbCs - Cornish Labs"
sitemap: false
permalink: /rbcs
---

# RbCs molecules

RbCs info here... Hello

### Lab publications
#### Papers
{% assign rbcs_papers = site.data.publist | where:"lab", "rbcs" %}
{% assign paper_counter = rbcs_papers.size %}

{% for publi in rbcs_papers %}

  \[{{ paper_counter }}\] {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

  {% assign paper_counter = paper_counter | minus:1 %}

{% endfor %}

<p> &nbsp; </p>
#### PhD theses
{% assign combined_members = site.data.team_members | concat: site.data.alumni %}
{% assign rbcs_theses = combined_members | where:"thesis_lab", "rbcs" %}
{% assign thesis_by_year = rbcs_theses | sort: "thesis_year" | reverse %}

{% for publi in thesis_by_year %}
  {% if publi.thesis_link %}
  {{publi.name}}: [_{{publi.thesis_title}}_ ({{publi.thesis_year}})]({{publi.thesis_link}})
  {% endif %}
{% endfor %}
