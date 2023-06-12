---
title: "Quantum Gas Microscope - Cornish Labs"
layout: textlay
excerpt: "Quantum Gas Microscope - Cornish Labs"
sitemap: false
permalink: /microscope
---

# Quantum Gas Microscope

<img src="{{ site.url }}{{ site.baseurl }}/images/microscopepic/render5square-1080x805.png" class="img-fluid rounded mx-auto center-block" style="max-width: 25%; height: auto;">

In our lab, we are building a quantum gas microscope for ultracold molecules. This is an attempt to bring together our established work on the creation and coherent control of dipolar molecules, with the exquisite spatial resolution and control afforded by recent developments in high-resolution imaging of ultracold atoms in optical lattice

## Quantum Simulation with Ultracold Molecules

Our experiment is designed to study large arrays of molecules in periodic potentials, which have been proposed as a highly versatile platform for studying quantum matter. Thanks to the long-range dipole-dipole interactions between heteronuclear molecules and coherent control over rotational states, many different aspects of quantum many-body physics can be studied. Condensed matter theorists propose using molecules in experiments like ours to study topological superfluidity, Chern insulating phases and many-body localisation phenomena, for a review see e.g. Bohn, J. L., et.al Science 357.6355 (2017). Our experiment aims to advance the techniques used to make and manipulate molecules and work towards the study of novel quantum phenomena in a regime beyond the reach of classical computation.

## Overview

In our experiment we plan to form ultracold molecules of <sup>87</sup>Rb<sup>133</sup>Cs molecules from ultracold mixtures of the two species. Atoms are cooled to ultracold temperatures in the main chamber using Degenerate Raman Sideband Cooling (1), and then loaded into an optical lattice which we can move to transfer them to a cell where we have a microscope.

<img src="{{ site.url }}{{ site.baseurl }}/images/microscopepic/ExperimentOverview.png" class="img-fluid" style="max-width: 100%; height: auto;">



## Virtual Lab tour

This image carousel shows you around our lab hardware, 



<div markdown="0" id="carousel" class="carousel slide" data-ride="carousel" data-interval="4000" data-pause="hover" >
    <!-- Menu -->
    <ol class="carousel-indicators">
        <li data-target="#carousel" data-slide-to="0" class="active"></li>
        <li data-target="#carousel" data-slide-to="1"></li>
        <li data-target="#carousel" data-slide-to="2"></li>
    </ol>

    <!-- Items -->
    <div class="carousel-inner" markdown="0">
        <div class="item active">
            <img src="{{ site.url }}{{ site.baseurl }}/images/microscopepic/microscope_lasers.jpg" alt="Slide 1" />
            <div class="carousel-caption bg-dark mb-4 text-light">
            <p>Laser Cooling Table, here we have the lasers we use for cooling <sup>87</sup>Rb,<sup>133</sup>Cs and <sup>39</sup>K. After passing through frequency control optics the light is sent to the vacuum table via optical fibre.</p>
            </div>
        </div>
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/microscopepic/microscope_SC.jpg" alt="Slide 2" />
            <div class="carousel-caption bg-dark mb-4 text-light">
            <p>Science cell. In the middle of this photo you can see the glass cell and microscope objective which we use for quantum gas microscopy. The optics around the cell are used for evaporative cooling of the atoms and forming the optical lattice used for single site resolved imaging.</p>
            </div>
        </div>
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/microscopepic/2DMOT.jpg" alt="Slide 3" />
            <div class="carousel-caption bg-dark mb-4 text-light">
            <p>2D MOT: We cool atoms from room temperature into a cold beam using a pair of 2D+ MOTs, which cool atoms and trap atoms in two dimensions, and push them in the final dimension into the main chamber. By using a small amount of cooling in the push direction we can improve the loading of atoms into the 3D mot in the main section of the chamber.</p>
            </div>
        </div>
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/microscopepic/stirap.jpg" alt="Slide 4" />
            <div class="carousel-caption bg-dark mb-4 text-light">
            <p>STIRAP lasers. These lasers will be used to tranfer molecules between a weakly bound state and the absolute ground state using a coherent process which keeps the molecules cold. As they address transitions in the bi-alkali molecule we use a high finesse cavity under vaccum (metal cylinder in top right) as a frequency refernce.</p>
            </div>
        </div>
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/microscopepic/control.jpg" alt="Slide 5" />
            <div class="carousel-caption bg-dark mb-4 text-light">
            <p>Control system. The experiment is controlled using digital and analog signals from an FPGA. We monitor the progress of the cooling on the scope, and then ultimately measure the properties of the ultracold atoms from images which are processed in real time. Other signals from the lab, such as table temperature, laser noise etc are monitored using a time series database.</p>

            </div>
        </div>
    </div>
  <a class="left carousel-control" href="#carousel" role="button" data-slide="prev">
    <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="right carousel-control" href="#carousel" role="button" data-slide="next">
    <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>





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