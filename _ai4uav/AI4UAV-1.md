---
title: "CARG AI4UAV: Obstacle detection and avoidance"
excerpt: "BVLoS Flights for infrastructure inspection <br/><img src='/images/BVLoSProjectOverview.jpg'>"
collection: AI4UAV
papertopic: AI4LUAV
author_profile: true
layout: archive
---
<div style="float: right; margin: 0 0 10px 10px;">
  <img src="/images/BVLoSProjectOverview.jpg" alt="UAV projects" width="300"/>
</div>

The research and technical developments sought in this project will enable UAS platforms to perform inspection, monitoring, and modeling the state of critical infra and superstructure in the BVLOS (Beyond Visual Line of Sight) mode, safely from a remote location. The threat detection and collision avoidance methods will provide the critical capability for BVLOS navigation of multiple drones to and around the infrastructure.




<div class="content-container">

  <!-- Section: Papers -->
  <section id="publications">
    <h2>Research Papers</h2>
    <div class="paper-grid">
      {% assign topic_papers = site.publications | where_exp: "item", "item.papertopic contains page.papertopic" %}
      {% for paper in topic_papers reversed %}
        <div class="paper-card">
            <dl><dt>{{ paper.citation }}</dt>
            <dd>- <em>Description</em>: {{ paper.excerpt }}</dd> </dl>
            <a href="{{ paper.url }}" class="btn">Read More</a>
        </div>
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
