---
title: "Tunable BECs"
layout: textlay
excerpt: "Tunable BECs"
sitemap: false
permalink: /bec
---

# Tunable BECs

Placeholder Text

### Lab publications
#### Papers
{% assign bec_papers = site.data.publist | where:"lab", "BEC" %}
{% assign paper_counter = bec_papers.size %}

{% for publi in bec_papers %}

  \[{{ paper_counter }}\] {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

  {% assign paper_counter = paper_counter | minus:1 %}

{% endfor %}

<p> &nbsp; </p>
#### PhD theses
{% assign combined_members = site.data.team_members | concat: site.data.alumni %}
{% assign becs_theses = combined_members | where:"thesis_lab", "BEC" %}
{% assign thesis_by_year = becs_theses | sort: "thesis_year" | reverse %}

{% for publi in thesis_by_year %}
  {% if publi.thesis_link %}
  {{publi.name}}: [_{{publi.thesis_title}}_ ({{publi.thesis_year}})]({{publi.thesis_link}})
  {% endif %}
{% endfor %}
