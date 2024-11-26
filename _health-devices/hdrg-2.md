---
title: "Portfolio item number 2"
excerpt: "Short description of portfolio item number 2 <br/><img src='/images/500x300.png'>"
collection: health-devices
topic: AI
---

This is an item in your portfolio. It can be have images or nice text. If you name the file .md, it will be parsed as markdown. If you name the file .html, it will be parsed as HTML.

## Research Papers
{% assign topic_papers = site.publications | where_exp: "item", "item.topic contains page.topic" %}
{% for paper in topic_papers %}
- **[{{ paper.title }}]({{ paper.url }})** by {{ paper.author }} ({{ paper.year }})
  ![Image for {{ paper.title }}]({{ paper.image }})
{% endfor %}
