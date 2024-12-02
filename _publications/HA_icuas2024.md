---
title: "DroneRanger: Vision-Driven Deep Learning for Drone Distance Estimation"
collection: publications
category: conferences
papertopic: [CAUS]
permalink: /publication/HA_icuas2024.pdf
slidesurl: /files/HA_icuas2024.pptx
excerpt: 'This paper introduces a novel approach to vision-based localization of drones using deep learning techniques.'
date: 2024-06-04
venue: '2024 International Conference on Unmanned Aircraft Systems (ICUAS)'
author: 'Azad, H, Mehta, V, Mantegh, I, Bolic, M'
paperurl: 'https://ieeexplore.ieee.org/abstract/document/10557013'
citation: 'H. Azad, V. Mehta, I. Mantegh and M. Bolic, DroneRanger: Vision-Driven Deep Learning for Drone Distance Estimation, 2024 International Conference on Unmanned Aircraft Systems (ICUAS), Chania - Crete, Greece, 2024, pp. 442-449, doi: 10.1109/ICUAS60882.2024.10557013.'
ieee_citation: 'H. Azad, V. Mehta, I. Mantegh, M. Bolic, DroneRanger: Vision-Driven Deep Learning for Drone Distance Estimation, 2024 International Conference on Unmanned Aircraft Systems (ICUAS), pp. 442--449, 2024.'
---

This paper introduces a novel approach to estimating the distance between a drone and a camera using deep learning techniques. The proposed method employs a low-complexity convolutional neural network (CNN), called DroneRanger, to analyze the captured 2D image and estimate the distance between the observer and target drones. Three types of input data for the CNN regression model are investi-gated, including extended bounding box, resized bounding box, and resized bounding box with additional size information. The effectiveness of the method is demonstrated through experi-ments conducted on both synthetic datasets built using AirSim © as well as real flight tests, showcasing its performance across various simulation conditions, including different weather and environments. Furthermore, experiments conducted on real-world data captured using camera-equipped drones validate the method's performance under practical conditions. To address uncertainties in training labels caused by imperfect localization information from GPS sensors, robust regression based on the Huber loss function is employed to improve accuracy (improvement of around 2 meters in RMSE compared to the MSE loss). These findings suggest promising prospects for accurately estimating 3D distances from 2D images (with RMSE of distance estimation error less than 5 meters and R^2 values of above 0.9 for the regression task), highlighting the potential of the proposed approach for real-world problems in drone applications such as collision avoidance between drones.
