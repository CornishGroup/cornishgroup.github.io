---
title: "Cornish Group - Team"
layout: gridlay
excerpt: "Cornish Group: Team members"
sitemap: false
permalink: /team
---

# Group Members

 **We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**

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
{% assign number_printed = 0 %}
{% for member in site.data.alumni %}

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
  <i>{% if member.years %}({{ member.years }}){% endif %}</i>
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

  {% if member.thesis_link %}
  {% if member.thesis_title %}
  [PhD thesis: _{{member.thesis_title}}_]({{member.thesis_link}})
  {% else %}
  [PhD thesis]({{member.thesis_link}})
  {% endif %}
  {% endif %}
  <p>{{ member.info }}</p>
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

<div class="row">

<!-- <div class="col-sm-4 clearfix">
<h4>Visitors</h4>
{% for member in site.data.alumni_visitors %}
{{ member.name }}
{% endfor %}
</div> -->

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
