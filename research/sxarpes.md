---
title: Electronic Structure of Buried Quantum Systems
permalink: /research/sxarpes/
layout: default
topic_id: sxarpes
---

## Probing the electronic structure of devices hidden inside silicon

Many of the quantum systems we study are **buried deep beneath the surface of a
semiconductor crystal**—δ-doped layers only a few atoms thick, engineered quantum wells,
and atomically sharp interfaces where new electronic states emerge.

These structures are too small to see with optical microscopes, too deep for STM, and too
complex to understand from electrical measurements alone. Yet their **electronic structure**
strongly determines how they behave as quantum devices.

Our goal is to *reveal what is happening inside the crystal*.

---

## How we “see” inside a solid

We use **soft X-ray angle-resolved photoemission spectroscopy** (SX-ARPES) to access the
full three-dimensional momentum structure of electrons inside these buried layers.

At soft X-ray energies, the photoelectrons originate from much deeper below the surface
than in conventional ARPES. This allows us to:

- **Probe electronic states in δ-doped layers and buried interfaces**  
- **Map their full band structure, including the out-of-plane momentum (k₋z)**  
- **Distinguish the contributions of specific atomic species or orbitals**  

In effect, SX-ARPES acts as a **non-destructive microscope for quantum states inside a
solid**, revealing how electrons move, couple, and reorganise in engineered atomic-scale
structures.

---

## What we study

We apply SX-ARPES to understand:

- Ultra-doped silicon δ-layers and their confined electron liquids  
- Designed semiconductor heterostructures and quantum wells  
- Buried two-dimensional materials and van der Waals interfaces  
- Interface states that only exist a few atomic layers beneath the surface  

Our measurements, combined with detailed modelling, provide a **real- and
momentum-space picture** of these hidden quantum systems—information that cannot be
obtained by any other technique.

---


## Related publications

{% assign all_citations = site.data.citations | default: empty %}
{% assign sx_pubs = all_citations | where_exp: "c", "c.sxarpes" %}

{% for c in sx_pubs %}
  {% include citation.html
     affiliation=c.affiliation
     author=c.author
     authors=c.authors
     buttons=c.buttons
     caption=c.caption
     content=c.content
     date=c.date
     description=c.description
     excerpt=c.excerpt
     height=c.height
     icon=c.icon
     id=c.id
     image=c.image
     last_modified_at=c.last_modified_at
     link=c.link
     lookup=c.lookup
     name=c.name
     publisher=c.publisher
     repo=c.repo
     role=c.role
     slug=c.slug
     style="rich"
     subtitle=c.subtitle
     tags=c.tags
     text=c.text
     title=c.title
     tooltip=c.tooltip
     type=c.type
     url=c.url
     width=c.width
  %}
{% endfor %}
