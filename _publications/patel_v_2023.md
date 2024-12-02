---
title: 'A Hybrid Framework for Object Distance Estimation using a Monocular Camera'
collection: publications
category: conferences
papertopic: [CUAS]
permalink: /publication/patel_v_2023
excerpt: 'A deep learning method for estimating the distance of intruder UAVs using a single camera.'
date: 2023-01-01
venue: '2023 IEEE/AIAA 42nd Digital Avionics Systems Conference (DASC)'
slidesurl:
paperurl: 'https://ieeexplore.ieee.org/document/10311189'
author: 'Patel, V, Mehta, V, Bolic, M, Mantegh, I'
image: ''
citation: 'Patel, V, Mehta, V, Bolic, M, Mantegh, I. A Hybrid Framework for Object Distance Estimation using a Monocular Camera. 2023 IEEE/AIAA 42nd Digital Avionics Systems Conference (DASC), 2023.'
ieee_citation: 'V. Patel, V. Mehta, M. Bolic, I. Mantegh, A Hybrid Framework for Object Distance Estimation using a Monocular Camera, 2023 IEEE/AIAA 42nd Digital Avionics Systems Conference (DASC), pp. 1--7, 2023.'
keywords: ''
---

## Abstract

Object distance estimation using the monocular camera is a challenging problem in computer vision with many practical applications. Various algorithms are developed for distance estimation using a monocular camera; some involve traditional techniques, while others are based on Deep Learning (DL). Both methods have limitations, such as requiring camera calibration parameters, limited distance estimation range, or the object of interest should be relatively large to get accurate distance estimation. Due to these drawbacks, such algorithms cannot be easily generalized for many practical applications. In this paper, we propose a hybrid monocular distance estimation framework that consists of You Look Only Once version 7 (YOLOv7) algorithm for visual object detection and linear regression model for distance estimation. For our use case, this framework is trained on our field-captured Unmanned Aerial Vehicle (UAV) dataset to detect and estimate distance of UAVs. The dataset includes videos of UAVs obtained from different Point of View (POV) using a Pan-Tilt-Zoom (PTZ) camera that captures and tracks UAVs in the large field of view. Video frames are synchronized with the distance range data obtained from Radio Detection and Ranging (RADAR) sensor which will act as ground truth for regression model. The regression model is trained on input features such as bounding box coordinates, the average number of red, blue, and yellow pixels within the bounding box, and embedded features of detected objects obtained from YOLOv7 and output were RADAR range measurements. Trained UAV detection network has mAP
<inf xmlns:mml='http://www.w3.org/1998/Math/MathML' xmlns:xlink='http://www.w3.org/1999/xlink'>0.5</inf>
 of 0.854, mAP
<inf xmlns:mml='http://www.w3.org/1998/Math/MathML' xmlns:xlink='http://www.w3.org/1999/xlink'>.5:.95</inf>
 of 0.595 and distance estimation regressor has Mean Squared Error (MSE) of 0.06375 on independent test set. We validated this framework on our field dataset and demonstrated that our approach could detect and estimate distance efficiently and accurately. This framework can be extended for any real-world monocular distance estimation use case just by retraining the YOLOv7 model for desired object detection class and regression model for object-specific distance estimation.
