---
title: "Disruption Prediction"
layout: single-portfolio
excerpt: "<img src='/images/research/disruption-prediction.png' alt=''>"
collection: research
order_number: 10
header: 
  og_image: "research/disruption-prediction.png"
---

## Introduction
In tokamak fusion reactors, plasma disruption remains a major challenge. This phenomenon involves a rapid loss of plasma confinement, releasing significant energy and particles that can erode or melt plasma-facing components. The thermal quench phase leads to a surge in toroidal electric fields, generating runaway electrons that exacerbate material degradation. Furthermore, the sudden loss of plasma energy and current induces mechanical stresses on the vessel structure. To mitigate these risks, early and accurate disruption prediction is essential. Our work leverages advanced machine learning techniques, such as deep learning and Bayesian modeling to enhance disruption prediction. 

## Disruption prediction based on multi-modal data 
In the first research, we utilized a deep learning framework for disruption prediction in KSTAR using In-vessel Visible Inspection System (IVIS) video data and plasma 0D parameters. Especially, IVIS is benefical to use since it contains the virtual information about time-varying position and shape of plasma boundary. 

<img src="/images/research/Disruption-Prediction-Multimodal/연구_소개_12.PNG" width="100%">

The neural network trained by IVIS data results in the identification of disruptions that are verified by GradCAM and Attention rollout. Our idea is to combine this visual data with plasma 0D parameters to enhance the precision of the disruption prediction and the enhanced precision can be seen from the below. The false alarms during the begining of the plasma operation can be covered through utilization of multiple sources of data including IVIS and EFIT data.

<p float = 'left'>
  <img src="/images/research/Disruption-Prediction-Multimodal/real_time_disruption_prediction_21310.gif"  width="50%">
  <img src="/images/research/Disruption-Prediction-Multimodal/real_time_disruption_prediction_0D_21310.gif"  width="50%">
</p>

## Bayesian modeling and cause estimation for disruption prediction
For better precision without depending on multiple sources of data, the bayesian probabiliistic learning can be utilized for uncertainty modeling. Basically, neural networks following a general approach lack the capability to gauge the uncertainty of their predictions accurately. This gives rise to several pertinent concerns, including overconfidence, which manifests as excessively assured predictions even when neural networks offer a confidence interval. Bayesian neural network, the scalable stochastic neural networks trained by variational inference, can cover this issue by allowing the uncertainty computation including aleatoric and epistemic uncertainty. 

<img src="/images/research/Bayesian-Disruption-Prediction/IMAGE_05.PNG"  width="100%">
<img src="/images/research/Bayesian-Disruption-Prediction/IMAGE_06.PNG"  width="100%">

We proceeded with continuous disruption prediction with KSTAR shot 30312 with uncertainty estimation. The result showed successful disruption prediction before 680 ms from thermal quench in shot 30312 with EFIT and diagnostics. Aleatoric and epistemic uncertainty estimated over time have shown drastic increase near the transition of disruptive phase, indicating that recognizing the transition between normal and disruptive state has high aleatoric and epistemic uncertainty. However, the uncertainties decrease again while approaching to thermal quench, meaning that the distinct data distribution of disruptive phase are detectable. Below figure depicts the detailed information of shot 30312. Drastic decrease in both ECE and TCI at 10.88 (s) from below figure indicates the disruptive phase (thermal quench) while observing the fluctuation in diagnostics and plasma current.  

<img src="/images/research/Bayesian-Disruption-Prediction/IMAGE_04.PNG"  width="80%">
 
Over 80% of disruptive shots in KSTAR collecting from 2019 to 2022 can be successfully predicted before 65 ms from thermal quench and about half ot disruptive shots were also predicted before 300 ms. 

## Article
Jinsu Kim et al.,<a href = "https://www.sciencedirect.com/science/article/pii/S0920379624000577">"Disruption prediction and analysis through multimodal deep learning in KSTAR"</a>, *Fusion Engineering and Design*., 2024

Jinsu Kim et al.,<a href = "https://iopscience.iop.org/article/10.1088/1361-6587/ad48b7">"Enhancing disruption prediction through Bayesian neural network in KSTAR"</a>, *Plasma Physics and Controlled Fusion*., 2024

## Presentation
<iframe src="/files/Disruption-Prediction-Multimodal.pdf" width="100%" height="500" frameborder="no" border="0" marginwidth="0" marginheight="0"></iframe>

<iframe src="/files/Bayesian-Disruption-Prediction.pdf" width="100%" height="500" frameborder="no" border="0" marginwidth="0" marginheight="0"></iframe>