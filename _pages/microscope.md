---
title: "Quantum Gas Microscope - Cornish Labs"
layout: textlay
excerpt: "Quantum Gas Microscope - Cornish Labs"
sitemap: false
permalink: /microscope
---

# Quantum Gas Microscope


<a href  ="{{ site.url }}{{ site.baseurl }}/images/microscopepic/render5square-1080x805.png">
<img src="{{ site.url }}{{ site.baseurl }}/images/microscopepic/render5square-1080x805.png" class="img-fluid rounded mx-auto center-block" style="max-width: 100mm; height: auto;">
</a>

In our lab, we are building a quantum gas microscope for ultracold molecules. This is an attempt to bring together our established work on the creation and coherent control of dipolar molecules, with the exquisite spatial resolution and control afforded by recent developments in high-resolution imaging of ultracold atoms in optical lattice

## Quantum Simulation with Ultracold Molecules

Our experiment is designed to study large arrays of molecules in periodic potentials, which have been proposed as a highly versatile platform for studying quantum matter. Thanks to the long-range dipole-dipole interactions between heteronuclear molecules and coherent control over rotational states, many different aspects of quantum many-body physics can be studied. Condensed matter theorists propose using molecules in experiments like ours to study topological superfluidity, Chern insulating phases and many-body localisation phenomena, for a review see e.g. Bohn, J. L., et.al Science 357.6355 (2017). Our experiment aims to advance the techniques used to make and manipulate molecules and work towards the study of novel quantum phenomena in a regime beyond the reach of classical computation.

## Overview

In our experiment we plan to form ultracold molecules of <sup>87</sup>Rb<sup>133</sup>Cs molecules from ultracold mixtures of the two species. Atoms are cooled to ultracold temperatures in the main chamber using Degenerate Raman Sideband Cooling (1), and then loaded into an optical lattice which we can move to transfer them to a cell where we have a microscope.

<a href  ="{{ site.url }}{{ site.baseurl }}/images/microscopepic/ExperimentOverview.png">
<img src="{{ site.url }}{{ site.baseurl }}/images/microscopepic/ExperimentOverview.png" class="img-fluid" style="max-width: 100%; height: auto;">
</a>



## Virtual Lab tour

This image carousel shows you around our lab hardware, 

{% include image-gallery-captions.html folder="microscopepic" %}

{% include cornish-carousel-captions.html folder = "microscopepic" %}

Image gallery here...






### Lab publications
#### Papers
{% assign microscope_papers = site.data.publist | where:"lab", "microscope" %}
{% assign paper_counter = microscope_papers.size %}

{% for publi in microscope_papers %}

  \[{{ paper_counter }}\] {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

  {% assign paper_counter = paper_counter | minus:1 %}

{% endfor %}

<p> &nbsp; </p>
#### PhD theses
{% assign combined_members = site.data.team_members | concat: site.data.alumni %}
{% assign microscope_theses = combined_members | where:"thesis_lab", "microscope" %}
{% assign thesis_by_year = microscope_theses | sort: "thesis_year" | reverse %}

{% for publi in thesis_by_year %}
  {% if publi.thesis_link %}
  {{publi.name}}: [_{{publi.thesis_title}}_ ({{publi.thesis_year}})]({{publi.thesis_link}})
  {% endif %}
{% endfor %}