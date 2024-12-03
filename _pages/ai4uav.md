---
layout: archive
title: "CARG AI4UAV"
permalink: /ai4uav/
author_profile: true
---
<div style="float: right; margin: 0 0 10px 10px;">
  <img src="/images/AI4UAVProjects.png" alt="UAV projects" width="400"/>
</div>

Our CARG AI4UAV group at the University of Ottawa is all about developing smarter ways to detect and deal with UAVs  that could pose a threat. We are working on everything from detecting UAVs and tracking their movements to figuring out what they are carrying and understanding their intentions. To do this, we use a mix of technologies—like radar, cameras and RF, and leverage advanced machine learning to handle challenges like tracking multiple targets and identifying objects from far away.

A big part of our work is making sure our AI systems are resilient, meaning they can keep performing well even in unpredictable or previously unseen situations. We’re pushing the boundaries of resilient AI for countering drones, focusing on things like sensor fusion, payload detection, and building complex systems that work reliably. With UAVs becoming more advanced, our goal is to create adaptable solutions that can keep up with these growing capabilities and handle real-world challenges effectively.

Here is the list of current projects:


{% include base_path %}
{% assign ordered_pages = site.ai4uav | sort:"order_number" %}

{% for post in site.ai4uav %}
  {% include archive-single.html  type="grid" %}
{% endfor %}

For the CUAS dataset that contains videos of UAVs with different backgrounds, please go to [CUAS and Power Line Datasets](http://206.12.93.58/).
