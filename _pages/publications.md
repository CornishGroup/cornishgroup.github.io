---
title: "Publications - Cornish Labs"
layout: gridlay
excerpt: "Publications - Cornish Labs"
sitemap: false
permalink: /publications
---


# Publications

## Group highlights

**At the end of this page, you can find a [list of recent publications](#list-of-recent-publications) and [PhD theses](#phd-theses). All papers are also available on [arXiv](https://arxiv.org/search/physics?searchtype=author&query=Cornish%2C+S+L).**

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## List of recent publications

{% assign paper_counter = site.data.publist.size %}

{% for publi in site.data.publist %}

  \[{{ paper_counter }}\] {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

  {% assign paper_counter = paper_counter | minus:1 %}

{% endfor %}

Publications prior to 2021 can be found on [Google Scholar](https://scholar.google.co.uk/citations?user=CfmFaf4AAAAJ).

<p> &nbsp; </p>

## PhD theses

{% assign combined_members = site.data.team_members | concat: site.data.alumni %}
{% assign thesis_by_year = combined_members | sort: "thesis_year" | reverse %}

{% for publi in thesis_by_year %}
  {% if publi.thesis_link %}
  {{publi.name}}: [_{{publi.thesis_title}}_ ({{publi.thesis_year}})]({{publi.thesis_link}})
  {% endif %}
{% endfor %}