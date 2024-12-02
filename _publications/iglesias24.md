---
title: "Two Students: Enabling Uncertainty Quantification in Federated Learning Clients"
collection: publications
category: conferences
papertopic: ["Bioreactor"]
permalink: /publication/iglesias24
excerpt: 'This paper is about novel Bayesian approaches for federated learning.'
date: 2024-12-17
venue: 'NeurIPS 2024 Workshop BDU'
slidesurl:
paperurl: 'https://openreview.net/pdf?id=eS9xH4vHEe'
author: "C. Iglesias Jr, et al."
image: /images/bio-photo-2.jpg
citation: 'C. Iglesias Jr, S. A. de Outeiro, C. Miceli de Farias and M. Bolic, Two Students: Enabling Uncertainty Quantification in Federated Learning Clients, NeurIPS 2024 Workshop on Bayesian Decision-making and Uncertainty, 2024.'
ieee_citation: 'C. Iglesias Jr, S. A. de Outeiro, C. Miceli de Farias and M. Bolic, Two Students: Enabling Uncertainty Quantification in Federated Learning Clients, NeurIPS 2024 Workshop on Bayesian Decision-making and Uncertainty, 2024.'
---

Federated Learning (FL) is a paradigm where multiple clients collaboratively train models while keeping their data decentralized. Despite advancements in FL, uncertainty quantification (UQ) on the client side remains poorly explored. Existing methods incorporating Bayesian approaches in FL are often resource-intensive and do not directly address client-side UQ. In this paper, we propose the 2S (Two Students) approach to address this gap. Our approach distills a Bayesian model ensemble (BME) into two student models: one focused on accurate predictions and the other on uncertainty quantification. The 2S approach also includes a novel truncation filter that uses credible intervals to selectively aggregate client models, mitigating the impact of non-i.i.d. data. Through empirical validation on a regression task, we demonstrate that the 2S approach enables effective and scalable UQ on the client side, providing robust and reliable updates across decentralized data sources.
[Code](https://github.com/cristovaoiglesias/2S)
