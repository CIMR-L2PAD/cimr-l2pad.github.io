---
layout: page
title: Team
permalink: /team/
---

The CIMR L2PAD project is implemented by a consortium of European and Canadian partners, under the
lead of the Norwegian Meteorological Institute (MET Norway). CIMR L2PAD started in November 2023, and
is initially planned to last four years (2023-2027).

<figure style="margin:1.5rem 0;">
  <img src="/assets/img/CIMRL2PAD_Consortium_Logos.png" 
       alt="Logos of the CIMR L2PAD partners" 
       style="max-width:100%; height:auto; border-radius:4px;">
  <figcaption style="margin-top:0.5rem; font-size:0.9rem; color:#555;">
    Logos of the CIMR L2PAD consortium, led by the Norwegian Meteorological Instistute
  </figcaption>
</figure>

<div class="partners-grid">
{% for partner in site.data.partners %}
  {% include partner-card.html partner=partner %}
{% endfor %}
</div>
