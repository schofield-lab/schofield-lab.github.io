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

- Ultrahigh vacuum (UHV) cryogenic STM (atomic-resolution imaging and spectroscopy) 
- Semiconductors and two-dimensional (2D) materials
- Donors, acceptors, deep centre defects
- Tight-binding, effective-mass theory, and density functional theory (via collaboration)

Together, these approaches allow us to probe and understand the real-space wave functions
of individual impurities and engineered atomic-scale structures.

---

## Imaging a wide range of quantum states

We explore a broad range of defects in semiconductors and two-dimensional materials that
support remarkably varied quantum states. These span shallow hydrogenic dopants,
deep-level defects, vacancy-derived states, and extended structures engineered directly
on semiconductor surfaces.

A major milestone from our group was the **first real-space imaging of the hydrogenic
acceptor wave function in silicon**. This was achieved by implanting high-energy bismuth
ions to create acceptor defects below the surface. The resulting quantum states exhibit a
distinctive square-ring appearance in STM images—an anisotropic envelope that is
accurately reproduced by both effective-mass and tight-binding calculations.

![Acceptor states in silicon](/images/research/quantum-state-imaging/acceptor_silicon.jpg){: style="display:block; margin-left:auto; margin-right:auto; max-width:60%;" }

*Figure 1: STM image and effective-mass calculation of a single acceptor state in silicon.  
The STM image (middle) shows the anisotropic wavefunction amplitudes of the buried acceptor  
state on H–Si(001). The effective-mass calculation is shown in 3D and as a simulated STM  
contrast ([Nano Lett. 2025, 25, 38, 13996–14001](https://doi.org/10.1021/acs.nanolett.5c02675)).*  
{: style="text-align:center; color:#555; font-size:0.9rem;"}

Beyond dopants, we have also uncovered **excited-state behaviour in dangling bonds (DBs)**
on the hydrogen-terminated Si(001) surface. A single DB acts as a deep-centre defect—similar
to the Pb-centre—with a ground and an excited state that can be resolved directly in STM.

By engineering closely spaced pairs and larger DB assemblies, we demonstrated that these
excited states hybridise across the structure. The signature is unmistakable: **a maximum of
intensity appears between DBs**, exactly where a simple ground-state-only picture would
predict a minimum. This provides clear experimental evidence for the formation of
molecule-like excited states in surface-engineered quantum structures.

![Dangling bond atomic scale quantum dot](/images/research/quantum-state-imaging/dangling_bond_quantum_dot.jpg){: style="display:block; margin-left:auto; margin-right:auto; max-width:80%;" }

*Figure 2: Atomic-scale quantum dot fabricated from dangling bonds on a hydrogen-terminated
Si(001) surface. The six-dot system was formed by removing hydrogen atoms individually, and
supports hybridised ground and excited states extending across the full structure  
([Nature Communications 4, 1649 (2013)](https://doi.org/10.1038/ncomms2679)).*  
{: style="text-align:center; color:#555; font-size:0.9rem;"}

We have also investigated a wide range of other quantum systems, from defect-induced
charge density waves in electron-doped MoS₂ to the hydrogenic donor wave function of
arsenic in silicon. Details of these studies can be found in the selected publications
listed below.

---

## Selected publications

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
