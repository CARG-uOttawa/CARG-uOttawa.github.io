---
layout: archive
title: "CARG Health Devices"
permalink: /health-devices/
author_profile: true
---
<div style="float: right; margin: 0 0 10px 10px;">
  <img src="/images/HealthDevices.png" alt="UAV projects" width="400"/>
</div>

The CARG Health Devices Group at the University of Ottawa has been working since 2012 on advanced research in monitoring physiological signals through wearable and contactless technologies. Our focus is to create intelligent systems that can continuously, non-invasively, and unobtrusively monitor vital signs, detect falls, and track activities, especially for elderly individuals. We're making our systems effective for use by older adults and individuals with conditions such as heart failure and arteriosclerosis. Our expertise lies in biomedical instrumentation, signal processing, and machine learning.

We work on both contractless and wearable devices and technologies. The work on wearable devices include ECG-assisted oscillometric and BCG-assisted cuffless blood pressure monitoring. The work on contactless monitoring includes breathing and heart rate estimation and breathing pattern classification using radars, RGB, thermal and 3D cameras. 

Here is the list of current projects:

{% include base_path %}

{% assign ordered_pages = site.health-devices | sort:"order_number" %}

{% for post in site.health-devices %}
  {% include archive-single.html type="grid" %}
{% endfor %}
