---
title: "Molecular BEC"
layout: textlay
excerpt: "Molecular BEC"
sitemap: false
permalink: /molecularbec
---

# Molecular BEC

Placeholder Text

### Lab publications
#### Papers
{% assign molecularbec_papers = site.data.publist | where:"lab", "molecularbec" %}
{% assign paper_counter = molecularbec_papers.size %}

{% for publi in molecularbec_papers %}

  \[{{ paper_counter }}\] {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

  {% assign paper_counter = paper_counter | minus:1 %}

{% endfor %}

<p> &nbsp; </p>
#### PhD theses
{% assign combined_members = site.data.team_members | concat: site.data.alumni %}
{% assign molecularbec_theses = combined_members | where:"thesis_lab", "molecularbec" %}
{% assign thesis_by_year = molecularbec_theses | sort: "thesis_year" | reverse %}

{% for publi in thesis_by_year %}
  {% if publi.thesis_link %}
  {{publi.name}}: [_{{publi.thesis_title}}_ ({{publi.thesis_year}})]({{publi.thesis_link}})
  {% endif %}
{% endfor %}
