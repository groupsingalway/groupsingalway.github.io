---
layout: post
title: Groups in Galway 2025
background: "/img/rory-hennessey-UR-9hOEW-Ww-unsplash-cropped-min.jpeg"
---

# Abstracts

{% assign sorted_abs = site.speakers2025 | sort: "surname" %}

{% for abs in sorted_abs %}

<br>

---


<span id="{{ abs.surname }}">
### {{ abs.title }}
#### [{{ abs.speaker }}]({{ abs.website }})
{{ abs.abstract }}
{% endfor %}