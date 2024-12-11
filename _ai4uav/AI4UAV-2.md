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

Detection and tracking of UAVs using radars poses significant challenges because small UAVs typically have a small radar cross-section, fly at lower speed, and mostly at lower altitudes compared to larger aircraft. In addition, it is a nontrivial task to distinguish these small flying objects from birds. Signature detection from birds by itself is a difficult task, as data collection, distinguishing a single bird from a flock of flying birds and distinguishing different types of birds from a distance are all challenging tasks. Until now, several attempts to detect UAVs and distinguish them from birds using various sensors have achieved only limited success. In this project, we will develop a system for automated classification of UAVs and birds using artificial intelligence algorithms. The system will be based on processing data from radar sensor and sensor fusion of radar and camera data.




<div class="content-container">

  <!-- Section: Papers -->
  <section id="publications">
      <h2>Research Papers</h2>
      <div class="paper-grid">
        {% assign topic_papers = site.publications %}
        {% for paper in topic_papers reversed %}
          {% assign match = false %}
          {% for topic in paper.papertopic %}
            {% if topic == page.papertopic %}
              {% assign match = true %}
            {% endif %}
          {% endfor %}
          {% if match %}
            <div class="paper-card">
                <dl>
                    <dt>{{ paper.citation }}</dt>
                    <dd>- <em>Description</em>: {{ paper.excerpt }}</dd>
                </dl>
                <a href="{{ paper.url }}" class="btn">Read More</a>
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
