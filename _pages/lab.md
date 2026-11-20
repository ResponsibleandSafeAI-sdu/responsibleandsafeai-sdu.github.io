---
layout: page
title: 
permalink: /Responsible and Safe AI Lab @ SDU/
description: 
nav: true
nav_order: 2
---

<!-- Team members and alumni are edited in _data/lab.yml, not here. -->


The Responsible and Safe AI Lab is part of the Applied Artificial Intelligence and Data Science Unit at The Mærsk Mc-Kinney Møller Institute, University of Southern Denmark. We build AI that is not only accurate, but also private, fair, transparent and dependable, and we study how AI can run efficiently on emerging quantum hardware. Our methods are developed together with partners in hospitals, industry and the life sciences, so that they solve real problems.

## Research areas

**Foundational AI.** Advancing deep learning, including graph-based and generative models, with a focus on efficiency, generalization and multimodal data.

**Responsible AI.** Privacy-preserving and trustworthy AI through federated learning, and machine unlearning methods that help AI comply with the GDPR and the EU AI Act while promoting fairness and transparency.

**Quantum AI.** Co-designing AI architectures to meet quantum requirements, so that classical AI models can be implemented efficiently in the quantum domain.

**Applied AI.** AI for healthcare, the industrial internet of things, life sciences and optics, including personalized cervical cancer screening and early detection of colorectal cancer, coronary artery calcification and dementia.

## Team

{% include lab_people.liquid people=site.data.lab.members %}

## Alumni

{% assign degrees = "PhD,Master,Bachelor" | split: "," %}
{% for degree in degrees %}
{% assign group = site.data.lab.alumni | where: "degree", degree | sort: "year" | reverse %}
{% if group.size > 0 %}

### {{ degree }}

{% include lab_people.liquid people=group show_thesis=true %}
{% endif %}
{% endfor %}
