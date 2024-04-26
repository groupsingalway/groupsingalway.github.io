---
layout: post
title: Groups in Galway 2024
background: "/img/rory-hennessey-UR-9hOEW-Ww-unsplash-cropped-min.jpeg"
---

# Abstracts

{% assign sorted_abs = site.abstracts %}

{% for abs in sorted_abs %}

<br>

---


<span id="{{ abs.surname }}">
### {{ abs.title }}
#### {{ abs.speaker }} 
{{ abs.abstract }}
{% endfor %}