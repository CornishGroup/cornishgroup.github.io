---
title: "Team - Cornish Labs"
layout: gridlay
excerpt: "Team - Cornish Labs"
sitemap: false
permalink: /team
---

# Group Members

 **We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/join-us) **!**

<!-- Jump to [staff](#staff), [master and bachelor students](#master-and-bachelor-students), [alumni](#alumni), [administrative support](#administrative-support), [lab visitors](#lab-visitors). -->

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  {% if member.photo %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  {% else %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/placeholder.jpg" class="img-responsive" width="25%" style="float: left" />
  {% endif %}
  <h4>{{ member.name }}</h4>
  <p> 
  <i>{{ member.role }}</i>
  {% if member.lab == "rbcs"%}
  [RbCs lab]({{ site.url }}{{ site.baseurl }}/rbcs)
  {% elsif member.lab == "csyb"%}
  [CsYb lab]({{ site.url }}{{ site.baseurl }}/csyb)
  {% elsif member.lab == "tweezers"%}
  [Tweezers lab]({{ site.url }}{{ site.baseurl }}/tweezers)
  {% elsif member.lab == "microscope"%}
  [Microscope lab]({{ site.url }}{{ site.baseurl }}/microscope)
  {% endif %}
  </p>
  <p>[{{ member.email }}](mailto:{{ member.email }})</p>
  <p>{{ member.links }}</p>
  {% if member.thesis_link %}
  {% if member.thesis_title %}
  [PhD thesis: _{{member.thesis_title}}_]({{member.thesis_link}})
  {% else %}
  [PhD thesis]({{member.thesis_link}})
  {% endif %}
  {% endif %}
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <!-- <br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


## Alumni

<h4>PDRAs</h4>
{% assign pdras = site.data.alumni | where:"role", "Postdoctoral research associate" %}
{% for member in pdras %}
<p>{{ member.name }},
{% if member.lab == "rbcs"%}
[RbCs lab]({{ site.url }}{{ site.baseurl }}/rbcs),
{% elsif member.lab == "csyb"%}
[CsYb lab]({{ site.url }}{{ site.baseurl }}/csyb),
{% elsif member.lab == "tweezers"%}
[Tweezers lab]({{ site.url }}{{ site.baseurl }}/tweezers),
{% elsif member.lab == "microscope"%}
[Microscope lab]({{ site.url }}{{ site.baseurl }}/microscope),
{% endif %}
{% if member.years %}{{ member.years }}{% endif %}
{% if member.thesis_link %}
([PhD thesis]({{member.thesis_link}}))
{% endif %}
{{ member.info }}
</p>
{% endfor %}

<h4>PhD students</h4>
{% assign phds = site.data.alumni | where:"role", "PhD student" %}
{% for member in phds %}
<p>{{ member.name }},
{% if member.lab == "rbcs"%}
[RbCs lab]({{ site.url }}{{ site.baseurl }}/rbcs),
{% elsif member.lab == "csyb"%}
[CsYb lab]({{ site.url }}{{ site.baseurl }}/csyb),
{% elsif member.lab == "tweezers"%}
[Tweezers lab]({{ site.url }}{{ site.baseurl }}/tweezers),
{% elsif member.lab == "microscope"%}
[Microscope lab]({{ site.url }}{{ site.baseurl }}/microscope),
{% endif %}
{% if member.years %}{{ member.years }}{% endif %}
{% if member.thesis_link %}
([PhD thesis]({{member.thesis_link}}))
{% endif %}
{{ member.info }}
</p>
{% endfor %}

<div class="row">
<div class="col-sm-6 clearfix">
<h4>Masters students</h4>
{% for member in site.data.alumni_masters %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-6 clearfix">
<h4>Summer students</h4>
{% for member in site.data.alumni_summer %}
{{ member.name }}
{% endfor %}
</div>

</div>
