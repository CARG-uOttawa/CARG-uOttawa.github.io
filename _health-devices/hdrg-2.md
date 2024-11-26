---
title: "Portfolio item number 2"
excerpt: "Short description of portfolio item number 2 <br/><img src='/images/500x300.png'>"
collection: health-devices
papertopic: AI
author_profile: true
layout: archive
---

This is an item in your portfolio. It can be have images or nice text. If you name the file .md, it will be parsed as markdown. If you name the file .html, it will be parsed as HTML.

## Research Papers
{% assign topic_papers = site.publications | where_exp: "item", "item.papertopic contains page.papertopic" %}
{% for paper in topic_papers %}
- **[{{ paper.title }}]({{ paper.url }})** by {{ paper.author }} ({{ paper.year }})
  ![Image for {{ paper.title }}]({{ publications.image }})
{% endfor %}
