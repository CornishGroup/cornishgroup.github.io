---
title: "Optical Tweezers - Cornish Labs"
layout: textlay
excerpt: "Optical Tweezers - Cornish Labs"
sitemap: false
permalink: /tweezers
---

# Molecules in optical tweezers

<style type="text/css">
    .carousel-caption {
        max-width: 100%;
        width:100%;
        background-color: #00000088;
        position: relative;
        left: auto;
        right: auto;
    }
    .center {
        max-width: 100%;
        height: auto;
        width: auto\9; /* ie8 */
        display: block;
        margin-left: auto;
        margin-right: auto;
    }
</style>



<div markdown="0" id="carousel" class="carousel slide" data-ride="carousel" data-interval="4000" data-pause="hover" >
    <!-- Menu -->
    <ol class="carousel-indicators">
        <li data-target="#carousel" data-slide-to="0" class="active"></li>
        <li data-target="#carousel" data-slide-to="1"></li>
        <li data-target="#carousel" data-slide-to="2"></li>
        <li data-target="#carousel" data-slide-to="3"></li>
    </ol>

    <!-- Items -->
    <div class="carousel-inner" markdown="0">
        <div class="item active">
            <img src="{{ site.url }}{{ site.baseurl }}/images/tweezerpic/experiment_composite_cropped.png" alt="Experiment composite" />
            <div class="carousel-caption mb-4 text-light">
            <p>Tweezer experimental apparatus showing the vacuum chamber where we create arrays of individually trapped RbCs molecules.</p>
            </div>
        </div>
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/tweezerpic/420nm_light_cropped.jpg" alt="420nm Rydberg light" />
            <div class="carousel-caption bg-dark mb-4 text-light">
            <p>420 nm laser light used to excite Rb atoms to energetic Rydberg states.</p>
            </div>
        </div>
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/picpic/stefan_viva.jpg" alt="Stefan viva" />
            <div class="carousel-caption bg-dark mb-4 text-light">
            <p>Congratulations to Dr. Stefan Spence of the Tweezer lab for a successful viva defence!</p>
            </div>
        </div>
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/tweezerpic/laser_table_cropped.jpg" alt="Laser table" />
            <div class="carousel-caption bg-dark mb-4 text-light">
            <p>Some of the lasers used from trapping and control of Rb and Cs atoms in our lab.</p>
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

## Overview
This experiment aims to explore new avenues of quantum science with ultracold polar molecules by forming single RbCs molecules in optical tweezers by associating individual Rb and Cs atoms.

<img src="{{ site.url }}{{ site.baseurl }}/images/tweezerpic/tweezer_array.png" alt="Experiment composite" class="center"/>

Controllable arrays of ultracold molecules offer an exciting new platform for quantum experiments. For example, such arrays may be used for quantum simulation of problems ubiquitous to condensed matter physics such as lattice spin models. Alternatively, with precise single-site control, the molecules may be independently moved around and merged together in miniature particle colliders, allowing for the study of ultracold chemistry on a single particle level where quantum effects dominate.

The group has recently realised the formation of ground state RbCs molecules trapped in individual tweezers. We are now studying the interactions of these molecules with Rb Rydberg atoms with the aim of creating a hybrid quantum system.

_Watch our short video to learn more about our work:_

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