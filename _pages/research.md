---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
header:
  og_image: "research/data-driven-control.png"
---

My academic research aims for data-driven modeling in nonlinear dnyamics and control, including nuclear fusion plasma. Learning dynamics via data is important for modeling complex systems and current studies have attempted combining neural network and operator theory for modling dynamics. 

In nuclear fusion, I developed physics-informed neural operator for zeorth-order plasma equilibrium for data-driven control with reinforcement learning. In addition, predicting plasma instabilities via multi-modal diagnostic data has been conducted with bayesian probabilistic learning for covering uncertainties in measurement. Lastly, I recently proceeded reactor design optimization through deep reinforcement learning.

My next reserach topics will cover reduced modeling for nonlinear dynamics including plasma through physics-informed neural operator. 

<img src='/images/research/research-loadmap.png' alt=''>

<nbsp>

{% include base_path %}

{% assign ordered_pages = site.research | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}