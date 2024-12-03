---
layout: archive
title: "CARG AI4UAV"
permalink: /ai4uav/
author_profile: true
---

## About CARG AI4UAV


## Datasets
[CUAS and Power Line Datasets](http://206.12.93.58/)

{% include base_path %}

<h2>Current projects</h2>
Here is the list of current projects:

{% include base_path %}

{% assign ordered_pages = site.ai4uav | sort:"order_number" %}
{% for post in site.ai4uav %}
  {% include archive-single.html  type="grid" %}
{% endfor %}
