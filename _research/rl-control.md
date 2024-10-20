---
title: "Data Driven Plasma Modeling and Control"
layout: single-portfolio
excerpt: "<img src='/images/research/data-driven-control.png' alt=''>"
collection: research
order_number: 20
header: 
  og_image: "research/data-driven-control.png"
---

Achieving a high-performance and stable tokamak plasma in a steady-state operation is a critical challenge for fusion reactors. However, human trials in experiments alone are not effective in finding the optimal operating condition to achieve a high-performance plasma, due to the presence of several competing objectives such as operation limits [1] and various instabilities [2,3]. In contrast, Reinforcement learning [4,5], a dynamic decision-making method in machine learning, offers a promising approach to discovering the optimal trajectory for high-performance plasma since it can provide a powerful framework for control engineering by adaptive, data-driven, and model-free methods without a priori knowledge or a precise mathematical model of the system being controlled. Previous studies have explored feedforward beta control with a KSTAR simulator based on LSTM [6] and plasma shape control using the MPO algorithm [7]. Moreover, Multiple 0D parameters control also has been conducted to control several physical parameters into different target values simultaneously with summing the reward function for each controlled parameter [8]. However, since each physical parameter depends on different dynamics and constraints, there would be a Pareto optimal case where other solutions can simultaneously improve all objectives without worsening at least one of them. This means that it is reasonable to approach multiple 0D parameters control as a multi-objective problem where the presence of several competing objectives should be considered. Therefore, we propose a new approach to tokamak plasma operation control based on multi-objective reinforcement learning. This new approach aims for learning near-optimal policies over several competing objectives including multi-parameter control under the virtual KSTAR environment. In this work, we develop the virtual KSTAR environment based on Transformer [9] for approximating the state of the plasma in response to the control by the agent of reinforcement learning. Heating sources including NBI and EC heating, shape parameters, plasma current, and toroidal magnetic field are set as control variables. As a result, we demonstrate that the single agent can find the optimal policy that controls poloidal beta and safety factor to reach the target values simultaneously by multi-objective reinforcement learning.

### References
[1] H.R.Koslowski, “Operational Limits and Limiting instabilities in Tokamak machines”, Transactions of fusion science and technology, 61:2T,96-103 (2012) 
[2] J.A.Wesson et al, “Disruptions in JET”, Nucl.Fusion 29 (1989)
[3] M.F.Turner and J.A.Wesson, “Transprot, Instability and Disruption in Tokamak”, Nucl. Fusion 22 (1982)
[4] L.P.Kaelbling, M.L.Littman and A.W.Moore, “Reinforcement Learning : A Survey”, Journal of Artificial Intelligence Research, Vol.4 (1996)
[5] Yuxi Li, “Deep Reinforcement Learning : An Overview”, arXiv preprint arXiv : 1701.07274 (2017)
[6] J.Seo, Y.-S.Na, B.Kim, C.Y.Lee, M.S.Park, S.J.Park and Y.H.Lee, “Feedforward beta control in the KSTAR tokamak by deep reinforcement learning”, Nucl. Fusion 61 (2021)
[7] Degrave,J., Felici, F., Buchli,J. et al, “Magnetic control of tokamak plasmas through deep reinforcement learning”, Nature 602, 414-419 (2022)
[8] J.Seo, Y.-S.Na, B.Kim, C.Y.Lee, M.S.Park, S.J.Park and Y.H.Lee, “Development of an operation trajectory design algorithm for control of multiple 0D parameters using deep reinforcement learning in KSTAR”, Nucl.Fusion 62 (2022)
[9] Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N.Gomez, Lukasz Kaiser and Lllia Polosukhin, “Attention is All You Need”, NIPS 2017 (2017)


### Article
Jinsu Kim. "Tokamak Plasma Operation Control using Multi-Objective Reinforcement Learning in KSTAR" *International Fusion Plasma Conference 2023*.
[Poster](/files/Poster-Plasma-Control-RL.pdf).