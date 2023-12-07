---
title: "CsYb: Quantum degenerate mixtures and magnetic molecules"
layout: textlay
excerpt: "CsYb: Quantum degenerate mixtures and magnetic molecules"
sitemap: false
permalink: /csyb
---

# CsYb: Quantum degenerate mixtures and magnetic molecules

{% include cornish-carousel-captions.html folder = "csybpic" %}

In the CsYb experiment, we trap and cool atoms of Caesium and Ytterbium to the quantum degenerate regime. We create dual-degenerate mixtures of Bose-Einstein condensates and study their interactions and novel quantum phases. 

We are also working towards assembling Caesium and Ytterbium atoms into CsYb molecules - the combination of an alkali-metal like Cs and a closed-shell atom like Yb.

## Quantum degenerate mixtures: Beyond mean-field interactions

The very different atomic structure of Cs and Yb makes it easy to independently manipulate them.  The large number of stable Yb isotopes allows us to tailor their interactions and quantum statistics to suit our experiments.

By using a two species mixture we can achieve a balance of intra- and interspecies interactions that allows us to observe higher order interaction terms, driven by quantum fluctuations.

This way we’ll be able to change the character of our ultra dilute quantum gas mixture to that of a liquid – instead of expanding freely, the mixture will form self-bound **quantum droplets**.

## Magnetic molecules

Unlike bi-alkali molecules produced in our other experiments, CsYb molecules have an unpaired electron. This means their ground state not only has an electric dipole moment, but also a **magnetic dipole moment**, giving us an additional handle to control. This makes them a promising experimental platform for quantum simulation of lattice spin models as well as quantum information.

We have recently observed magnetic Feshbach resonances, the first step towards assembling Cs and Yb atoms into molecules by magnetoassociation. We are also researching alternative association mechanisms like photoassociation and mergoassociation.

## Apparatus

In summer 2023, we upgraded our vacuum apparatus to include a glass cell. Ultracold Cs and Yb atoms will be transferred into this cell from the stainless-steel chamber where previous experiments were performed by optical transport.

Improved optical access in the glass cell will allow us to finely control the experimental properties of our atomic mixtures and perform high-resolution imaging of our atom clouds.

## Join us!

We are looking to recruit **a PhD student in 2024**. For more information email [s.l.cornish@durham.ac.uk](mailto:s.l.cornish@durham.ac.uk).

## Collaborations

As part of our quantum degenerate mixtures research, we actively collaborate with the <a href="https://blogs.ncl.ac.uk/quantum-matter/">Quantum Matter Research Group</a> at Newcastle University, and the <a href="https://eqop.phys.strath.ac.uk/vsf-projects/vsf-main/">Vortices in Superfluids group</a> at the University of Strathclyde.

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
