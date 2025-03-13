---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
header:
  og_image: "research/research-loadmap.png"
---

{% include base_path %}
{% assign ordered_pages = site.research | sort:"order_number" %}

My research goal is to explore and foster a data-driven modeling and control in nonlinear dynamics. The main target for nonlinear dynamics is plasma system, including MHD system and Vlasov-Maxwell kinetic system. Learning dynamics from data is important for modling complex systems and can be applied to several applications for state estimation, reduced modeling, and control. The key point of learning dynamics is to bridge the gap between physics domain knowledge and data-driven modeling, and I am now focusing on how to solve this discrepancy.

## Dynamics and Control
With increasing computational power and data availability, data-driven modeling and control have become essential in science and engineering. Traditional models rely on first-principles physics, often using PDEs for fluid dynamics, electromagnetism, and plasma physics. However, complex systems with nonlinear, high-dimensional behaviors challenge purely analytical approaches.

Data-driven methods leverage machine learning and optimization to infer governing equations and develop controllers from data, reducing reliance on explicit analytical models. Integrating these methods with physics-based insights has led to Physics-Informed Machine Learning (PIML), ensuring interpretability, stability, and generalizability

### 📌 Model reduction on nonlinear dynamic systems
* Structure-preserving model reduction for Vlasov-Poisson plasma system
  * Development of Particle-In-Cell simulation in electrostatic plasma system
  * Symplectic model reduction for preserving Hamiltonian form in reduced space

### 📌 Computational plasma physics
* Symplectic integration of Particle-In-Cell method for plasma kinetic simulations
  * Development on PIC with symplectic integration in electromagnetic plasma system
  * Spectral solver for electromagnetic PIC and application of parallel computation

## Plasma Physics (Nuclear Fusion, MHD)
In nuclear fusion, I developed physics-informed neural operator for zeorth-order plasma equilibrium for data-driven control with reinforcement learning. In addition, predicting plasma instabilities via multi-modal diagnostic data has been conducted with bayesian probabilistic learning for covering uncertainties in measurement. Lastly, I recently proceeded reactor design optimization through deep reinforcement learning.

### 📌 Data-driven modeling for fusion plasma and optimized control

* Disruption prediction in KSTAR tokamak plasma with Deep Learning
{% include archive-single.html type="grid" post=order_number[0]%}

* Data-driven modeling and control for tokamak plasma operation
{% include archive-single.html type="grid" post=order_number[1]%}

### 📌 Reactor Design Optimization
* Design optimization of a tokamak reactor with data-driven approaches
{% include archive-single.html type="grid" post=order_number[2]%}


<!-- <img src='/images/research/research-loadmap.png' alt='research-loadmap' width="100%"> -->