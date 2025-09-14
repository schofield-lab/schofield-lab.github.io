---
title: Contact
nav:
  order: 5
  tooltip: Email, address, and location
---

# {% include icon.html icon="fa-regular fa-envelope" %}Contact

{% capture col1 %}
<div class="contact-box" markdown="1">
**Steven R. Schofield**

Professor of Physics  
London Centre for Nanotechnology and  
Department of Physics & Astronomy  
University College London  

17–19 Gordon Street  
London WC1H 0AH, UK  

Office: Room 4.C1, LCN Building  

{%
  include button.html
  type="email"
  text="s.schofield@ucl.ac.uk"
  link="s.schofield@ucl.ac.uk"
%}

{%
  include button.html
  type="phone"
  text="+44-(0)20-7679-9965"
  link="+44-(0)20-7679-9965"
%}
{% endcapture %}



{% capture col2 %}
<figure class="figure">
  <div class="figure-image">
    <iframe
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1241.1644036080222!2d-0.1334133294025219!3d51.52552876270976!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x48761b2f7dbba21f%3A0xec138f9cd57d252!2sLondon%20Centre%20for%20Nanotechnology!5e0!3m2!1sen!2suk!4v1757878773838!5m2!1sen!2suk"
      style="width:100%; height:350px; border:0;" 
      loading="lazy" allowfullscreen
      referrerpolicy="no-referrer-when-downgrade">
    </iframe>
  </div>
  <figcaption class="figure-caption">
    Map showing location of the London Centre for Nanotechnology
  </figcaption>
</figure>
{% endcapture %}



{% include cols.html col1=col1 col2=col2 %}

---


{% include section.html dark=true %}

{% capture col1 %}
**Nearest Underground Stations** 

**Euston Square** 
(Circle line, Metropolitan line, Hammersmith & City line) 

**Warren Street** (Northern line, Victoria line)  
{% endcapture %}


{% capture col2 %}
{% endcapture %}

{% capture col3 %}
{% endcapture %}

{% include cols.html col1=col1 col2=col2 col3=col3 %}

