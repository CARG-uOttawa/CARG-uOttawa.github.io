---
layout: archive
title: "Portfolio"
permalink: /health-devices/
author_profile: true
---


Dr. Bolic’s research is focused on solving practical challenges using signal processing and machine learning across multiple fields:
•	Biomedical Applications: Developing wearable and contactless monitoring solutions for healthcare, utilizing technologies like radar, thermal, depth, and RGB cameras in collaboration with medical experts to address patient monitoring needs.



{% include base_path %}

{% assign ordered_pages = site.health-devices | sort:"order_number" %}

{% for post in site.uav %}
  {% include archive-single.html type="grid" %}
{% endfor %}


*	Automotive and UAV Applications: Concentrated on UAV detection, inspection, and counter-drone strategies, with an emphasis on collecting and analyzing field data for practical solutions in safety and surveillance.
* Through modeling and simulation, his work seeks to understand complex real-world scenarios in both healthcare and UAV technologies.
