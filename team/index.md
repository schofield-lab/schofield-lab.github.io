---
title: Team
nav:
  order: 3
  tooltip: About our team
---

# {% include icon.html icon="fa-solid fa-people-group" %}Team

We are a research group at University College London working at the atomic scale. Our team shares an interest in quantum materials and nanoscience, and we aim to provide a collaborative environment where students develop expertise while contributing to cutting-edge research.


{% include section.html %}

{% include list.html data="members" component="portrait" filter="role == 'principal-investigator'" %}
{% include list.html data="members" component="portrait" filter="role == 'phd'" %}

{% include section.html %}

TWe also host long- and short-term visiting PhD students, who contribute to specific projects and collaborations.


{% include section.html %}

{% include list.html data="members" component="portrait" filter="role == 'visitor'" %}

{% include section.html %}

Our work is centred on the ultrahigh vacuum low-temperature scanning tunnelling microscopy (LT-STM) laboratory in the London Centre for Nanotechnology. We also make frequent use of synchrotron facilities and collaborate with partners in theory and experiment in the UK and abroad.



{% include section.html %}

{% capture content %}

{% include figure.html image="images/team/team-becky-graduation.jpg" caption="Becky and her PhD examiner, Sam Jarvis" %}
{% include figure.html image="images/team/team-ltstm.jpg" caption="Emma and Procopi working on the LT-STM" %}
{% include figure.html image="images/team/team-ltstm-santa.jpg" caption="LT-STM getting the Christmas spirit" %}

{% endcapture %}

{% include grid.html style="square" content=content %}


{% include section.html %}

# {% include icon.html icon="fa-solid fa-graduation-cap" %}Alumni

{% include section.html %}

## Postdoctoral

<ul>
{% for alum in site.data.alumni.postdoctoral %}
  <li>
    <strong>{{ alum.name }}</strong> ({{ alum.years }})  
    {% if alum.destination %}
    <br>
    Destination: {{ alum.destination }}
    {% endif %}
  </li>
{% endfor %}
</ul>


## PhD 

<ul>
{% for alum in site.data.alumni.phd %}
  <li>
    <strong>{{ alum.name }}</strong> ({{ alum.years }})  
    <br>
    {{ alum.supervision }} 
    <br>
    Thesis: <em>{{ alum.thesis }}</em>  
    {% if alum.destination %}
    <br>
    Post-PhD Destination: {{ alum.destination }}
    {% endif %}
  </li>
{% endfor %}
</ul>


## Visiting PhD Students 

<ul>
{% for v in site.data.alumni.visitors %}
  <li>
    <strong>{{ v.name }}</strong> ({{ v.years }}) — {{ v.affiliation }}{% if v.note %}. <em>{{ v.note }}</em>{% endif %}
  </li>
{% endfor %}
</ul>

## MSci and MSc Students

<ul>
{% for student in site.data.alumni.masters %}
  <li>
    <strong>{{ student.name }}</strong> ({{ student.years }}) · {{ student.degree }}{% if student.thesis %} — <em>{{ student.thesis }}</em>{% endif %}
  </li>
{% endfor %}
</ul>

## Summer Research Students

<ul>
{% for student in site.data.alumni.summer %}
  <li>
    <strong>{{ student.name }}</strong> ({{ student.years }}) · {{ student.program }}
  </li>
{% endfor %}
</ul>

