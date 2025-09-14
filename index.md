---
---

# Atomic Frontiers in Quantum Nanoscience

We probe semiconductors and 2D materials atom-by-atom, combining experiment and theory to uncover new quantum phenomena.  Through this work, we are defining new frontiers in the field of quantum nanotechnology, driving innovation at the edge of atomic-scale science.





{% include section.html %}

## News & announcements

<ul>
{% for item in site.data.updates %}
  <li>
    <em>{{ item.date | date: "%Y-%m-%d" }}</em> — 
    <strong>{{ item.title }}</strong>
    {% if item.details %} – {{ item.details }}{% endif %}
    {% if item.link %} <a href="{{ item.link }}">Read more</a>{% endif %}
  </li>
{% endfor %}
</ul>

{% include section.html %}

{% capture text %}

We investigate atomic and nanoscale structure in semiconductors and 2D materials using surface-sensitive probes and simulation. Our aim is to understand—and ultimately control—quantum behaviour in these systems, enabling future electronic and quantum technologies.
{%
  include button.html
  link="research"
  text="Explore our research"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/teaser/teaser_research.jpg"
  link="research"
  title="Our Research"
  text=text
  flip=false
%}


{% include section.html %}

{% capture text %}

We investigate atomic and nanoscale structure in semiconductors and 2D materials using surface-sensitive probes and simulation. Our aim is to understand—and ultimately control—quantum behaviour in these systems, enabling future electronic and quantum technologies.
{%
  include button.html
  link="publications"
  text="Read our publications"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/teaser/teaser_publications.jpg"
  link="publications"
  title="Publications"
  text=text
  flip=true
%}







{% include section.html %}

{% capture text %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

{%
  include button.html
  link="projects"
  text="Browse our projects"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="projects"
  title="Our Projects"
  flip=true
  style="bare"
  text=text
%}



{% include section.html %}

{% capture text %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

{%
  include button.html
  link="team"
  text="Meet our team"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="team"
  title="Our Team"
  text=text
%}
