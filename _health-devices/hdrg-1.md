---
layout: archive
title: "CARG Health-Devices: <br/>Continuos blood pressure monitoring"
excerpt: "Machine learning and signal processing advances for cuffless blood pressure monitoring <br/><img src='/images/Oscillometric.png'>"
collection: health-devices
papertopic: BloodPressure
author_profile: true
---

- [Motivation](#motivation)
- [Our Current Research](#research)
- [Our Research Directions](#directions)
- [Research Papers](#publications)
- [Researchers](#researchers)

<img width="500" src='/images/ContinousBPProcessing.png'>

## Motivation
The motivation behind developing cuffless blood pressure (BP) estimation techniques is largely driven by the limitations associated with traditional cuff-based methods. Conventional BP measurement methods, such as auscultatory and oscillometric techniques, are cumbersome, uncomfortable, and unsuitable for continuous long-term monitoring, which is crucial for the early diagnosis and management of hypertension and cardiovascular diseases. The use of cuffs also presents barriers for nocturnal measurements and long-term patient monitoring.

Despite the development of cuffless BP estimation techniques, there are still key challenges preventing widespread adoption. These include the need for improved model generalization, adaptation to new subjects, time-series analysis for more reliable long-term tracking, and uncertainty quantification to ensure reliability in real-world applications. Additionally, current evaluation protocols for cuffless BP devices are inadequate, as they mainly use distance-based metrics that fail to capture the models' ability to accurately track BP changes over time.

## Our Current Research {#research}
The current research focuses on enhancing cuffless BP estimation through comprehensive end-to-end frameworks. A key component of this research is the review and identification of limitations in existing methods:

* Adaptation and Calibration: Existing cuffless BP models generally train and test on the same datasets, limiting their generalizability to new subjects or different datasets. There is a need to explore model adaptation for personalized BP estimation when different devices are used.

* Time Series Analysis: The study proposes the use of time-series analysis techniques to enhance long-term BP monitoring. Current models often overlook the sequential nature of BP and related signals, which is crucial for accurate estimation.

* Uncertainty Quantification: BP estimation models must address not only accuracy but also the reliability of their predictions. Introducing Bayesian methods for uncertainty quantification ensures that the models are more interpretable and reliable, which is critical in medical applications.

* Novel Evaluation Metrics: Existing performance metrics for cuffless BP evaluation are insufficient for tracking BP changes. The research proposes new evaluation metrics that incorporate both distance and trend similarity to more accurately reflect a model's performance in tracking BP variations. These metrics are intended to ensure that models can handle the real-world variability seen in BP patterns and provide better clinical utility.

## Our Research Directions {#directions}
The potential future research directions based on the findings and contributions of these studies are:

* Advanced Personalization Techniques: Exploring more sophisticated adaptation and personalization techniques, such as meta-learning and domain adaptation, to improve the accuracy of BP monitoring across diverse populations and devices.

* Improved Metrics and Real-World Validation: Developing and validating improved metrics that evaluate both accuracy and trend tracking. Validation should be carried out with clinical datasets to test the robustness of the models under various real-world conditions.

* Integration with Wearables and Multi-Modal Approaches: Integrating cuffless BP estimation with wearable technologies and other health monitoring sensors (e.g., respiration, body temperature, movement) to provide a more comprehensive assessment of cardiovascular health.

* Focus on Real-World Application and Clinical Utility: Further studies should focus on evaluating the usability and clinical utility of cuffless BP monitoring in real-world settings, including the impact of the new evaluation metrics on diagnosis, disease management, and patient outcomes.


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

<section id="researchers">
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
</section>

  <h2>External Collaborators</h2>
  <h2>Alumni</h2>
