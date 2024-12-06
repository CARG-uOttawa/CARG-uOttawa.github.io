---
title: "CARG Health Devices: <br/>Contactless Estimation of Vital Signs"
excerpt: "Radar-based signal processing and machine learning for detecting activities and falls and estimating vital signs. <br/><img src='/images/ElderlyContactless.png'>"
collection: health-devices
papertopic: RadarBreathing
author_profile: true
layout: archive
---
<div style="float: right; margin: 0 0 10px 10px;">
<video width="320" height="240" controls>
  <source src="/images/RadarActivities.mp4" type="video/mp4">
</video>
</div>

## Motivation:
We’re working on developing advanced, contactless monitoring systems to make life easier for healthcare professionals and improve outcomes for patients. Our goal is to provide continuous and reliable monitoring that doesn’t disrupt people’s daily routines or add extra work for nursing staff.

For nursing home residents, we want to better understand their activities and needs by collecting data seamlessly. For heart failure patients, we’re focused on spotting early signs of health issues so that doctors and caregivers can step in before things get worse.
________________________________________
## Current work
1.	Monitoring Elderly in Nursing Homes:
-	We’re building a contactless system that tracks residents’ activities, breathing patterns, and detects falls.
-	The system works in the background, so residents don’t have to do anything differently, and staff don’t have to take on extra tasks.
-	By collecting a lot of data over time, we’ll be able to get a clearer picture of what residents need to live healthier, safer lives.
2.	Classifying Breathing Patterns in Heart Failure Patients:
-	We’re designing algorithms to measure breathing patterns and predict when heart failure patients might be getting worse.
-	Our prototype system can monitor patients from a distance, which we’re testing in hospitals to make sure it’s as accurate as the medical equipment used today.
-	Eventually, we want to move this technology into patients’ homes, so it can send alerts to caregivers or emergency services when needed.
________________________________________
##Future directions
1.	Expanding Contactless Monitoring:
-	We want to add more features to the nursing home system, like predicting health issues early based on changes in activity or breathing patterns.
-	We’re also exploring how AI can help analyze the data to spot trends and provide better insights.
2.	Bringing CHF Monitoring Home:
-	After testing in hospitals, we’ll adapt our heart failure monitoring system for home use, so patients can stay safe and connected to their care teams without needing to visit a hospital.
3.	Adding More Sensors:
-	We’re looking into using other types of sensors, like thermal imaging or environmental monitors, to give a more complete picture of a person’s health.
4.	Making It Easy to Use:
-	We’re designing these systems to be user-friendly for both healthcare staff and the people being monitored. That means testing and improving them based on real-world feedback.


<div class="content-container">

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
