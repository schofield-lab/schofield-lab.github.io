---
title: Team
permalink: /team/
description: "Meet the Schofield Group at UCL — a collaborative team of researchers and students exploring atomic-scale quantum nanoscience with STM, ARPES, and theory."
image: /images/share.jpg
image_alt: "The Schofield Group research team at UCL"
nav:
  order: 4
  tooltip: About our team
---


# {% include icon.html icon="fa-solid fa-people-group" %}Team

We are a research group at University College London working at the atomic scale. Our team shares an interest in quantum materials and nanoscience, and we aim to provide a collaborative environment where students develop expertise while contributing to cutting-edge research.


{% include section.html %}

{% include list.html data="members" component="portrait" filter="role == 'principal-investigator'" %}
{% include list.html data="members" component="portrait" filter="role == 'phd'" %}

{% include section.html %}

We also host long- and short-term visiting PhD students, who contribute to specific projects and collaborations.


{% include section.html %}

{% include list.html data="members" component="portrait" filter="role == 'visitor'" %}

{% include section.html %}

Our work is centred on the ultrahigh vacuum low-temperature scanning tunnelling microscopy (LT-STM) laboratory in the London Centre for Nanotechnology. We also make frequent use of synchrotron facilities and collaborate with partners in theory and experiment in the UK and abroad.



{% include section.html %}

{% capture content %}

{% include figure.html image="images/team/team-becky-graduation.jpg" caption="Becky and her PhD examiner, Sam Jarvis" %}
{% include figure.html image="images/team/team-desy.jpg" caption="Members of the group at Petra III/DESY" %}
{% include figure.html image="images/team/team-ltstm-santa.jpg" caption="LT-STM getting the Christmas spirit" %}

{% endcapture %}

{% include grid.html style="square" content=content %}


{% include section.html %}

# {% include icon.html icon="fa-solid fa-user-graduate" %}Current Student Supervision

{% include section.html %}

## PhD – Primary Supervision

<ul>
  <li>
    <strong>Owain Pateman</strong> (October 2026 – present)
    <br>
    Thesis topic: <em>Atomic-scale imaging of quantum defects in two-dimensional materials</em>
  </li>
  <li>
    <strong>Byron Gamble</strong> (October 2025 – present)
    <br>
    Thesis topic: <em>STM studies and device fabrication for quantum materials, co-supervised with A*STAR, Singapore</em>
  </li>
  <li>
    <strong>Sean Egan</strong> (October 2025 – present)
    <br>
    Thesis topic: <em>Atomic-scale quantum science for scalable quantum technology using silicon- and germanium-based devices</em>
  </li>
  <li>
    <strong>Georgia Predila</strong> (October 2023 – present)
    <br>
    Thesis topic: <em>Arsenic δ-doped layers in germanium studied by STM and SX-ARPES</em>
  </li>
</ul>

## MSci and MSc Students

<ul>
  <li>
    <strong>Hannah Iqbal Miah</strong> (October 2026 – present) · MSc Advanced Materials Science
    <br>
    Thesis topic: <em>First-principles study of precursor molecule adsorption and incorporation on silicon surfaces</em>
  </li>
  <li>
    <strong>Amitoj Singh</strong> (October 2026 – present) · MSc Quantum Technologies
    <br>
    Thesis topic: <em>Machine learning analysis of atomic-resolution STM images for quantum device fabrication on silicon</em>
  </li>
</ul>

## Natural Sciences Literature Review Projects

<ul>
  <li>
    <strong>Sasha Temple</strong> (October 2026 – present) · NSci
    <br>
    Literature Review Topic: <em>Tip-induced chemistry and nanographenes</em>
  </li>
</ul>

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


## PhD – Primary Supervision

<ul>
{% assign primary_phd = site.data.alumni.phd | where_exp: "alum", "alum.supervision == 'Primary supervisor'" %}
{% for alum in primary_phd %}
  <li>
    <strong>{{ alum.name }}</strong> ({{ alum.years }})  
    <br>
    Thesis: <em>{{ alum.thesis }}</em>  
    {% if alum.destination %}
    <br>
    Post-PhD Destination: {{ alum.destination }}
    {% endif %}
  </li>
{% endfor %}
</ul>

## PhD – Secondary Supervision

<ul>
{% assign secondary_phd = site.data.alumni.phd | where_exp: "alum", "alum.supervision != 'Primary supervisor'" %}
{% for alum in secondary_phd %}
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
{% assign msci_msc_alumni = site.data.alumni.masters | where_exp: "student", "student.degree != 'Natural Sciences'" %}
{% for student in msci_msc_alumni %}
  <li>
    <strong>{{ student.name }}</strong> ({{ student.years }}) · {{ student.degree }}
    {% if student.thesis %}
    <br>
    Thesis: <em>{{ student.thesis }}</em>
    {% endif %}
  </li>
{% endfor %}
</ul>

## Natural Sciences Literature Review Projects

<ul>
{% assign natsci_alumni = site.data.alumni.masters | where_exp: "student", "student.degree == 'Natural Sciences'" %}
{% for student in natsci_alumni %}
  <li>
    <strong>{{ student.name }}</strong> ({{ student.years }}) · NSci
    {% if student.thesis %}
    <br>
    Thesis: <em>{{ student.thesis }}</em>
    {% endif %}
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

