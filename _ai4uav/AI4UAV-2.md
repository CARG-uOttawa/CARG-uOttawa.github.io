---
title: "CARG AI4UAV: AI-based Counter UAS Systems"
excerpt: "Deep learning models for detection and tracking of intruder UAS <br/><img src='/images/CUASSystemArchitecture.png'>"
collection: AI4UAV
papertopic: CUAS
author_profile: true
layout: archive
---
<div style="float: right; margin: 0 0 10px 10px;">
  <img src="/images/CUASSystemArchitecture.png" alt="UAV projects" width="400"/>
</div>

Rapid advancements in UAV technology demand sophisticated detection and response systems to address threats in national defense, security, and airspace safety. The CARG AI4UAV team utilizes their expertise in radar, statistical signal processing, machine learning, and computer vision to develop systems capable of detecting, classifying, and tracking UAVs using both ground and airborne sensors.

Key aspects of our research include the development of resilient AI systems that maintain reliability despite domain shifts and uncertainties. The system architecture integrates ground sensors like radar and PTZ cameras with interceptor UAVs to provide early warning, detection, tracking, and payload classification. The team tackles challenges such as long-distance object detection, ensuring model robustness with unseen data, and multi-sensor fusion. Our work combines modeling and simulations with extensive data collection. This work is supported by funding from NRC and NSERC.


<div class="content-container">

  <!-- Section: Papers -->
  <section id="publications">
      <h2>Research Papers</h2>
      {% assign topic_papers = site.publications %}
      {% assign page_topics = page.papertopic | join: ',' %}
      {% for paper in topic_papers reversed %}
        {% assign match = false %}
        {% for topic in paper.papertopic %}
          {% if page_topics contains topic %}
            {% assign match = true %}
          {% endif %}
        {% endfor %}
        {% if match %}
          <div>
            <p>{{ paper.citation }}</p>
            <p>Description: {{ paper.excerpt }}</p>
            <a href="{{ paper.url }}">Read More</a>
          </div>
        {% endif %}
      {% endfor %}
      </div>
  </section>

  <!-- Section: Researchers -->

  <h2>Researchers</h2>
  {% assign people_sorted = site.people | sort: 'joined' %}
  {% assign role_array = "pi|postdoc|gradstudent|researchstaff|visiting|projectstudent|collaborators|alumni" | split: "|" %}

  {% for role in role_array %}

  {% assign people_in_role = people_sorted | where: 'position', role %}

  <!-- Skip section if there's nobody -->
  {% if people_in_role.size == 0 %}
    {% continue %}
  {% endif %}

  <!-- Additional check to skip empty roles with no valid profiles -->
  {% assign valid_profiles = false %}
  {% for profile in people_in_role %}
  {% if profile.field contains page.papertopic %}
    {% assign valid_profiles = true %}
    {% break %}
  {% endif %}
  {% endfor %}

  {% if valid_profiles == false %}
  {% continue %}
  {% endif %}

  <div class="pos_header">
  {% if role == 'postdoc' %}
  <h3>Postdoctoral Fellows</h3>
   {% elsif role == 'pi' %}
  <h3>Principal Investigator</h3>
   {% elsif role == 'gradstudent' %}
  <h3>Graduate Students</h3>
   {% elsif role == 'researchstaff' %}
  <h3>Research Staff</h3>
   {% elsif role == 'visiting' %}
  <h3>Visiting Scholars</h3>
   {% elsif role == 'collaborators' %}
  <h3>Collaborators</h3>
  {% elsif role == 'projectstudent' %}
  <h3>M.Eng. and Undergrad Project Students</h3>
   {% elsif role == 'alumni' %}
  <h3>Alumni</h3>
  {% endif %}
  </div>


  <div class="content list people">
    {% for profile in people_sorted %}
      {% if profile.position contains role %}
       {% if profile.field contains page.papertopic %}
        <div class="list-item-people">
          <p class="list-post-title">
            {% if profile.avatar %}
              <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/{{profile.avatar}}" style="width: 70px;"></a>
            {% else %}
              <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg" style="width: 70px;"></a>
            {% endif %}
            <a class="name" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a>
          </p>
        </div>
        {% endif %}
      {% endif %}
    {% endfor %}
  </div>
  <hr>
  {% endfor %}
  <h2>External Collaborators</h2>
  <h2>Alumni</h2>
