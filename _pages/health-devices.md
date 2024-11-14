---
layout: archive
title: "Health Devices Research Group (HDRG)"
permalink: /health-devices/
author_profile: true
---


The Health Devices Research Group (HDRG) at the University of Ottawa, was formed in 2012 with the goal of performing state-of-the-art research in monitoring physiological signals based on wearable and contactless technologies. Our vision is to develop intelligent systems that perform continuous, non-invasive and unobtrusive monitoring of vital signs, detecting falls and activities of people as well as learning and distinguishing patterns that can lead to worsening of symptoms of monitored people. We currently collaborate with the Heart Institute, The Perley and Rideau Veterans' Health Centre, National Research Council and several companies in Canada with the common goals on making our systems useful to elderly people in general, as well as people with conditions such as heart failure and arteriosclerosis. Our expertise is in biomedical instrumentation, signal processing and machine learning.

For the description of completed projects, please go to [Completed projects](https://carg-uottawa.github.io/year-archive/)

Here is the list of the current projects:

{% include base_path %}

{% assign ordered_pages = site.health-devices | sort:"order_number" %}

{% for post in site.health-devices %}
  {% include archive-single.html type="grid" %}
{% endfor %}
