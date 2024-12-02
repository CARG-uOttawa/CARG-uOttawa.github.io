---
title: 'Object Semantics Give Us the Depth We Need: Multi-task Approach to Aerial Depth Completion'
collection: publications
category: conferences
papertopic: ["AI4LUAV"]
permalink: /publication/gazani_sh_2023_depth
excerpt: 'The paper combines aerial depth completion and object detection tasks in a multi-task network.'
date: 2023-10-01
venue: '2023 IEEE International Conference on Systems, Man, and Cybernetics (SMC)'
slidesurl:
paperurl: 'https://arxiv.org/abs/2304.12542'
author: 'Gazani, SH, Dadboud, F, Bolic, M, Mantegh, I, Najjaran, H'
image:
citation: 'S. H. Gazani, F. Dadboud, M. Bolic, I. Mantegh and H. Najjaran, Object Semantics Give Us the Depth We Need: Multi-Task Approach to Aerial Depth Completion, 2023 IEEE International Conference on Systems, Man, and Cybernetics (SMC), Honolulu, Oahu, HI, USA, 2023, pp. 2565-2570, doi: 10.1109/SMC53992.2023.10393905.'
ieee_citation: 'S. Gazani, F. Dadboud, M. Bolic, I. Mantegh, H. Najjaran,Object Semantics Give Us the Depth We Need: Multi-task Approach to Aerial Depth Completion, arXiv preprint arXiv:2304.12542, 2023.'
keywords: ''
---

## Abstract

Depth completion and object detection are two crucial tasks often used for aerial 3D mapping, path planning, and collision avoidance of Uncrewed Aerial Vehicles (UAVs). Common solutions include using measurements from a LiDAR sensor; however, the generated point cloud is often sparse and irregular and limits the system's capabilities in 3D rendering and safety-critical decision-making. To mitigate this challenge, information from other sensors on the UAV (viz., a camera used for object detection) is utilized to help the depth completion process generate denser 3D models. Performing both aerial depth completion and object detection tasks while fusing the data from the two sensors poses a challenge to resource efficiency. We address this challenge by proposing a novel approach to jointly execute the two tasks in a single pass. The proposed method is based on an encoder-focused multi-task learning model that exposes the two tasks to jointly learned features. We demonstrate how semantic expectations of the objects in the scene learned by the object detection pathway can boost the performance of the depth completion pathway while placing the missing depth values. Experimental results show that the proposed multi-task network outperforms its single-task counterpart, particularly when exposed to defective inputs.
