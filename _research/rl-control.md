---
title: "Data Driven Plasma Modeling and Control"
layout: single-portfolio
excerpt: "<img src='/images/research/data-driven-control.gif' alt=''>"
collection: research
order_number: 20
header: 
  og_image: "research/data-driven-control.gif"
---

# Abstract
Achieving a high-performance and stable tokamak plasma in a steady-state operation is a critical challenge for fusion reactors. However, human trials in experiments alone are not effective in finding the optimal operating condition to achieve a high-performance plasma, due to the presence of several competing objectives such as operation limits and various instabilities. In contrast, Reinforcement learning, a dynamic decision-making method in machine learning, offers a promising approach to discovering the optimal trajectory for high-performance plasma since it can provide a powerful framework for control engineering by adaptive, data-driven, and model-free methods without a priori knowledge or a precise mathematical model of the system being controlled. Previous studies have explored feedforward beta control with a KSTAR simulator based on LSTM and plasma shape control using the MPO algorithm. Moreover, Multiple 0D parameters control also has been conducted to control several physical parameters into different target values simultaneously with summing the reward function for each controlled parameter. However, since each physical parameter depends on different dynamics and constraints, there would be a Pareto optimal case where other solutions can simultaneously improve all objectives without worsening at least one of them. This means that it is reasonable to approach multiple 0D parameters control as a multi-objective problem where the presence of several competing objectives should be considered. Therefore, we propose a new approach to tokamak plasma operation control based on multi-objective reinforcement learning. This new approach aims for learning near-optimal policies over several competing objectives including multi-parameter control under the virtual KSTAR environment. In this work, we develop the virtual KSTAR environment based on Transformer for approximating the state of the plasma in response to the control by the agent of reinforcement learning. Heating sources including NBI and EC heating, shape parameters, plasma current, and toroidal magnetic field are set as control variables. As a result, we demonstrate that the single agent can find the optimal policy that controls poloidal beta and safety factor to reach the target values simultaneously by multi-objective reinforcement learning.

<iframe src="/files/Plasma-Control-RL.pdf" width="100%" height="500" frameborder="no" border="0" marginwidth="0" marginheight="0"></iframe>

### Article
Jinsu Kim. "Tokamak Plasma Operation Control using Multi-Objective Reinforcement Learning in KSTAR" *International Fusion Plasma Conference 2023*.
[Poster](/files/Poster-Plasma-Control-RL.pdf).