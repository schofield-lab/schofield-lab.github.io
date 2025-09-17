---
---

# Atomic Frontiers in Quantum Nanoscience

We probe semiconductors and 2D materials atom-by-atom, combining experiment and theory to uncover new quantum phenomena.  Through this work, we are defining new frontiers in the field of quantum nanotechnology, driving innovation at the edge of atomic-scale science.

{% include section.html %}


{% comment %} Pull latest posts tagged 'news' and render a short list {% endcomment %}
{% assign updates = site.posts
  | where_exp: "p", "p.tags contains 'news'"
  | sort: "date"
  | reverse %}

{% capture text %}

<ul class="updates">
  <li>
    <em>2025-09-17</em> — 
    <a href="/join"><strong>PhD studentships are now available → click for more information.</strong></a> 
  </li>
  {% for post in updates limit:6 %}
    <li>
      <em>{{ post.date | date: "%Y-%m-%d" }}</em> —
      <a href="{{ post.url | relative_url }}"><strong>{{ post.title }}</strong></a>
      {% if post.excerpt %}
        — {{ post.excerpt | strip_html | truncate: 120 }} 
      {% endif %}
    </li>
  {% endfor %}
</ul>
{% endcapture %}

{%
  include feature_text.html
  title="News & announcements"
  text=text
%}



<!-- 
{% capture text %}
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
{% endcapture %}

{%
  include feature_text.html
  title="News & announcements"
  text=text
  flip=false
%} -->

---

{% capture text %}

We investigate atomic and nanoscale structure in semiconductors and 2D materials using surface-sensitive probes and simulation. Our aim is to understand—and ultimately control—quantum behaviour in these systems, enabling future electronic and quantum technologies.
{%
  include button.html
  link="publications"
  text="Read our publications"
  icon="fa-solid fa-arrow-right"
  flip=false
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/teaser/teaser-publications.jpg"
  link="publications"
  title="Publications"
  text=text
  flip=true
%}

---



{% capture text %}

We are a research group at University College London working at the atomic scale. Our team shares an interest in quantum materials and nanoscience, and we aim to provide a collaborative environment where students develop expertise while contributing to cutting-edge research.

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
  image="images/teaser/teaser-team.jpg"
  link="team"
  title="Our Team"
  text=text
%}


<!-- 
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
%} -->

