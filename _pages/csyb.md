---
title: "CsYb - Cornish Labs"
layout: textlay
excerpt: "CsYb - Cornish Labs"
sitemap: false
permalink: /csyb
---

# CsYb molecules

In the CsYb experiment, we trap and cool atoms of Caesium and Ytterbium to the quantum degenerate regime. We create dual-degenerate mixtures of Bose-Einstein condensates and study their interactions and novel quantum phases. 

We are also interested in ways to assemble Caesium and Ytterbium atoms into CsYb molecules. The molecules have both an electric and a magnetic dipole moment in the electronic ground state, making them a promising experimental platform for quantum simulation of lattice spin models. We study interspecies Feshbach resonances, which could in future be used for molecular association. 

In summer 2023, we upgraded our vacuum apparatus to include a glass cell. This will allow us to finely control the experimental properties of our atomic mixtures, and perform high-resolution imaging of our atom clouds. 

We have a PhD position available, starting autumn 2024. For more information email s.l.cornish@durham.ac.uk. 

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
