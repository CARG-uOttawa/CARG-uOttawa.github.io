---
layout: archive
title: "Talks and presentations"
permalink: /talks/
author_profile: true
---
## Recent Talks

1.	Keynote speech: “Methods for UAV Detection,” ICCIMS conference, presented by M. Bolic, July 2024.
2.	EMBC Workshop: “Model-Based Design for Cardiovascular Monitoring Devices: Examples Using Oscillometric and Continuous Blood Pressure Methods,” presented by M. Bolic, EMBC 2024.
3.	Invited speech, “Contactless Cardiac and Respiratory Monitoring,” presented by M. Bolic, University College London, UK, 2024.
4.	Tutorial: “Quantifying Uncertainty in Measurement Devices,” presented by M. Bolic, I2MTC conference, Glasgow, UK, 2024.
5.	Invited speech, “Computer Architectures and Algorithms: From Filtering to Deep Learning,” presented by M. Bolic, CMC Canada, Accelerating AI 2022.
6.	Keynote speech, “Computer Architectures and Algorithms: From Filtering to Deep Learning,” presented by M. Bolic, EMCA Developer Conference, Ericsson, Ottawa, 2019
7.	Keynote speech, “Contactless monitoring of people,” presented by M. Bolic, Infoware 2017 in France
8.	Invited speech, “Contactless monitoring of vital signs,” presented by M. Bolic, Canadian Intellectual Property Office, 2017
9.	Invited tutorial, “Uncertainties in biomedical instrumentation and signal processing,” presented by M. Bolic, MeMea Conference, Rochester, USA, 2017.
10.	Invited speech, “Contactless monitoring of vital signs,” presented by M. Bolic, IEEE EMBS Ottawa Seminar, 2017.

{% if site.talkmap_link == true %}

<p style="text-decoration:underline;"><a href="/talkmap.html">See a map of all the places I've given a talk!</a></p>

{% endif %}

{% for post in site.talks reversed %}
  {% include archive-single-talk.html %}
{% endfor %}
