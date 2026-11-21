---
layout: page
title: Alumni
permalink: /alumni/
description: Former students of the lab and their theses. Edited in _data/lab.yml.
nav: true
nav_order: 4
---

{% assign degrees = "PhD,Master,Bachelor" | split: "," %}
{% for degree in degrees %}
{% assign group = site.data.lab.alumni | where: "degree", degree | sort: "year" | reverse %}
{% if group.size > 0 %}

## {{ degree }}

{% include lab_people.liquid people=group show_thesis=true %}
{% endif %}
{% endfor %}
