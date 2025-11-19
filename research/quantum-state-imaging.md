---
title: Quantum State Imaging
permalink: /research/quantum-state-imaging/
layout: default
topic_id: quantum-state-imaging
---

## Quantum state imaging

Quantum state imaging is one of the core research activities of our group.
We use low-temperature scanning tunnelling microscopy (STM) and spectroscopy to
visualise the extended quantum states of dopants and defects in semiconductors,
revealing their symmetry, spatial extent, and interactions with the surrounding lattice.

Our work combines:

- UHV cryogenic STM (atomic-resolution imaging and spectroscopy)  
- tight-binding and effective-mass theory  
- delta-doped silicon systems and 2D materials  
- ARPES and synchrotron-based measurements  

Together, these approaches allow us to probe and understand the real-space wave functions
of individual impurities and engineered atomic-scale structures.

---
## Related publications

{% assign all_citations = site.data.citations | default: empty %}
{% assign qs_pubs = all_citations | where_exp: "c", "c.quantumstateimaging" %}

{% for c in qs_pubs %}
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
