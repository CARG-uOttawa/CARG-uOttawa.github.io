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
<div class="news">
  {% if site.latest_posts != blank %}
    {% assign latest_posts_size = site.posts | size %}
    <div
      class="table-responsive"
      {% if site.latest_posts.scrollable and latest_posts_size > 3 %}
        style="max-height: 60vw"
      {% endif %}
    >
      <table class="table table-sm table-borderless">
        {% assign latest_posts = site.posts %}
        {% if site.latest_posts.limit %}
          {% assign latest_posts_limit = site.latest_posts.limit %}
        {% else %}
          {% assign latest_posts_limit = latest_posts_size %}
        {% endif %}
        {% for item in latest_posts limit: latest_posts_limit %}
          <tr>
            <th scope="row" style="width: 20%">{{ item.date | date: '%b %d, %Y' }}</th>
            <td>
              {% if item.redirect == blank %}
                <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
              {% elsif item.redirect contains '://' %}
                <a class="news-title" href="{{ item.redirect }}" target="_blank">{{ item.title }}</a>
                <svg width="2rem" height="2rem" viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
                  <path
                    d="M17 13.5v6H5v-12h6m3-3h6v6m0-6-9 9"
                    class="icon_svg-stroke"
                    stroke="#999"
                    stroke-width="1.5"
                    fill="none"
                    fill-rule="evenodd"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  ></path>
                </svg>
              {% else %}
                <a class="news-title" href="{{ item.redirect | relative_url }}">{{ item.title }}</a>
              {% endif %}
            </td>
          </tr>
        {% endfor %}
      </table>
    </div>
  {% else %}
    <p>No posts so far...</p>
  {% endif %}
</div>
