---
title: "CARG Health Devices: <br/>Contactless Estimation of Vital Signs"
excerpt: "Radar-based signal processing and machine learning for detecting activities and falls and estimating vital signs. <br/><img src='/images/radar_system.png'>"
collection: health-devices
papertopic: RadarBreathing
author_profile: true
layout: archive
---

## Monitoring elderly people in nursing homes

We will develop and test a contactless monitoring system intended for use by healthcare professionals for continuous monitoring of resident’s activity and breathing patterns as well as fall detection in assisted living facilities and retirement homes. The key benefit of our system is to allow for continuous monitoring without any impact on residents’ daily routines. Monitoring without any requirement for compliance by the residents or any additional burden to the nursing staff will allow us to collect a large number of data that will lead towards in-depth understanding of the activities and needs of the residents.

## Classifying breathing patterns of heart failure patients

The objectives of the primary phase of this study are to develop and verify algorithms for estimating breathing patterns of each patient and for reliable prediction of decompensating congestive heart failure (CHF). By the end of this project, we will be able to demonstrate the ability of our technology to continuously monitor CHF patients. The key requirement is that the system be unobtrusive yet capable of continuous, accurate monitoring over distances of several meters. Initially, our prototype will be assessed in a hospital setting so as to corroborate data fidelity with currently available medical telemetry, now considered the gold standard. The eventual goal is to create a system capable of monitoring patients at home and relaying physiological alerts to care providers or emergency services in the community.


<div class="content-container">
  <h2>Motivation</h2>

  <!-- Section: Papers -->
  <section id="publications">
    <h2>Research Papers</h2>
    <div class="paper-grid">
      {% assign topic_papers = site.publications | where_exp: "item", "item.papertopic contains page.papertopic" %}
      {% for paper in topic_papers reversed%}
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
