---
title: Atomic-Scale Semiconductor Chemistry
permalink: /research/molecular-adsorption/
layout: default
topic_id: molecular-adsorption
---

## How molecules bond, react, and transform on semiconductor surfaces

Molecules interacting with semiconductor surfaces give rise to a rich landscape of
bonding, charge transfer, and reaction pathways—behaviour that ultimately controls how
we build **atomic-scale devices** and **precision-doped materials**.

At the scale of individual molecules, adsorption is not simply “sticking to the surface”:
subtle changes in geometry, local strain, electronic structure, and charge distribution
determine whether a molecule acts as a precursor for dopant incorporation, a functional
unit in a molecular device, or something entirely different.

Our goal is to **understand and control these processes one molecule at a time**.

---

## Imaging chemistry with atomic resolution

We use **ultrahigh-vacuum, low-temperature scanning tunnelling microscopy (STM)** to
visualise how molecules adsorb, diffuse, and react on technologically important surfaces
such as silicon, germanium, and 2D materials.

STM allows us to:

- **Locate individual molecules with atomic precision**  
- **Resolve their adsorption geometries and reaction products**  
- **Track diffusion pathways, bonding configurations, and local charge states**  
- **Correlate structure with electronic signatures through STS**  

These measurements provide an atom-by-atom view of the chemistry that underpins
atomically precise fabrication strategies.

---

## What theory tells us

Our experiments are carried out in close collaboration with **first-principles DFT
modelling**, which reveals the atomistic mechanisms that STM alone cannot fully access.

Through DFT we can:

- Determine **adsorption energies and preferred binding sites**  
- Map **reaction pathways and transition states**  
- Predict **charge transfer and electronic coupling** between molecule and substrate  
- Interpret STM contrast and electronic structure in terms of real orbitals  

The combination of STM and DFT provides a **complete real- and electronic-structure
picture**, allowing us to identify the microscopic rules governing molecule–surface
interactions.

---

## Towards atomic-precision dopants and molecular devices

By understanding the chemistry at this level, we aim to **design new routes to
atomically precise dopant incorporation**, using molecular precursors that deliver donors
or acceptors exactly where they are needed on the lattice.

This work also opens possibilities for **molecular-scale electronics**, where functional
organic or organometallic molecules are integrated directly with semiconductor
surfaces to form components such as:

- single-molecule switches  
- spin-active molecular centres  
- charge-transfer complexes  
- hybrid quantum–molecular architectures  

These concepts feed directly into emerging quantum and nanoelectronic technologies.

---

## Systems we study

Our research focuses on:

- Organometallic precursors for donor and acceptor incorporation  
- Molecular adsorption on reconstructed Si(001) and Ge(001) surfaces  
- Reaction pathways of halogenated and functionalised aromatic molecules  
- Adsorption and charge-transfer behaviour on 2D materials  
- Molecule-induced defect formation and healing  
- Molecular assemblies and templated adsorption  

Each system provides insight into how molecules can be used as **tools for atomic-scale
fabrication**.

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
