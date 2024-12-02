---
title: 'How Not to Make the Joint Extended Kalman Filter Fail with Unstructured Mechanistic Models'
collection: publications
category: manuscripts
papertopic: ["Bioreactor"]
permalink: /publication/iglesias_cf_2024
excerpt: 'Addresses the problems in joint estimation of states and parameters with an extended Kalman filter.'
date: 2024-01-01
venue: 'Sensors'
slidesurl:
paperurl: 'https://www.mdpi.com/1424-8220/24/2/653'
author: 'Iglesias Jr, CF, Bolic, M'
image: 'https://pub.mdpi-res.com/img/design/mdpi-pub-logo-black-small1.svg?da3a8dcae975a41c?1732615622'
citation: 'Iglesias Jr, CF, Bolic, M. How Not to Make the Joint Extended Kalman Filter Fail with Unstructured Mechanistic Models. Sensors, 2024.'
ieee_citation: 'C. Iglesias Jr, M. Bolic, 'How Not to Make the Joint Extended Kalman Filter Fail with Unstructured Mechanistic Models,' Sensors, vol. 24, no. 2, pp. 653, 2024.'
keywords: ''
---

## Abstract

The unstructured mechanistic model (UMM) allows for modeling the macro-scale of a phenomenon without known mechanisms. This is extremely useful in biomanufacturing because using the UMM for the joint estimation of states and parameters with an extended Kalman filter (JEKF) can enable the real-time monitoring of bioprocesses with unknown mechanisms. However, the UMM commonly used in biomanufacturing contains ordinary differential equations (ODEs) with unshared parameters, weak variables, and weak terms. When such a UMM is coupled with an initial state error covariance matrix P(t=0) and a process error covariance matrix Q with uncorrelated elements, along with just one measured state variable, the joint extended Kalman filter (JEKF) fails to estimate the unshared parameters and state simultaneously. This is because the Kalman gain corresponding to the unshared parameter remains constant and equal to zero. In this work, we formally describe this failure case, present the proof of JEKF failure, and propose an approach called SANTO to side-step this failure case. The SANTO approach consists of adding a quantity to the state error covariance between the measured state variable and unshared parameter in the initial P(t = 0) of the matrix Ricatti differential equation to compute the predicted error covariance matrix of the state and prevent the Kalman gain from being zero. Our empirical evaluations using synthetic and real datasets reveal significant improvements: SANTO achieved a reduction in root-mean-square percentage error (RMSPE) of up to approximately 17% compared to the classical JEKF, indicating a substantial enhancement in estimation accuracy.
