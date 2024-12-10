---
title: "Hybrid AI-enabled Method for UAS and Bird Detection and Classification"
collection: publications
category: conferences
papertopic: ["CAUS", "UAVSim"]
permalink: /publication/zhang2020
slidesurl:
excerpt: 'A novel approach combining IMM filters and LSTM-based RNNs achieved 99.3% accuracy in classifying drones versus birds using synthetic trajectory data.'
date: 2020-10-01
venue: 'IEEE International Conference on Systems, Man, and Cybernetics (SMC)'
paperurl:
author: 'X. Zhang, V. Mehta, M. Bolic and I. Mantegh'
citation: 'X. Zhang, V. Mehta, M. Bolic and I. Mantegh, Hybrid AI-enabled Method for UAS and Bird Detection and Classification, IEEE International Conference on Systems, Man, and Cybernetics (SMC), 2020.'
ieee_citation: 'X. Zhang, V. Mehta, M. Bolic and I. Mantegh, Hybrid AI-enabled Method for UAS and Bird Detection and Classification, IEEE International Conference on Systems, Man, and Cybernetics (SMC), 2020.'
---

The advancement of UAS (Unmanned Aircraft Systems) technologies, and the rise in potential misuse of these vehicle platforms, and in particular small UAS (sUAS), has highlighted the demand for a robust and reliable solution for detection and classification of the aircraft (commonly referred to by Drone)vs. other flying objects. Most of the existing research addresses this problem either by extracting micro-Doppler from radar data or features from visual data. But these solutions do not perform well in all weather conditions and beyond a particular distance. To solve the problem of classifying small UASs and differentiating them from the birds, we propose a novel approach by merging classical Interactive Multiple Model tracking (IMM) filter and state of the art Recurrent Neural Network (RNN) with Long Short-Term Memory (LSTM) unit. The IMM extracts the kinematic features of the target flight trajectory and the RNN with LSTM learn the complex sequence of flight maneuvers. We generated synthetic trajectories emulating birds and drones flights using 3D kinematic models for training. The paper demonstrates that the classification accuracy of 99.3% was achieved with five-fold cross-validation on a network with convolutional layers, LSTM layers, and the dense output layer.
