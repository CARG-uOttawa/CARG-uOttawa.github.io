---
layout: archive
title: "CARG Health-Devices: <br/>Continous cuffless blood pressure (BP) monitoring"
excerpt: "Machine learning and signal processing advances for BP monitoring <br/><img src='/images/ContinousBPProcessing.png'>"
collection: health-devices
papertopic: BloodPressure
author_profile: true
---

<img width="500" src='/images/ContinousBPProcessing.png'>

## Motivation
The motivation behind developing cuffless blood pressure (BP) estimation techniques is largely driven by the limitations associated with traditional cuff-based methods. Conventional BP measurement methods, such as auscultatory and oscillometric techniques, are cumbersome, uncomfortable, and unsuitable for continuous long-term monitoring, which is crucial for the early diagnosis and management of hypertension and cardiovascular diseases. The use of cuffs also presents barriers for nocturnal measurements and long-term patient monitoring.

Despite the development of cuffless BP estimation techniques, there are still key challenges preventing widespread adoption. These include the need for improved model generalization, adaptation to new subjects, time-series analysis for more reliable long-term tracking, and uncertainty quantification to ensure reliability in real-world applications. Additionally, current evaluation protocols for cuffless BP devices are inadequate, as they mainly use distance-based metrics that fail to capture the models' ability to accurately track BP changes over time.

## Our Current Research
The current research focuses on enhancing cuffless BP estimation through comprehensive end-to-end frameworks. A key component of this research is the review and identification of limitations in existing methods:

* Adaptation and Calibration: Existing cuffless BP models generally train and test on the same datasets, limiting their generalizability to new subjects or different datasets. There is a need to explore model adaptation for personalized BP estimation when different devices are used.

* Time Series Analysis: The study proposes the use of time-series analysis techniques to enhance long-term BP monitoring. Current models often overlook the sequential nature of BP and related signals, which is crucial for accurate estimation.

* Uncertainty Quantification: BP estimation models must address not only accuracy but also the reliability of their predictions. Introducing Bayesian methods for uncertainty quantification ensures that the models are more interpretable and reliable, which is critical in medical applications.

* Novel Evaluation Metrics: Existing performance metrics for cuffless BP evaluation are insufficient for tracking BP changes. The research proposes new evaluation metrics that incorporate both distance and trend similarity to more accurately reflect a model's performance in tracking BP variations. These metrics are intended to ensure that models can handle the real-world variability seen in BP patterns and provide better clinical utility.

## Our Research Directions
The potential future research directions based on the findings and contributions of these studies are:

* Advanced Personalization Techniques: Exploring more sophisticated adaptation and personalization techniques, such as meta-learning and domain adaptation, to improve the accuracy of BP monitoring across diverse populations and devices.

* Improved Metrics and Real-World Validation: Developing and validating improved metrics that evaluate both accuracy and trend tracking. Validation should be carried out with clinical datasets to test the robustness of the models under various real-world conditions.

* Integration with Wearables and Multi-Modal Approaches: Integrating cuffless BP estimation with wearable technologies and other health monitoring sensors (e.g., respiration, body temperature, movement) to provide a more comprehensive assessment of cardiovascular health.

* Focus on Real-World Application and Clinical Utility: Further studies should focus on evaluating the usability and clinical utility of cuffless BP monitoring in real-world settings, including the impact of the new evaluation metrics on diagnosis, disease management, and patient outcomes.


<div class="content-container">
  <h2>Motivation</h2>

  <!-- Section: Papers -->
  <section id="publications">
    <h2>Research Papers</h2>
    <div class="paper-grid">
      {% assign topic_papers = site.publications | where_exp: "item", "item.papertopic contains page.papertopic" %}
      {% for paper in topic_papers %}
        <div class="paper-card">
          <img width="100" src="{{ paper.image }}" alt="{{ paper.title }}">
            <h3>{{ paper.title }}</h3>
            <p>By {{ paper.author }} ({{ paper.date | date: "%Y-%m-%d" }})</p>
            <a href="{{ paper.url }}" class="btn">Read More</a>
        </div>
      {% endfor %}
    </div>
  </section>

  <!-- Section: Researchers -->
<section id="people">
  <h2>Researchers</h2>
  <div class="researcher-grid">
    {% assign field_researchers = site.people | where_exp: "item", "item.field contains page.papertopic" | where: "status", "active" %}
    {% for researcher in field_researchers %}
      <div class="researcher-card">
        <img width="100" src="{{site.baseurl}}/images/people/{{researcher.avatar}}" alt="{{ researcher.name }} ">
        <h3>{{ researcher.name }}</h3>
        <p>{{ researcher.bio }}</p>
      </div>
    {% endfor %}
  </div>
</section>

<section id="alumni-researchers">
  <h2>Alumni Researchers</h2>
  <div class="researcher-grid">
    {% assign alumni_researchers = site.people | where_exp: "item", "item.field contains page.papertopic" | where: "status", "alumni" %}
    {% for researcher in alumni_researchers %}
      <div class="researcher-card">
        <h3>{{ researcher.name }}</h3>
        <p>{{ researcher.bio }}</p>
      </div>
    {% endfor %}
  </div>
</section>
</div>
