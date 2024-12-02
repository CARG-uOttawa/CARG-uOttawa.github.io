---
layout: archive
title: "People"
permalink: /people/
author_profile: true
---
<ul>
  <li><a href="#active-researchers">Active Researchers</a></li>
  <li><a href="#alumni">Alumni</a></li>
</ul>

<h2 id="active-researchers">Active Researchers</h2>
{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "pi|postdoc|gradstudent|researchstaff|visiting|projectstudent|collaborators|alumni" | split: "|" %}

{% for role in role_array %}

{% assign people_in_role = people_sorted | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0 %}
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
<h3 id="alumni">Alumni</h3>
{% endif %}
</div>

{% if role != 'alumni' %}
<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">
          {% if profile.avatar %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/{{profile.avatar}}" style="width: 150px;"></a>
          {% else %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg" style="width: 150px;"></a>
          {% endif %}
          <a class="name" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a>
        </p>
      </div>    
    {% endif %}
  {% endfor %}
</div>
<hr>

{% else %}

<br>


| Name | Period | Status | Topic | Currently at |
|------|--------|--------|-------|--------------|
| [Saif Ahmad](https://ca.linkedin.com/in/saiftron) | 2008-2013 | PostDoc | ECG-Assisted Blood Pressure Measurement Systems |
| [Shan Zhao](https://ca.linkedin.com/in/shan-zhao-74423580) | 2010-2011 | PostDoc | Complex event processing for RFID systems |
| [Abeye Mekonnen](https://uk.linkedin.com/in/abeye-mekonnen-3414353b) | 2012-2014 | PostDoc | Simulation of the current propagation during non-invasive brain stimulation |
| [Pankaj K. Mishra](https://sg.linkedin.com/in/captainpankaj) | 2009-2010 | PostDoc | RFID for underground detection |
| [Varunkumar Mehta](https://www.linkedin.com/in/varun-mehta-b9b669a) | 2019-2022 | PostDoc | Machine learning and signal processing for breathing rate estimation and for drone tracking |
| [Somaiyeh Khodadadi](https://ir.linkedin.com/in/somaiyeh-khodadadi-karimvand-b62b1174) | 2022-2023 | PostDoc | AAV process modeling |
| [HamidReza Sadreazami](https://ca.linkedin.com/in/hamidreza-sadreazami-56baa747) | 2017-2019 | PostDoc | Fall detection using radars |
| [Daniel Shapiro](https://www.linkedin.com/in/dcshapiro/?originalSubdomain=ca) | 2018-2019 | PostDoc | Multi-Microphone Signal Processing and Machine Learning |  Lemay.ai |
| [Isar Nejadgholi](https://ca.linkedin.com/in/isarnejad) | 2013-2016 | PostDoc | Radar signal processing and classification |
| [Parisa Pouladzadeh](https://ca.linkedin.com/in/parisa-pouladzadeh-408a3437) | 2016-2016 | PostDoc | Processing video signal to detect obstructive sleep apnea |
| [Mohammad Forouzanfar](https://www.linkedin.com/pub/dir/Mohammad/Forouzanfar) | 2014-2014 | PostDoc | Classification of the human actions and breathing using CW radars |
| [Crystal Villeneuve](https://ca.linkedin.com/in/crystal-villeneuve-a93313338) | 2012-2014 | PostDoc | Clinical trial of opioid addiction to assess the extended viability of tDCS stimulation |
| [Shiva Gholami](https://www.linkedin.com/pub/dir/Shiva/Gholami) | 2014-2014 | PostDoc | Biompedance measurements |
| [Abid Muslim Malik](https://www.linkedin.com/in/abid-m-malik-38097318) | 2008-2009 | PostDoc | Compilers for multiprocessing systems on chip |
| [Subhasis Banerjee](https://www.linkedin.com/in/subhashis-banerjee-md) | 2009-2010 | PostDoc | Computer architecture research |
| [Balakumar Balasingam](https://ca.linkedin.com/in/balasingam) | 2008-2010 | PostDoc | Complexity reduction of particle filters |
| [Soojeong Lee](https://www.linkedin.com/pub/dir/Soojeong/Lee) | 2009-2010 | PostDoc | Confidence levels for blood pressure measurement |
| [Mira Vrbaski](https://ca.linkedin.com/in/miravrbaski) | 2015-2023 | PhD | [Cost-Effective Large-Scale Digital Twins Notification System with Prioritization Consideration](https://ruor.uottawa.ca/items/2a69c445-0797-42cd-927f-0d88075659c9) |
| [Hershel Caytak](https://ca.linkedin.com/in/herschelcaytak-phd) | 2011-2018 | PhD | [BioImpedance spectroscopy methods for analysis and control of neurostimulation dose](https://ruor.uottawa.ca/items/c4ff7975-a600-4392-a323-219e3d4db316) |
| [Daniel Shapiro](https://ca.linkedin.com/in/dcshapiro) | 2008-2017 | PhD | [Composing Recommendations Using Computer Screen Images: A Deep Learning Recommender System for PC Users](https://ruor.uottawa.ca/bitstream/10393/36272/3/Shapiro_Daniel_2017_thesis.pdf) |
| [Jing Wang](https://ky.linkedin.com/in/jing-wang-576a3772) | 2012-2017 | PhD | [Indoor Localization using Augmented UHF RFID System for the Internet-of-Things](https://ruor.uottawa.ca/bitstream/10393/32588/1/Wang_Jing_2015_Thesis.pdf) |
| [Mohamed Mabrouk](https://ca.linkedin.com/in/mohamed-mabrouk-baa72213a) | 2012-2015 | PhD | [Signal Processing of Ultra-Wideband Radar Signals for Human Detection behind Walls](https://ruor.uottawa.ca/bitstream/10393/31945/1/Mabrouk_Mohamed_2015_thesis.pdf) |
| [Frédéric Mustière](https://fr.linkedin.com/in/frederic-gosselin-8a8720bb) | 2006-2010 | PhD | [Speech enhancement in real-world environments using state-space based algorithms](https://ruor.uottawa.ca/server/api/core/bitstreams/288324b2-3341-487c-bbba-91169e622941/content) |
| [Brady Laska](https://ca.linkedin.com/in/brady-laska-17720211) | 2007-2010 | PhD | [Transform Domain Model-Based Wideband Speech Enhancement with Hearing Aid Applications](https://ruor.uottawa.ca/bitstreams/20f99b21-0d2e-4b3d-9f55-5c6073f91dfd/download) |
| [Farzaneh Bannazadeh](https://ca.linkedin.com/in/farzaneh-bannazadeh) | 2022-2024 | M.Sc. | [Model Predictive Control for Dissolved Oxygen and Temperature to Study Adeno-Associated Virus (AAV) Production in Bioreactor](https://ruor.uottawa.ca/bitstreams/2b22b510-68e2-4689-81db-b184a53fd7b3/download) |
| [Hamid Asad](https://ca.linkedin.com/in/asad-hamid-588455b) | 2021-2023 | M.Sc. | [Deep learning based drone localization and payload detection using vision data](https://ruor.uottawa.ca/bitstream/10393/41540/1/Asad_Hala_2020_Thesis.pdf) |
| [Khurram Shafiq](https://ca.linkedin.com/in/khurram-shafiq-336966123) | 2019-2023 | M.Sc. | [Drone Detection and Classification using Machine Learning](https://ruor.uottawa.ca/bitstreams/5cc42600-d568-4b4e-a242-d7765b0025fe/download) |
| [Zixiong Han](https://ca.linkedin.com/in/zixiong-han-093a58177) | 2018-2021 | M.Sc. | [Respiratory Patterns Classification using UWB radar](https://ruor.uottawa.ca/items/cc1b9f82-4843-457d-96ad-a7804326e156) |
| [Fan Yang](https://ca.linkedin.com/in/fan-yang-a7900818) | 2018-2021 | M.Sc. | [Object detection for contactless vital sign estimation](https://ruor.uottawa.ca/bitstream/10393/42297/1/Yang_Fan_2021_thesis.pdf) |
| Rajitha Hathurusinghe | 2018-2020 | M.Sc. | [Building a Personally Identifiable Information Recognizer in a Privacy Preserved Manner using Automated Annotation and Federated Learning](https://ruor.uottawa.ca/items/a2f123ee-edf3-455e-b21c-76afd524a8e3) |
| [Shan He](https://www.linkedin.com/in/shan-he-25400b16) | 2017-2019 | M.Sc. | [Time-interval Based Blood Pressure Measurement Technique and System](https://ruor.uottawa.ca/bitstream/10393/37361/1/Hassan_Syed_2018_thesis.pdf) |
| [Isuru Gunasekara](https://ca.linkedin.com/in/isurug) | 2016-2017 | M.Sc. | [Contactless Estimation of Breathing Rate using UWB Radar](https://ruor.uottawa.ca/bitstreams/316080cd-490f-464e-95f3-affa3436000b/download) |
| [Xinyang Zhang](https://www.linkedin.com/in/zhang-xy) | 2014-2017 | M.Sc. | Characterizing performance of the radar system for breathing and heart rate estimation in real-life conditions |
| [Gregory Somers](https://ca.linkedin.com/in/greg-somers-16b659) | 2013-2016 | M.Sc. | Acceleration of Block-Aware Matrix Factorization on Heterogeneous Platforms |
| [Ovidiu Draghici](https://ca.linkedin.com/in/ovidiu-draghici-13467311) | 2010-2014 | M.Sc. | The MouthPad – a Tongue Interface for Hands-Free Computer Control |
| [Hassan Ahmad Roshan](https://zw.linkedin.com/pub/dir/Hassan+M./+/ca-0-Canada) | 2012-2013 | M.Sc. | Eloping Prevention, Occupancy Detection and Localizing System for Smart Healthcare Applications |
| [Iype Joseph](https://ca.linkedin.com/in/iypejoseph) | 2012-2013 | M.Sc. | Acceleration of Java programs on embedded GPUs |
| [Majed Rostamian](https://ca.linkedin.com/in/majed-rostamian-45569946) | 2011-2014 | M.Sc. | Localization and Proximity Detection in the Internet of Things Based on an Augmented UHF RFID System |
| [Josip Popovic](https://ca.linkedin.com/in/josip-popovic-8b3b03b) | 2009-2013 | M.Sc. | FPGA-Based Coprocessors for Clouds |
| Chamira Perera | 2010-2013 | M.Sc. | Improving Digital Control System Performance Through a Novel Jitter Compensating Method |
| Bardia Bandali | 2011-2013 | M.Sc. | Steady-State Analysis of Nonlinear Circuits using the Harmonic Balance on GPU |
| Wei Wang | 2012-2013 | M.Sc. | Accessing an FPGA-based Hardware Accelerator in a Paravirtualized Environment |
| Alexey Borisenko | 2010-2012 | M.Sc. | Augumented RFID system with localization capabilities |
| Majid Mafi | 2009-2011 | M.Sc. | Blood Pressure Estimation using Oscillometric Pulse Morphology |
| Tzu Hao Li | 2008-2011 | M.Sc. | Open Platform Semi-Passive Ultra High Frequency Radio Frequency Identification Tag |
| Michael Montcalm | 2008-2011 | M.Sc. | An ILP-based Task and Instruction Scheduling Algorithm for Instruction Set Extended Symmetrical Homogeneous Multiprocessor Systems-on-Chip |
| Vishal Thareja | 2007-2010 | M.Sc. | Design space exploration for RISC Processors |
| Silu Chen | 2008-2010 | M.Sc. | Improving Algorithms for Oscillometric Blood Pressure Estimation by Suppressing Breathing Effects |
| Jonathan Parri | 2007-2008 | M.Sc. | Effective Modeling for Selection and Integration of Custom Instructions for Hybrid System-on-Chips |
| Daniel Shapiro | 2004-2006 | M.Sc. | Design and Implementation of Instruction Set Extension Identification for a Multiprocessor System-on-chip Hardware/Software Co-design Toolchain |
| Frédéric Mustière | 2005-2008 | M.Sc. | Particle Filter methods for Speech Processing |


{% endif %}
{% endfor %}



<h3>M. Eng. students</h3>

<h3>Collaborators</h3>
