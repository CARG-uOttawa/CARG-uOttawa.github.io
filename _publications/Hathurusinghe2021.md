---
title: 'A Privacy-Preserving Approach to Extraction of Personal Information through Automatic Annotation and Federated Learning'
collection: publications
category: conferences
papertopic: ["Gen"]
permalink: /publication/Hathurusinghe2021
excerpt: 'A collaborative training of NER models through federated learning.'
date: 2021-01-01
venue: 'Proceedings of the Third Workshop on Privacy in Natural Language Processing (PrivateNLP 2021)'
slidesurl:
paperurl: 'https://aclanthology.org/2021.privatenlp-1.5'
author: 'Hathurusinghe, R., Nejadgholi, I., Bolic, M.'
image: 'https://aclanthology.org/images/acl-logo.svg'
citation: 'Rajitha Hathurusinghe, Isar Nejadgholi, and Miodrag Bolic. 2021. A Privacy-Preserving Approach to Extraction of Personal Information through Automatic Annotation and Federated Learning. In Proceedings of the Third Workshop on Privacy in Natural Language Processing, pages 36–45, Association for Computational Linguistics.'
ieee_citation: 'R. Hathurusinghe, I. Nejadgholi, M. Bolic, A Privacy-Preserving Approach to Extraction of Personal Information through Automatic Annotation and Federated Learning, arXiv preprint arXiv:2105.09198, 2021.'
keywords: ''
---

## Abstract

We curated WikiPII, an automatically labeled dataset composed of Wikipedia biography pages, annotated for personal information extraction. Although automatic annotation can lead to a high degree of label noise, it is an inexpensive process and can generate large volumes of annotated documents. We trained a BERT-based NER model with WikiPII and showed that with an adequately large training dataset, the model can significantly decrease the cost of manual information extraction, despite the high level of label noise. In a similar approach, organizations can leverage text mining techniques to create customized annotated datasets from their historical data without sharing the raw data for human annotation. Also, we explore collaborative training of NER models through federated learning when the annotation is noisy. Our results suggest that depending on the level of trust to the ML operator and the volume of the available data, distributed training can be an effective way of training a personal information identifier in a privacy-preserved manner. Research material is available at https://github.com/ratmcu/wikipiifed.
