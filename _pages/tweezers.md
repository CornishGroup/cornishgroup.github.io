---
title: "Optical Tweezers - Cornish Group"
layout: textlay
excerpt: "Optical Tweezers - Cornish Group"
sitemap: false
permalink: /tweezers
---

# Molecules in optical tweezers

This experiment aims to explore new avenues of quantum science with ultracold polar molecules by forming single RbCs molecules in optical tweezers by associating individual Rb and Cs atoms.

Controllable arrays of ultracold molecules offer an exciting new platform for quantum experiments. For example, such arrays may be used for quantum simulation of problems ubiquitous to condensed matter physics such as lattice spin models. Alternatively, with precise single-site control, the molecules may be independently moved around and merged together in miniature particle colliders, allowing for the study of ultracold chemistry on a single particle level where quantum effects dominate.

The group has recently realised the formation of ground state RbCs molecules trapped in individual tweezers. We are now studying the interactions of these molecules with Rb Rydberg atoms with the aim of creating a hybrid quantum system.

<div class="embed-responsive embed-responsive-16by9">>
<iframe  src="https://www.youtube.com/embed/B4qszpnSG-E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

<p> &nbsp; </p>

### Lab publications
#### Papers
{% assign tweezer_papers = site.data.publist | where:"lab", "tweezers" %}
{% assign paper_counter = tweezer_papers.size %}

{% for publi in tweezer_papers %}

  \[{{ paper_counter }}\] {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

  {% assign paper_counter = paper_counter | minus:1 %}

{% endfor %}

<p> &nbsp; </p>
#### PhD theses
{% assign combined_members = site.data.team_members | concat: site.data.alumni %}
{% assign tweezer_theses = combined_members | where:"thesis_lab", "tweezers" %}
{% assign thesis_by_year = tweezer_theses | sort: "thesis_year" | reverse %}

{% for publi in thesis_by_year %}
  {% if publi.thesis_link %}
  {{publi.name}}: [_{{publi.thesis_title}}_ ({{publi.thesis_year}})]({{publi.thesis_link}})
  {% endif %}
{% endfor %}