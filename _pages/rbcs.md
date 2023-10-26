---
title: "RbCs - Cornish Labs"
layout: textlay
excerpt: "RbCs - Cornish Labs"
sitemap: false
permalink: /rbcs
---

# RbCs molecules

This experiment aims to create a 3-dimensional (3D) lattice of RbCs molecules.

Beginning with a gas of ultracold RbCs molecules, we introduce a 3D optical lattice trapping potential. 
Molecules individually occupy sites in the lattice, creating an array of molecules confined to different positions in space (sites of the lattice). This system serves as an exciting platform for simulating quantum-mechanical models in condensed matter physics. For instance, molecules in neighbouring sites of the lattice can interact and exchange energy states which can be an analogous to spin-exchange in the Ising model. 

To achieve this goal we need three main ingredients:

• A 3D optical lattice trapping potential. 
This traps the molecules in space.
 
• A high filling-fraction of the 3D lattice. This means interactions between molecules in the lattice are strong.
 
• Long quantum coherence times between different rotational energy states of RbCs in the lattice. 
          This allows the states of different molecules in the lattice to maintain 
	  their appropriate character over the time period of simulations. 
 

### Where are we now?

We have recently made great strides in realising a 3D lattice of RbCs molecules with long coherence times between different rotational states. 
Utilising a 'magic' wavelength trap we recently produce world-leading coherence times. 'Magic' in this context means eliminating differential ac Stark shifts from the trapping light. This allowed us to observe the effects of relatively weak dipolar interactions between different molecules in the lab for the first time! 

Figures:
Long coherence time figure and dipole-dipole interaction figure 

<a href  ="{{ site.url }}{{ site.baseurl }}/images/rbcspic/Coherence+Dipole_v4.pdf">
<img src="{{ site.url }}{{ site.baseurl }}/images/rbcspic/Coherence+Dipole_v4.pdf" class="img-fluid rounded mx-auto center-block" style="max-width: 100mm; height: auto;">
</a>



We have started to install optics for a magic 3D lattice, using high-power optical fibres to launch to magic wavelength light towards the molecules for trapping. 

### The next steps

We want to load molecules into the lattice potential. The method in which to do that is to be decided. We could use an accordion lattice,




Image gallery here...




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
