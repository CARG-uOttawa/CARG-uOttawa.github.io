---
permalink: /
title: "Welcome to CARG at the University of Ottawa"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---
![CARG applications and research areas](/images/CARG_BlockDiagram.png){: .align-right width="300px"}
The group is performing research in the following areas:

- UAV (drone) detection and tracking, computer vision and sensor fusion, and biomedical machine learning
- Merging physical and machine learning models: signal processing, probabilistic machine learning and deep learning models.
- Improving computational efficiency of algorithms: hardware and software accelerators

It combines two subgroups:
- [Health-Devices Research Group](https://carg-uottawa.github.io/health-devices/)
- [UAV Research Group](https://carg-uottawa.github.io/uav/)

### Why we chose the name CARG
- History: this research group evolved from Computer Architecture research group (original CARG). Computer architecture research group was formed in 2008 and focused on the following topics: computer architectures, signal processing architectures, hardware and software accelerators, GPU architectures and programming and algorithmic modifications for more efficient implementation in hardware.
In recent years our research has gone in several different directions and therefore we decided to change the name of our group to Computational Analysis and Acceleration Research Group (new CARG).
- Computational analysis combines aspects of mathematical modeling, data processing, and algorithm development to produce insights that guide research and practical applications.
- Acceleration refers to techniques and technologies used to increase the speed of data processing and computation.

### Contact info
School of Electrical Engineering and Computer Science (EECS), University of Ottawa  
800 King Edward, Ottawa, Ontario, Canada, K1N 6N5  
SITE, Room 5130  
Coordinator Contact: Miodrag Bolic, [email address](mailto:mbolic@uottawa.ca)

{% include base_path %}

<!-- New style rendering if publication categories are defined -->
<div class="news">
  {% assign news_files = site.static_files | where: "dir", "/_news" %}
  {% if news_files != blank %}
    {% assign news_size = news_files | size %}
    <div
      class="table-responsive"
      {% if include.limit and site.announcements.scrollable and news_size > 3 %}
        style="max-height: 60vw"
      {% endif %}
    >
      <table class="table table-sm table-borderless">
        {% assign news = news_files | reverse %}
        {% if include.limit and site.announcements.limit %}
          {% assign news_limit = site.announcements.limit %}
        {% else %}
          {% assign news_limit = news_size %}
        {% endif %}
        {% for file in news limit: news_limit %}
          {% capture file_content %}{{ file | read_static_file }}{% endcapture %}
          {% assign front_matter_end = file_content | split: '---' | slice: 1, 1 %}
          {% assign front_matter = front_matter_end[0] | strip %}
          {% assign post_content = file_content | split: '---' | last | strip %}
          {% assign front_matter_data = front_matter | parse_yaml %}

          <tr>
            <th scope="row" style="width: 20%">{{ front_matter_data.date | date: '%b %d, %Y' }}</th>
            <td>
              {% if front_matter_data.inline %}
                {{ post_content | remove: '<p>' | remove: '</p>' | emojify }}
              {% else %}
                <a class="news-title" href="{{ file.path | relative_url }}">{{ front_matter_data.title }}</a>
              {% endif %}
            </td>
          </tr>
        {% endfor %}
      </table>
    </div>
  {% else %}
    <p>No news so far...</p>
  {% endif %}
</div>
