---
title: "An Attention based Complex-valued Convolutional Autoencoder for GEO SA-Bi SAR Ship Target Refocusing"
collection: publications
category: conferences
permalink: /publication/sas23
excerpt: 'This paper is about deep learning approaches for radar image refocusing.'
date: 2023-09-22
venue: 'SAS 2023 Conference'
slidesurl:
paperurl: 'https://ieeexplore.ieee.org/document/10254087'
citation: 'M. Lian and M. Bolic, An Attention Based Complex-valued Convolutional Autoencoder for GEO SA-Bi SAR Ship Target Refocusing, 2023 IEEE Sensors Applications Symposium (SAS), Ottawa, ON, Canada, 2023, pp. 1-6, doi: 10.1109/SAS58821.2023.10254087.'
---

Since ship targets are defocused due to heave motions caused by ocean waves, and contaminated by background clutter under rough sea conditions, high-resolution (HR) ship imaging is a great challenge in a Geosynchronous spaceborne/airborne bistatic synthetic aperture radar (GEO SA-Bi SAR)
system. Inspired by the recent success of artificial neural network (ANN) and deep learning (DL) in optical image processing, an improved complex-valued convolutional autoencoder (ICV-CAE) based on attention mechanism is proposed for GEO SA-Bi SAR ship target imaging. Different from the conventional SAR imaging methods that depend on parameters estimation and motion compensation, the proposed ICV-CAE can be trained to learn the mapping relation between the defocused inputs and the HR SAR images of ship targets. Hence, the well trained ICV-CAE can be regarded as a refocusing processor and applied to the complex-valued GEO SA-Bi SAR signals after range compression to achieve the HR ship target refocusing and sea clutter suppression simultaneously. The correctness and effectiveness of the proposed algorithm is validated by the experiment results in both ship target refocusing and sea clutter suppression.
[Code](https://github.com/Lian-M/CV_CAE)
