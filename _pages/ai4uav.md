---
layout: archive
title: "CARG HUB"
permalink: /hub/
author_profile: true
---
<div style="float: right; margin: 0 0 10px 10px;">
  <img src="/images/AI4UAVProjects.png" alt="UAV projects" width="500"/>
</div>


Our CARG HUB group at the University of Ottawa is all about developing

Here is the list of current projects:

<section id="section2">

{% include base_path %}
{% assign ordered_pages = site.hub | sort:"order_number" %}

{% for post in site.hub %}
  {% include archive-single.html  type="grid" %}
{% endfor %}
</section>
