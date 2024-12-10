---
title: "Simulated Dataset for the Loaded vs. Unloaded UAV Classification Problem Using Deep Learning"
collection: publications
category: conferences
papertopic: ["CAUS","UAVSim"]
permalink: /publication/HA_sas2023
slidesurl: /files/HA_sas2023.pptx
paperurl: /files/HA_sas2023.pdf
author: 'Azad, H, Mehta, V, Bolic, M, Mantegh, I'
excerpt: 'This paper introduces the first published vision dataset for the loaded vs. unloaded UAV classification problem.'
date: 2023-05-18
venue: '2023 IEEE Sensors Applications Symposium (SAS)'
paperurl: 'https://ieeexplore.ieee.org/abstract/document/10254046'
citation: 'H. Azad, V. Mehta, M. Bolic and I. Mantegh, Simulated Dataset for the Loaded vs. Unloaded UAV Classification Problem Using Deep Learning, 2023 IEEE Sensors Applications Symposium (SAS), Ottawa, ON, Canada, 2023, pp. 1-6, doi: 10.1109/SAS58821.2023.10254046.'
ieee_citation: 'H. Azad, V. Mehta, M. Bolic, I. Mantegh, Simulated Dataset for the Loaded vs. Unloaded UAV Classification Problem Using Deep Learning, 2023 IEEE Sensors Applications Symposium (SAS), pp. 1--6, 2023.'
---

Detecting payloads on Uncrewed (or Unmanned) Aerial Vehicles (UAVs) is crucial for safety and security reasons. Deep learning methods can utilize changes in UAV appearance caused by payloads for detection, but collecting sufficient training data through real tests is costly and time-consuming. Therefore, simulation can be a more practical option. This paper presents the first synthetic air-to-air vision dataset for classifying loaded vs. unloaded UAVs. The dataset includes five types of aerial vehicles with attached and hanging payloads of different colors. It also incorporates three environmental conditions (sunny, rainy, and snowy) to diversify the background in recorded videos. Annotated frames and XYZ coordinates of the camera and drone are provided. To validate the dataset, a ResNet-34 network is trained with synthetic data and tested on real UAV flight data. The classification results on the test dataset confirm the effectiveness of the synthetic dataset for payload detection. The synthetic datasetandclassificationcodes arepublicly available on GitHub (https://github.com/CARG-uOttawa/loaded-unloaded-drone-dataset/).
