---
title: "RbCs - Cornish Labs"
layout: textlay
excerpt: "RbCs - Cornish Labs"
sitemap: false
permalink: /rbcs
---

# RbCs molecules

This experiment aims to create a 3-dimensional (3D) lattice of RbCs molecules. 

Beginning with a gas of ultracold RbCs molecules, we plan to introduce a 3D optical lattice trapping potential. 
Molecules individually occupy sites in the lattice, creating an array of molecules confined to different positions in space (sites of the lattice). This system serves as an exciting platform for simulating quantum-mechanical models in condensed matter physics. For instance, molecules in neighbouring sites of the lattice can interact and exchange energy states which can be an analogous to spin-exchange in the Ising model. 

<a href  ="{{ site.url }}{{ site.baseurl }}/images/rbcspic/into fig.PNG">
<img src="{{ site.url }}{{ site.baseurl }}/images/rbcspic/into fig.PNG" class="img-fluid rounded mx-auto center-block" style="max-width: 175mm; height: auto;">
</a>

###### Figure


To achieve this goal we need three main ingredients:

• A 3D optical lattice trapping potential. 
This traps the molecules in space.
 
• A high filling-fraction of the 3D lattice. This means interactions between molecules in the lattice are strong.
 
• Long quantum coherence times between different rotational energy states of RbCs in the lattice. 
          This allows the states of different molecules in the lattice to maintain 
	  their appropriate character over the time period of simulations. 
 

### Magic wavelength trapping

We have recently made great strides in realising a 3D lattice of RbCs molecules with long coherence times between different rotational states. 
Utilising a 'magic' wavelength, we recently produce world-leading coherence times of diatomic molecules in an optical trap. 'Magic' in this context means eliminating differential ac Stark shifts from the trapping light. This allowed us to observe the effects of relatively weak dipolar interactions between different molecules in the lab for the first time! 


<a href  ="{{ site.url }}{{ site.baseurl }}/images/rbcspic/coherence.png">
<img src="{{ site.url }}{{ site.baseurl }}/images/rbcspic/coherence.png" class="img-fluid rounded mx-auto center-block" style="max-width: 175mm; height: auto;">
</a>

Caption: Ramsey coherence experiment of molecules in magic trap showing world-leading coherence times of order seconds (left). Dipolar mixtures of states presented as squares and non-dipolar mixtures as circles. Dipole-dipole interactions clearly contributes to a shorter coherence time.    
Coherence time as a function of dipole-dipole interaction strength in the trap (right). Coherence time vs the reciprocal of dipole moment squared follows a linear trend, shown by the bottom-left inset. [5] 

We have started to install optics for a magic 3D lattice, using high-power optical fibres to launch the magic wavelength light towards the molecules for trapping. 
We have also taken steps to better frequency stabilize our magic laser using a ultra low expansion cavity as reference.

### The next steps

We want to load molecules into the lattice potential. The method in which to do that is to be decided. We plan to use an accordian lattice setup to help load molecules into the 3D lattice by judiciously ramping the different trapping lights on and off. We hope to see dipole-dipole interactions between many states in of the molecule in the same experiment as well as 'bulk' exchange interactions between molecules in different areas of the lattice.


{% include cornish-carousel-captions.html folder = "rbcspic" %}


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
