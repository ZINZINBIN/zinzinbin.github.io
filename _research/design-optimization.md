---
title: "Reactor Design Optimization"
layout: single-portfolio
excerpt: "<img src='/images/research/design-optimization.png' alt=''>"
collection: research
order_number: 30
header: 
  og_image: "research/design-optimization.png"
---

## Introduction
This research explores the application of Deep Reinforcement Learning (DRL) to optimize the design of a nuclear fusion reactor. DRL can efficiently address the challenging issues attributed to multiple physics and engineering constraints for steady-state operation. The fusion reactor design computation and the optimization code applicable to parallelization with DRL are developed. The proposed framework enables finding the optimal reactor design that satisfies the operational requirements while reducing building costs. Multi-objective design optimization for a fusion reactor is now simplified by DRL, indicating the high potential of the proposed framework for advancing the efficient and sustainable design of future reactors.

<p float = 'left'>
    <img src="/images/research/design-optimization/design-computation-scheme.png"  width="100%">
</p>

The framework for optimizing the design configuration of a tokamak is based on proximal policy optimization. As the scheme given below, the reactor design computation code acts as an environment for interacting with the agent, which determines the input design parameters required for computing plasma parameters. The training process of the agents equals to the optimization process of a tokamak reactor design. In this research, however, it is required to design specific reward functions for inducing the agent to avoid operational limits. In our case, the minimum requirements for steady-state operation are represented as tanh function of (1-x) formula, which can prevent the parameters being close to limits. 

<p float = 'left'>
    <img src="/images/research/design-optimization/design-optimization-scheme.png"  width="100%">
</p>

## Optimization
The figures below represent the comparison between original designed tokamak (left) and optimal designed tokamak based on DRL (right). We use the initial configuration of the tokamak from the grid search algorithm to find out the naive solution which satisfies the conditions for operation limit. Using single-step PPO algorithm, we can obtain the optimal design configuration of the tokamak which satisfies both the conditions and minimum cost condition, despite of some reduction in Q factor. 

- Lawson criteria 
<p float = 'left'>
    <img src="/images/research/design-optimization/lawson_comparison.png"  width="70%">
</p>

- Overall performance (Left:reference, Right:PPO)
<p float = 'left'>
    <img src="/images/research/design-optimization/project_overall.png"  width="50%">
    <img src="/images/research/design-optimization/ppo_overall.png"  width="50%">
</p>

- Design configuration (Left:reference, Right:PPO)
<p float = 'left'>
    <img src="/images/research/design-optimization/project_poloidal_design.png"  width="50%">
    <img src="/images/research/design-optimization/ppo_poloidal_design.png"  width="50%">
</p>

## Article
Jinsu Kim et al.,<a href = "https://arxiv.org/abs/2409.08231">"Design Optimization of Nuclear Fusion Reactor through Deep Reinforcement Learning"</a>, *Arxiv*., 2024

## Presentation
<iframe src="/files/Reactor-Design-Optimization.pdf" width="100%" height="500" frameborder="no" border="0" marginwidth="0" marginheight="0"></iframe>