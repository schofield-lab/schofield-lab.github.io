---
title: Atomic-Scale Semiconductor Chemistry
permalink: /research/molecular-adsorption/
layout: default
topic_id: molecular-adsorption
---

## Molecular adsorption on semiconductor surfaces

This area of our research looks at how molecules adsorb and interact with semiconductor
surfaces, mainly using low-temperature STM. We study adsorption structures, reaction
pathways, and how molecules can be used as precursors for introducing dopants or for
building simple molecular devices.

---

## STM and DFT

Our experimental work is supported by density-functional theory (DFT), which helps us
interpret adsorption geometries, reaction products, and electronic structure. STM and DFT
together provide a straightforward way to link what we see in real space with the
underlying atomic-scale processes.

---

## Applications

Understanding molecule–surface interactions is important for:

- using molecular precursors to place dopants with high precision  
- exploring simple molecular electronic structures on silicon and germanium  
- investigating how adsorbed molecules modify the local electronic environment  

This page will be expanded with more examples and images in future.

---

## Selected publications

{% assign all_citations = site.data.citations | default: empty %}
{% assign ads_pubs = all_citations | where_exp: "c", "c.molecular_adsorption" %}

{% for c in ads_pubs %}
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
